# Apache 2
## PHP
### File upload limit
By default the size of files that are uploaded to an Apache2 server is limited. To change this limit edit your `php.ini` usually located in `/etc/php/7.3/apache2/php.ini` where `7.3` can be an other version number. Locate the option `upload_max_filesize` and set it to any amount you wish. Amounts kann be any integer followed by any of the letters `K`,`M`,`G` or `T` which stand for Kilo-, Mega-, Giga- and Terrabytes. (Though i doubt anyone will ever upload a file of a Terrabyte in size)

> Important: 
> PHP also defines a `post_max_size`! Files uploaded via POST are limited by the lower number set at `post_max_size` AND `upload_max_filesize`! Remember to change both in case you want to use POST for uploading files!