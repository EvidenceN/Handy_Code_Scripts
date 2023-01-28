Start SSH Agent

* Run powershell as administrator

Then enter this command

`Get-Service ssh-agent | Set-Service -StartupType Manual`
