Start SSH Agent

* Run powershell as administrator

Then enter this command

`Get-Service ssh-agent | Set-Service -StartupType Manual`


To setup SSH on Windows Powershell for github, follow these instructions.

(Steps 2 to 5 might need to be done as admin)

1. Generate SSH key by typing `ssh-keygen -t ed25519 -C "your_email"`
2. Start your SSH client server by typing `Start-Service sshd`
3. To check the status of your SSH-AGENT and make sure it's installed, type  `Get-Service ssh-agent` The status will either say running or stopped. 
4. If it says stopped, you need to start it by typing `Start-Service ssh-agent`
5. You can set your SSH-AGENT and SSH-CLIENT Server to start automatically by typing these 2 commands. To automatically startup SSH-CLIENT Server `Set-Service -Name sshd -StartupType ‘Automatic’` and to automatically start SSH-AGENT type `Get-Service ssh-agent | Set-Service -StartupType Manual`
    a. If running both or either of the commands above returns error, you can set it up to start automatically using the GUI. First, type in "Services" in windows search box. Second, look for "OpenSSH (Server and Agent)" Click on both of them and change the startup type to automatic. 
6. Add the private SSH key to windows powershell by typing (from the home (~) directory) `ssh-add .ssh/private_key_file_name`
