# odctl
OneDrive Client Wrapper Script

# Initial Configuration:

Follow the instructions in the `README-onedrive-sharepoint`/`README-onedrive-sharepoint.md` file to configure the initial sync profile.

# Usage:

**IMPORTANT:** 

The first time the `odctl` command is run a new config file will be created (`~/.config/odctl.cfg`). Before running the `odctl` command again this file must be updated by editing the ONEDRIVE_CONFIG variable to match the name of the sync profile and ONEDRIVE_CONFIG_DIR variable to match the path to the sync profile's config directory that were configured when following the instructions in the README-onedrive-sharepoint file.

## Options

Enable/disable the Systemd service that monitors and syncs the sync profile.

`odctl enable` / `odctl disable `

Start/stop the Systemd service that monitors and syncs the sync profile.

`odctl start` / `odctl stop ` / `odctl restart`

Display the status of the Systemd service that monitors the sync profile.

`odctl reauth` 

Reauthorize (log out then log back in) the onedrive client with OneDrive/SharePoint. This will refresh the authentication token if it has gone stale. You will need to follow the instructions that are displayed in the terminal to use the provided URL in a web browser to log in and then copy/paste the resulting URL from the browser back to the command line.

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
