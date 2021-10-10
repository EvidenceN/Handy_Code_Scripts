# CHMOD

Let's say you are the owner of a file named myfile, and you want to set its permissions so that:

<ol>
  <li>the user can read, write, and execute it;</li>
  <li>members of your group can read and execute it; and </li>
  <li>others may only read it.</li>  
</ol>

This command will do the trick:

`chmod u=rwx,g=rx,o=r myfile`

This example uses symbolic permissions notation. The letters u, g, and o stand for **"user", "group", and "other"**. 
The equals sign ("=") means "set the permissions exactly like this," and the letters **"r", "w", and "x"** stand for "read", "write", and "execute", respectively. 
The commas separate the different classes of permissions, and there are no spaces between them.

**Here is the equivalent command using octal permissions notation:**

`chmod 754 myfile`

Here the digits 7, 5, and 4 each individually represent the permissions for the user, group, and others, in that order. 
Each digit is a combination of the numbers 4, 2, 1, and 0:

 <ul>
  <li> 4 stands for "read",</li>
  <li>2 stands for "write",</li>
  <li>1 stands for "execute", and</li>
  <li>0 stands for "no permission."</li>
</ul>

So 7 is the combination of permissions 4+2+1 (read, write, and execute), 5 is 4+0+1 (read, no write, and execute), 
and 4 is 4+0+0 (read, no write, and no execute).

<a href = https://www.computerhope.com/unix/uchmod.htm target="_blank">More CHMOD commands can be found here</a>

# CHOWN

Change Owner of a file and Change Group Owner. Also, how to change the owner and group of every file in the directory. 

<a href = https://linuxize.com/post/linux-chown-command target="_blank">CHOWN Blog Post Instructions </a>

<a href = https://www.cyberciti.biz/faq/how-to-use-chmod-and-chown-command/Another target="_blank"> Another blog that goes into more depth about chmod and chown. What file symbols like "drwx-rw--" means</a>
