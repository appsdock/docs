# Server Backup

## Strategy

The backup strategy is quite simple. A daily backup is created and downloaded by the [Backup Tool](https://github.com/bloodhunterd/backup-tool). The backup files are stored on a NAS to get further backed up by the proprietary backup solution of the NAS.

### Description

The [Backup Tool](https://github.com/bloodhunterd/backup-tool) is will be executed in agent mode by a cron job on the server. The tool itself is stored at **/srv** together with the configuration file, which contains the directories and databases to backup. The docker version of the [Backup Tool](https://github.com/bloodhunterd/backup-tool-docker) runs in server mode at the NAS and connects to the server to download the packages. The connection is encrypted by [SSH](https://wiki.ubuntuusers.de/SSH/) and secured by public/private key. The backup user is restricted to the backup directory.

The tool creates packages of the directories and databases compressed by [bzip2](https://www.sourceware.org/bzip2/). The packages are stored in **/backup**. The previously created packages will be replaced (*overwritten*).

After the packages are created on the server the [Backup Tool](https://github.com/bloodhunterd/backup-tool-docker) at the NAS connects to the server and downloads the packages to a local directory. After that the backup report is created and send to the configured receivers.

The NAS backup solution provides restoring a daily version for the last 4 weeks and a weekly version for the last year.

### Timings

* **02:00** Packages are created at the server.
* **03:00** Packages are downloaded by the NAS from the server.
* **04:00** Packages are backed up by the NAS backup solution.
