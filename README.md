# BackUpBashScriptrepo

This Bash script performs a backup operation for the contents of the user's Desktop directory. Here's what each part of the script does:

1. `#!/bin/bash`: This line is called a shebang and indicates that the script should be executed using the Bash shell.

2. `DATE=$(date +%m-%d-%Y-%M)`: This line uses the `date` command to obtain the current date and time. The `+%m-%d-%Y-%M` format string specifies that the date should be formatted as month-day-year-minute. This formatted date and time are then assigned to the variable `DATE`.

3. `BACKUP_DIR="$HOME/backups"`: This line sets the `BACKUP_DIR` variable to the path where the backups will be stored. The `$HOME` environment variable points to the user's home directory, and the script will create a subdirectory named "backups" within it.

4. `tar -cvzf $BACKUP_DIR/backup-$DATE.tar.gz $HOME/Desktop`: This line creates a compressed archive (tarball) of the contents of the user's Desktop directory. Here's what each flag does:
   - `-c`: Create a new archive.
   - `-v`: Verbosely list the files being archived.
   - `-z`: Compress the archive using gzip.
   - `-f`: Specify the name of the archive file.

   The source directory for the backup is `$HOME/Desktop` (the user's Desktop directory), and the destination path for the backup archive is `$BACKUP_DIR/backup-$DATE.tar.gz`. This means that the backup will be stored in the previously defined backup directory with a filename that includes the formatted date and time.

In summary, this script creates a backup of the user's Desktop directory, compresses it into a tarball, and saves it in a specified backup directory with a filename containing the current date and time.
