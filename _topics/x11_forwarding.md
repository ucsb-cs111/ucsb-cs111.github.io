---
topic: "X11 Forwarding"
desc: "X11 Forwarding from CSIL workstations to run graphics programs over ssh"
---

<!-- saved from url=(0076)http://www.cs.ucsb.edu/~gilbert/cs111/old/cs111Fall2010/remoteX_content.html -->

## What is X Forwarding and why do we care?

The X Window System (commonly X or X11) is a computer software system
and network protocol that provides a graphical user interface (GUI)
for networked computers. This means that you can run graphic
applications remotely (and not only command line programs).

To achieve X Forwarding from the CSIL (Computer Science Instructional
Lab) workstations you must own a CS account, an ssh client and an X
Server program to handle the local display. In operating systems like
Linux Ubuntu and Mac OS X this can be done with the default OS
installation. :-)


## Unix Based Systems


So, if you own a Unix Based System like Linux or Mac OS X all you have
to do is connect to the remote workstation using the ssh command,
adding the `-X` (uppercase x) flag. This tells to the remote
workstation to forward any graphic output to your computer.

The command must be like this:



```
ssh -X username@hostname.cs.ucsb.edu
```


where `<username>` is your CS username and `<hostname>` should be one of the
`csil-01` through `csil-48` boxes.


Now you can run any application you want by giving the application's name in the command line (e.g. `matlab`, `firefox`). The 
output will be directed in your monitor!


# Windows Systems

TODO: Consider replacing PuTTY plus XMing instructions with MobaXTerm,
which is a much easier replacement.

See: <https://mobaxterm.mobatek.net/>



If you own a Windows Operating System the most effective solution for you is to change OS. If by any chance you want something 
more complicate though, there is still a way:



Download the PuTTY ssh client from here: <a href="http://www.chiark.greenend.org.uk/~sgtatham/putty">www.chiark.greenend.org.uk/~sgtatham/putty</a>



Download an X Server: <a href="http://www.starnet.com/products/xwin32">www.starnet.com/products/xwin32</a>



Configure XWin-32 (you must do this only once):



<ol>
	<li>Run XWin-32</li>
	<li>Choose the "Security" tab and click "Add..."</li>
	<li>Enter "localhost" and click "OK"</li>
	<li>Quit XWin-32</li>
</ol>






Connect:



<ol>
	<li>Run XWin-32</li>
	<li>Run PuTTY</li>
	<li>In PuTTY, go to "Tunnels" from "Category" list and check the "Enable X11 Forwarding" option</li>
	<li>Go back to "Session". To connect to the CSIL workstations you will have to type in the Host Name field something like 
this:

	<code>hostname.cs.ucsb.edu</code>

	where &lt;username&gt; is your CS username and &lt;hostname&gt; can either be "csil" or any specific workstation name 
(e.g. "megatron", 
"homer", "calvin" etc). Then click "Open" (your password will be asked).
	</li>
</ol>






Note: You can always add the X11 Forwarding option in a saved session.


Now you can run any application you want by giving the application's name in the command line (e.g. "matlab", "firefox"). The
output will be directed in your monitor!






<i>Disclaimer: The above method for Windows is not tested by the author. In case you have any problem or there are changes in 
newer versions of the programs used (PuTTY and XWin-32) please <a href="http://www.cs.ucsb.edu/~gilbert/cs111/old/cs111Fall2010/contact.php">contact me</a>.</i>





In any case, [Google](http://www.google.com/webhp?q=X+forwarding)Google is always your
friend.


