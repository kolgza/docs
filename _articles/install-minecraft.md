---
layout: article
title: Install and Optimize Minecraft!
description: 
  So you want some of that blocky goodness? Well, get Java and some graphics cards and let's go!
keywords:
  - Minecraft
  - Mojang
  - Games
hidden: false
section: community

---

Alright! Hitch on and let's go on!

### Pop!_OS 20.04 and later

First, open the Pop!_Shop. Next, in the search box, type Minecraft, and click "Minecraft" in the search results. Finally, click "Install".

Now you have installed Minecraft! Open the application and log in with your username and password to start playing!

### Debian and Ubuntu
  
First, you will need Java runtime.  
  
```bash
sudo apt-get install openjdk-8-jre
```

So, you want oracle runtime instead? But.... fine....  
Get the repository and install the package.  

```bash
sudo apt-add-repository ppa:webupd8team/java
sudo apt-get update
sudo apt-get install oracle-java8-installer
```

You will then download the launcher. Go to the [minecraft.net](https://minecraft.net/en-us/download/) page to download or...

```bash
wget http://s3.amazonaws.com/Minecraft.Download/launcher/Minecraft.jar
```

Now run the file! Log in with your username and password and start playing!

---

This article was contributed by [kylerschin](https://github.com/kylerschin).
