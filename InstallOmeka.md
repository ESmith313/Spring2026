# Install Omeka Assignment

## Overview
 - Installing Omeka Classic and then adding a link to it on my Wordpress site helped me understand how different web tools actually work together. Since everything was running on my Google Cloud VM I had to pay attention to things like file paths, URLs, and server settings, and permissions.

## Problems
 - The main problem I ran into was with Apache mod_rewrite. Even though the VM showed it was enabled, Omeka kept giving me an error saying it wasn’t. This was frustrating and confusing at first.

## Solution
 - I eventually figured out that it also needed to be allowed in the Apache configuration by setting the correct directory permissions (‘AllowOverride All’). Once I updated the configuration and restarted Apache the issue was resolved.

## Reflection
 - This experience improved my understanding of server management and debugging. It also showed how Omeka can be used in real world digital library settings to organize and present collections.

## Links
 - Omeka: http://34.9.67.253/omeka/
 - WordPress: http://34.9.67.253/wordpress/index.php/lis-624/ 

