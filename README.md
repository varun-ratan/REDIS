REDIS for WINDOWS

STEPS:
1. For Windows, first we need to install WSL2 (Windows Subsystem for Linux)
    -> First run cmd as an Adminitrator and then Type wsl --install
2. After that open Ubuntu which is installed by above line in your system, Setup the username and Password
3. Run below lines one by one:
		
   3.1 curl -fsSL https://packages.redis.io/gpg | sudo gpg --dearmor -o /usr/share/keyrings/redis-archive-keyring.gpg
   
   3.2 echo "deb [signed-by=/usr/share/keyrings/redis-archive-keyring.gpg] https://packages.redis.io/deb $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/redis.list
   
   3.3 sudo apt-get update
   
   3.4 sudo apt-get install redis
   
   3.5 sudo service redis-server start
   
   3.6 redis-cli
   
   After this it will show and IP just type ping, It will return PONG

