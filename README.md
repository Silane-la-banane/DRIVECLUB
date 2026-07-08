# DRIVECLUB

This repo allows you do unlock DLCs and online cars.

Tutorial: LINK

## How does it work?
The AFR plugin allows you to replace game files directly on a game without creating a fake update package. So on this README, you will see how to install the AFR plugins and put the new required files on your console.

## Prerequisite

To continue, you **must** have :

- A jailbroken console
- GoldHen ready
- DRIVECLUB installed


<p align="center" width=100%>
  <img src="https://raw.githubusercontent.com/Silane-la-banane/DRIVECLUB/refs/heads/main/github_images/fleche.gif" alt="Sublime's custom image" width=50% />
  </p>

# NO, YOU CAN'T DO IT WITHOUT A JAILBREAK

<p align="center" width=100%>
  <img src="https://raw.githubusercontent.com/Silane-la-banane/DRIVECLUB/refs/heads/main/github_images/fleche_inversee.gif" alt="Sublime's custom image" width=50% />
  </p>

## Step 1: FTP connection
For simpler handling, we will use FTP, which allows us to modify PS4 files from a computer.
I am using WinSCP for this tutorial.

[WinSCP for Windows](https://winscp.net/eng/download.php)
[FileZilla for Linux users and old macs](https://filezilla-project.org/)

Be sure to have the FTP server enabled by checking on the GoldHen menu -> Servers Settings-> Enable FTP Server

When connecting to your console, fill the infos :

- Protocol : FTP
- Encryption: No encryption
- IP : Check on your console pop-up
	- If the pop-up disappears, uncheck and re-check the FTP box
- Port : 2121 by default, check on the console pop-up
- Name : Anything you want
- Password : Leave blank

![GoldHen Server](https://raw.githubusercontent.com/Silane-la-banane/DRIVECLUB/refs/heads/main/github_images/GoldHen_serveur.png)

![FTP connection](https://raw.githubusercontent.com/Silane-la-banane/DRIVECLUB/refs/heads/main/github_images/FTP_connection.png)

## Step 2: Installing the new files

In the /data/GoldHEN/ folder, put the plugin.ini file and the plugins folder. If you already have some plugins enabled for other games, open both plugin.ini files and copy/paste my content. It begin with ; DRIVECLUB BEGIN and end with ; DRIVECLUB END

On /data/GoldHEN/, create /AFR/[TITLE_ID], in my case the path is /data/GoldHEN/AFR/CUSA00093/.

Once created, unzip the file Driveclub Mega Fix and put its content inside.

You should have 3 folders (data, liveryeditor and newdata) in /data/GoldHEN/AFR/CUSA00093/

![FTP GIF](https://raw.githubusercontent.com/Silane-la-banane/DRIVECLUB/refs/heads/main/github_images/FTP_connection.gif)

## Step 3: Launch and try

Be sure to have the plugins activated by checking on the GoldHen menu -> Plugin Settings-> Enable Plugins Loader

Now if you go into your garage, you should see all 114 cars.
To easily check, sort by manufacturers, and search for bikes. If there is still the Playstation Store logo, it means you failed somewhere.

![DC_ingame](https://raw.githubusercontent.com/Silane-la-banane/DRIVECLUB/refs/heads/main/github_images/DC_ingame.gif)

In this case, delete everything you did in this tutorial, and try again.