# odctl
OneDrive Client Wrapper Script

# Initial Configuration:

Follow the instructions in the `README-onedrive-sharepoint`/`README-onedrive-sharepoint.md` file to configure the initial sync profile.

# Usage:
Enable/disable the Systemd service that monitors and syncs the sync profile.

`odctl enable` / `odctl disable `

Start/stop the Systemd service that monitors and syncs the sync profile.

`odctl start` / `odctl stop ` / `odctl restart`

Display the status of the Systemd service that monitors the sync profile.

`odctl status`

Kick off a resync of the sync profile. (Must be done after editing the `config` file or the `sync_list` file).

`odctl resync`

Kick off a manual sync of the sync profile. (The Systemd service must not be running).

`odctl manualsync`

Display the log file for the sync profile.

`odctl showlog [<number_of_lines>|follow]`

Display the sync list (i.e. specific directories/files being synced) for the sync profile.

`odctl synclist`

Add a file/directory to the sync list for the sync profile. (A resync must be done after modifying the sync_list file).

`odctl addsync <subdir_or_file>`

Add a file/directory to the sync list for the sync profile. (A resync must be done after modifying the sync_list file).

`odctl rmsync <subdir_or_file>`
