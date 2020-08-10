# Mongodb
* This tutorial is written specifically for OSX.
* Follow this tutorial to learn how to set up a Mongodb server on port 27017.

# Commands used in this Tutorial
* mongod: starts the mongodb server
* mongo: Launch the mongo terminal environment (mongod needs to be running in a separate terminal window for this command to work)
* [chmod](https://linux.die.net/man/1/chmod) : change file permissions. chmod 777 "file_name" gives read, write, execution permissions to all users of the file in question.
* [chown](https://linux.die.net/man/1/chown) : change file ownership.
* [cd](http://linuxcommand.org/lc3_man_pages/cdh.html) : change working terminal directory.
* [mkdir](https://linux.die.net/man/1/mkdir) : make a directory. If no path specified, makes the directory in the current working directory

# Install & set up Mongodb
* Install brew if you haven’t. The command is:  '''/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
* Create a directory in your place of choice to install mongodb. Since we are using Mac OSX we cannot install it at the root directory which it usually does at default. For example, create a directory at the base of your user directory called data. Then create a directory inside data called db.
* In a terminal issue the command: cd /Users/"first.last@plex-llc.com"/data/db
* Install mongodb using brew: brew tap mongodb/brew
* Once installed run the command: mongod --dbpath /Users/"first.last@plex-llc.com"/data/db
* Lastly, you may need to change the owner of the ‘mongod.lock’. If you get an error message saying permission denied, note the name of the file and issue the chown command to change the owner of the file to yourself instead of root. If an error message still persists, use the chmod 777 command on the file in question.

# Start the Tutorial
* Once set up, the tutorial at [quackit](https://www.quackit.com/mongodb/tutorial/mongodb_installation.cfm) covers the ins and outs of mongodb fairly well. 
* When you get to the mongoimport and export sections of the tutorial, create a database in your location of choice. This database will hold the .json files created via the mongoexport command you run in the tutorial. Remember to specify the path of the custom database you created to hold the files. /Users/"first.last@plex-llc.com"/"database_name"
