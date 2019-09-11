# SignalR-Redis

A simple ASP.NET CORE SingalR hub with some client examples and redis caching.

### Prerequisites


[.NET Core 2.2 SDK](https://dotnet.microsoft.com/download/archives) - NET Core is a cross-platform version of .NET for building websites, services, and console apps.

### Installing Redis

A step by step series of examples that tell you how to get a development env running

You can find the official Redis site below. This is where you can find a standard setup instruction, if you want to do teh set-up yourself on an accessible Linux machine.

[Official Redis site](https://redis.io/)

If you are, however, a Windows user and want to run Redis cache on the same machine that you are developing your software on, there is an unofficial Redis version for Windows available as this [GitHub project](https://github.com/MicrosoftArchive/redis). This port is very easy to set up, especially if you only intend to use it for limited testing purposes. These are the steps you should take:

1 - Download and install the latest version
Download the latest version of Redis for Windows from this [page](https://github.com/MicrosoftArchive/redis/releases). Either unzip the content of the folder (if you are using .ZIP file) or follow the installation instructions (if you are using .MSI file).

2 - Configure Redis
Navigate to the folder containing the extracted Redis files and open "redis.windows-service.conf" file. Ensure that the line that begins with "port" has the value set to "6379", i.e. "port 6379". After this, ensure that the line that begins with "bind" has the value of local IP address, i.e. "bind 127.0.0.1".

3 - Install Redis server
While in the folder, open the command line prompt and run the following command to install Redis server:
```
redis-server --service-install redis.windows-service.conf --service-name Redis6379 --port 6379
```

4 - Launch Redis server
To launch Redis server and make it useful, run the following command:
```
redis-server --service-start --service-name Redis6379
```

5 - To stop the server once you are finished with it, run the following command:
```
redis-server --service-start --service-name Redis6379 
```
###### Yep its the same command.
