# automysqlcheck

This is a small bash script that checks all mysql databases for errors and mails a log file to a specified email address.

## USAGE

1) Modify `automysqlcheck` script to specify the following configuration values:

    * `OPTIONS_FILE` - The path to a MySQL options file containing auth credentials (see [Using Options Files](https://dev.mysql.com/doc/refman/8.0/en/option-files.html))
    * `dbhost` - The MySQL server hostname (or `localhost`)
    * `logfile` - The path where you'd like to save the `automysqlcheck` log file
    * `mailto` - The email address to send the summary to upon completion
    * `dbnames` - A space delimited list of database names to check (or `all`)
    * `dbexclude` - A space delimited list of database names to skip

2) Create a MySQL options file at the path specified above which contains auth credentials, for example:

        [mysql]
        user=root
        password=SECRET_PASSWORD

3) Add `automysqlcheck` to your crontab or update & install the macOS launchd .plist file

## LICENSE

This was originally published on http://dev.mysql.com/doc/refman/5.0/en/check-table.html#c5003 by Stuart Bray and modified by the community.

Copyright (c) 2004 Stuart Bray  
Copyright (c) 2005 eyechart  
Copyright (c) 2006 Mickael Sundberg  
Copyright (c) 2006 Jake Carr  
Copyright (c) 2010 Fabrizio La Rosa  
Copyright (c) 2011 Morgan Aldridge  
