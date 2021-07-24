


>

# Installing VS CODE on android

## Step 1 - install Termux

><a href="https://play.google.com/store/apps/details?id=com.termux">download termux from playstore</a>
>
>Open the termux and run command
>`pkg update && pkg upgrade`
>
>In case of any error run
>`termux-change-repo`
>to change repo, try again and make sure everthing is working fine.

## Step 2 - installing ubuntu
>Run the below command
>`pkg update -y && pkg install curl proot tar -y && curl https://raw.githubusercontent.com/AndronixApp/AndronixOrigin/master/Installer/Ubuntu20/ubuntu20-xfce.sh | bash`

>Make sure there would not be a line break between whole command.
>
>you can also run these command one by one.  Here we are running multiple commands using &&.

>After installation it will ask for create vncpassword. Type anything that you want. For me it is`android`

>Start your ubuntu using command
>`./start-ubuntu20.sh`
>
>you will be able to see ubuntu terminal path followed by `#` in termux

## Step - 3 - Downloading VS Code and code server

>Now you are in ubuntu terminal and going to install things in ubuntu.
>
>Run below command to download vs code
>`wget https://github.com/cdr/code-server/releases/download/v3.10.2/code-server-3.10.2-linux-arm64.tar.gz`

>Extract Tarball using
>`tar -xvf ./code-server-3.10.2-linux-arm64.tar.gz`
>
>Now install chromium browser
>run command
>`sudo apt-get install google-chrome-stable`

## Step - 4 - Download VNC viewer and run desktop
><a href="https://play.google.com/store/apps/details?id=com.realvnc.viewer.android">download VNC viewer from playstore</a>
>
>Run below command in termux
>  `vncserver -localhost yes`
    
>Open VNC viewer and add new server using  `+`  button type `localhost:1` for Address and for Name type anything. Let's say `Ubuntu`
>
>Press `connect` button then it will ask for password. so type that you have given. In my case it is `android`
>
>Press `OK` then you will be able to see Ubuntu screen. 

## Step - 5 - Start vs code in ubuntu

>Open terminal from the menu from top left corner. 
>Go to directry where code-server is,
>using
>`cd code-server-3.10.2-linux-arm64` 
>`cd bin`
>
>Now launch the code server using
>`./code-server --auth none`

>Open chromium browser from menu>>>Internet.
>Type `loacalhost:8080` and hit enter.
>You would be able to see vs code
>
>Here you can drag and drop any folder and work.
>
>Thankyou for reading
