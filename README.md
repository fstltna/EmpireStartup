# Empire Server Startup Scripts (1.0.0)
Startup scripts for the Empire game server - uses the "screen" command to manage session. This also restarts the Empire server process if it crashes.

Official support sites: [Official Github Repo](https://github.com/fstltna/EmpireStartup) - [Official Forum](https://empiredirectory.net/index.php/forum/startup-scripts)

---
These start up the Empire server at boot time with a "screen" process.

1. Copy **empire** into **/etc/init.d** - make sure it is executable
2. Copy **startempire** into **/root/empire** - make sure it is executable
4. Run "**systemctl enable empire**" (only needed once, will stick)
5. Run "**systemctl start empire**" - starts Empire without restarting the server

When you want to view the Empire console, just enter "**screen -r**" in your shell.

To disconnect from the Empire console just press **CTRL-A CTRL-D**. This will leave it running and you can reconnect to it again.

I have only tested this on a Ubuntu 16.04 server...

If you want to turn off the server respawning type "**touch /root/empire/nostart**". To reenable it type "**rm /root/empire/nostart**".

---
Note: If you don't already have the "screen" tool installed you will need to install it by "**sudo apt-get install screen**".
