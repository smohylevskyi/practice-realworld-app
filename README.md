
This repository is intended for local practice in test automation and test case writing.

# Run with Docker (currently WiP, not usable)
To run the local application execute the following command on the local machine with Docker installed.
```docker run smohylevskyi/automation-practice-application:0.2```

The command should download the Docker image from Dockerhub, build the app and launch it.
Once the application is running - it will be available by the following URLs:
[frontend](http://localhost:3000/) and [backend](http://localhost:3001/).

# Run without Docker 

## Setting up reqiured tools
To make everything work you will need ```git```, ```npm``` and ```yarn``` installed.

To install all these tools - the easiest way is to use [chocolatey](https://chocolatey.org/install)

### Installing chocolatey
This piece is copied from the chocolatey documentation.
1. Run powershell as administrator.
    * Run ```Get-ExecutionPolicy```. If it returns ```Restricted```, then run ```Set-ExecutionPolicy AllSigned``` or ```Set-ExecutionPolicy Bypass -Scope Process```.
    * Now run the following command: <br>
    ```Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))```
2. Paste the copied text into your shell and press Enter.
3. Wait a few seconds for the command to complete.
4. If you don't see any errors, you are ready to use Chocolatey! Type ```choco``` or ```choco -?``` to see if the commands are recognized.

### Installing required tools
To install all the required tools run the command line as admin and execute the following command
```choco install git yarn nodejs``` (only leave the names of tools that you do not have yet on your machine)
and follow the instructions in the command line. 

After the installation is finished you should restart the command line and ```npm```, ```yarn``` and ```git``` commands should be recognized.

## Running the app
To run the application locally you need to run the following commands one by one. 

1. ```git clone https://github.com/smohylevskyi/practice-realworld-app.git``` 
2.  ```cd .\practice-realworld-app\```
3.  ```yarn```
4.  ```yarn dev```

Once you go through the initial setup and just need to run the application - run command #4 only.

# How to use
Once the application is running locally - it will be available by the following URLs:
[frontend](http://localhost:3000/) and [backend](http://localhost:3001/).

For authentication you can register a new user with arbitrary information or just use a user [from the following JSON](https://github.com/smohylevskyi/practice-realworld-app/blob/develop/data/database.json). 
For all users the default password is ```s3cret``` (even if there's another one is the JSON). 
