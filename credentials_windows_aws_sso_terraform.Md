After logging into AWS, the credentials files is created but it is not transported into the .aws current directory. 

Here is the error and code to fix it. 

Error -  `mv: cannot open '/tmp/tmp.uxoK21tS5P/credentials' for reading: Permission denied`


To fix error, 

`sudo mv /tmp/tmp.uxoK21tS5P/credentials .`

`sudo chmod 644 credentials`

`sudo chown evidence credentials to change owner`

`chgrp evidence credentials`
