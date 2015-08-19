# countfiles
A simple way to summarize file usage in a given directory. I wrote this a long long time ago and was recently asked for the source. The script is still in production today in an linux environment with quota'd NFS-mounted home directories.

## NAME
    count_files.pl - A tool for summarizing inode usage within a directory

## SYNOPSIS
        count_files.pl 
         - summarizes the current directory

        -- or --

        count_files.pl <<directory_to_search>>
        - summarizes the given directory

        -- or --

        count_files.pl --help
        count_files.pl --man
        - prints out help and man pages

## DESCRIPTION
    This script provides a simple way to summarize file usage for a given
    directory. Why is this important? Well, you probably got here because
    you are over your "files" quota and need help in clearing out
    unused/uneeded files. While there are good tools for determine disk
    space usage there were not (until now) any for determining file usage.

    Run this tool from within your home directory to get a listing of your
    10 directories with the most files. You can then tar or delete
    unused/uneeded files and directories until you are under quota. As
    always be careful when deleting files from your directory.

## COMMAND LINE OPTIONS
    -h, --help
        Display a program usage screen and exit.

    -m, --man
        Displays this page.

## EXAMPLES
        count_files.pl 
        - gives an file summary for the current working directory

        count_files.pl public_html 
        - gives an file summary for the public_html directory

## REQUIREMENTS
        [core]
        File::Find: The meat and potatoes of this script
        Getopt::Long: Handles argument parsing
        Pod::Usage: Prints out this great message

## TODO
        1) ignore requests for additional features
        2) drink beer
