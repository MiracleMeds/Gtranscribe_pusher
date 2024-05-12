# Gtranscribe_pusher
Takes whatever output is created by google transcribe and sends the output as text to another device. The program is set up to read similarly to a group chat for the receiver, having names for each person communicating and showing up in text bubbles. 

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Developer Resources:

* Real-Time Communication Options:
  *  Websocket:
    Consider using WebSocket protocol for real-time requests between a computer and a server.
    WebSocket provides low-latency, full-duplex communication over a single, long-lived connection. Latency comparable to a phone call.
    WebSocket uses browsers though so that is a possible downside, as it limits the program's design to a website (which requires upkeep to function!)
    On the other hand, HTML & CSS are very easy to design and you are familiar with them, making the development easier.
    More on WebSocket: https://www.youtube.com/watch?v=gCkyqAjY-pM&ab_channel=CodingReflections

  *Tutorial Duuuumps:
    -----For making a server from scratch hosted at thine home:
         To host a website, you need a web server. This can be any computer with an internet connection (even a laptop!) The computer will need to be running a server operating system (Linux distributions like Ubuntu are           popular, but Windows Server is used too). Generally, you should use a different computer from your main computer. For the sake of argument, I'll assume here you'll be using a Linux server running Ubuntu rather             than pay for Windows Server.
         Once you have your computer set up, you need to give it a static local IP address
         (try 192.168.1.230). It will need to be left on 24 hours a day. Then, you need to login to your router and set up what is called 'port forwarding'. This means when web traffic arrives at your router at the ports           you forward, it is sent to the IP address of your web server. You need to forward ports 22, 80 and 443, and the process is different for each router. There are guides for different routers explaining how to do it.
         Next, you have to install a server program on your computer, like Apache or nginx. I personally use nginx. You can see how to set it up here
         and how to configure it here
         . You create a folder with the name of your website (eg example.com) in the /var/www folder (the above website would be /var/www/example.com), and create a folder called 'html' inside that. You then put the files          for your website in that folder, using SFTP through a program like WinSCP or FileZilla (the port is port 22).
         If everything has gone correctly, you should be able to navigate to example.com
         and see the index.html file in the /var/www/example.com/html folder. If you're using something like WordPress, things will be a little more complicated (you'll need to install a database like MySQL on your     
         server, for instance), but there are tutorials online for those.
         If you were using a professionally hosted web server, this is all you would need to do. However, since most home routers have dynamically assigned IP addresses that change regularly, you need to register your     
         domain name with a dynamic DNS service, which maps your domain name to your IP address. I use https://www.dynu.com/
         (you get 4 addresses for free and then it costs $9.99 per year for up to 500 addresses). If your router doesn't support dynu.com
         , then you need to run a program like ddclient
         on your server. What this does is regularly checks your IP address and updates it on dynu.com
         if it changes. You should run it as a cron job
         (scheduled task) every 15 minutes.
         Setting up a server the way I have described above requires some familiarity with the Linux command line, as Linux server distributions do not generally have graphical user interfaces. Try searching Google for   
         some Linux tutorials if you're not familiar with Linux.
