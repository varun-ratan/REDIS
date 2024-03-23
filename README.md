REDIS for WINDOWS

STEPS:
1. For Windows, first we need to install WSL2 (Windows Subsystem for Linux)
    -> First run cmd as an Adminitrator and then Type wsl --install
2. After that open Ubuntu which is installed by above line in your system, Setup the username and Password
3. Run below lines one by one
   -> curl -fsSL https://packages.redis.io/gpg | sudo gpg --dearmor -o /usr/share/keyrings/redis-archive-keyring.gpg

   -> echo "deb [signed-by=/usr/share/keyrings/redis-archive-keyring.gpg] https://packages.redis.io/deb $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/redis.list
   -> sudo apt-get update
   -> sudo apt-get install redis
   -> sudo service redis-server start
   -> redis-cli
   

