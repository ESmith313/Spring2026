#Install Omeka Assignment

Installing Omeka Classic and then adding a link to it on my Wordpress site helped me understand how different web tools actually work together. Since everything was running on my Google Cloud VM I had to pay attention to things like file paths, URLs, and server settings. The main problem I ran into was with Apache mod_rewrite. Even though the VM showed it was enabled, Omeka kept giving me an error saying it wasn’t. This was frustrating and confusing at first. I eventually figured out that it also needed to be allowed in the Apache configuration, not just turned on. Once I fixed that everything started working the way it should. The problem of my VM losing connection has also been resolved which is a relief.

*Omeka:* http://34.9.67.253/omeka/ 
*WordPress:* http://34.9.67.253/wordpress/index.php/lis-624/
