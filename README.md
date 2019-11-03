# automysqlcheck

This is a small bash script that checks all mysql databases for errors and mails a log file to a specified email address.

## USAGE

1) Use the following environment variables to override default configuration values:

    * `OPTIONS_FILE` - The path to a MySQL options file containing auth credentials (default : `~/.my.cnf`; see [Using Options Files](https://dev.mysql.com/doc/refman/8.0/en/option-files.html))
    * `DBHOST` - The MySQL server hostname (default: `localhost`)
    * `LOGFILE` - The path where you'd like to save the `automysqlcheck` log file (default: /var/log/automysqlcheck.log`)
    * `MAILTO` - The email address to send the summary to upon completion (default: `root@localhost`)
    * `DBNAMES` - A space delimited list of database names to check (or `all`; default: `all`)
    * `DBEXCLUDE` - A space delimited list of database names to skip (default: none)

2) Create a MySQL options file at the path specified above which contains auth credentials, for example:

        [mysql]
        user=root
        password=SECRET_PASSWORD

3) Add `automysqlcheck` to your crontab or install the macOS launchd .plist file, specifying environment variables to override any necessary configuration values.

## LICENSE

This was originally published on http://dev.mysql.com/doc/refman/5.0/en/check-table.html#c5003 by Stuart Bray and modified by the community.

Copyright (c) 2004 Stuart Bray  
Copyright (c) 2005 eyechart  
Copyright (c) 2006 Mickael Sundberg  
Copyright (c) 2006 Jake Carr  
Copyright (c) 2010 Fabrizio La Rosa  
Copyright (c) 2011 Morgan Aldridge  
