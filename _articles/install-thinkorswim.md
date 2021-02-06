---
layout: article
title: Install thinkorswim Desktop
description: Install thinkorswim and ensure that all the compenents are in place to get it up and running
keywords:
  - thinkorswim
  - Electronic trading platform
  - TD Ameritrade
hidden: false
section: community

---

thinkorswim by TD Ameritrade® is an electronic trading platform written in Java that fully supports GNU/Linux. Unfortunatly, the [official documentation](https://tlc.thinkorswim.com/center/faq/technical) instructing users on the install process is somewhat lackluster. Here is a step-by-step guide on how to install thinkorswim and get it up and running on Pop!_OS Linux 20.10.

### Install the neccesary dependencies

thinkorswim depends on the Java Runtime Enviroment (JRE) version 8. To install, open Terminal and input the following:
```
sudo apt install openjdk-8-jre
```


### Download and run the installation script

Go to [the thinkorswim downloads page](https://www.tdameritrade.com/tools-and-platforms/thinkorswim/desktop/download.page), scroll down to the "Linux users" heading, and click `Install thinkorswim`. A file titled `thinkorswim_installer.sh` should be placed in your Downloads folder.

Open the files application and navigate to your downloads folder, right click on the file `thinkorswim_installer.sh`, click "Permissions," and click "Allow executing file as program."

Next, open Terminal and navigate to your Downloads folder by typing the following:
```
cd ~/Downloads
```

Run the installer by typing the following:

```
./thinkorswim_installer.sh
```



#### Following the installation prompts

On the screen that says "Selection Installation Options," select "Install only for the current user."

On the screen that says "Select integration Options," ***make sure that "Create Desktop Icon" is checked***.

### Ensure there are no conflicts with dependencies.

The installation process should lead to the creation of a new folder in your home dirrectory titled `thinkorswim`. Navigate to this folder, and edit a file in titled `thinkorswim`. I know this is confusing, but there is both a folder and a file titled `thinkorswim`; essentially, you need to edit `~/thinkorswim/thinkorswim`.

Add a new line below the first line, and paste in the following:

```
export PATH=/usr/lib/jvm/java-8-openjdk-amd64/jre/bin/:$PATH
```

### Add thinkorswim to the application menu

Durring the installation process, a file should be created in your Desktop folder titled `thinkorswim.desktop`. This file will need to be moved into the directory `~/.local/share/applications/`. This can be easily accomplished by opening Terminal and typing the following command:
```
mv ~/Desktop/thinkorswim.desktop ~/.local/share/applications/
```
