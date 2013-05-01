bashsctipts
===========

Some useful bash scripts

makevhost
---------
Tool for creating an apache vhosts. Useful with Debian/Ubuntu apache dist (with sites-available/enabled directories). This tool uses a little bit of sudo, so be careful. See the script before use. You can change #directories section or apache username if you have non standard configuration.

Usage:
`makevhost VHOSTDIRECTORY [gitrepository]`

Example:
`makevhost com.test.dev git@github.com:someuser/somerepo`

Will:
* Create directories for vhost in /var/www/vhosts/com.test.dev
* Clone someuser's somerepo into [...]/com.test.dev/httpdocs
* Fix permissions (chown yourusername:apacheusername [...]/httpdocs)
* Create vhost file in [...]/sites-available
* Enable vhost with a2ensite
* Append 127.0.0.1 server.name to /etc/hosts
* Reload apache configuration

