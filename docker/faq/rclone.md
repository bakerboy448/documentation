# **Rclone Docker FAQ**

**Q1.** I am seeing the following message in ```/config/supervisord.log```, what does it mean and how can i fix it?:-

```[warn] RCLONE_CONFIG_PATH '<path defined by user>' does not exist, please run 'rclone config --config /config/rclone/config/config.conf' from within the container```

**A1.** The message above means that you have not run through the initial configuration wizard built into Rclone. This has to be done through the CLI and may require a Web Browser to authenticate (depends on Cloud Provider selected).

To run the Rclone wizard open unRAID Web UI and go to Docker tab, then left click the Rclone icon and select 'Console'. Once at the console of the container please issue the following command to start the Rclone wizard:-

```rclone config --config /config/rclone/config/config.conf```

Depending on the Cloud provider you want to use you will now follow different procedures, a few of the popular ones are linked below:-

OneDrive		https://rclone.org/onedrive/<br>
Google Drive	https://rclone.org/drive/<br>
Amazon Drive	https://rclone.org/amazonclouddrive/<br>

*Note* Certain Cloud Providers will require a Web Browser to be present to be able to complete the Rclone configuration, there is an alternative to this via the Rclone auth configuration option - see here:- https://rclone.org/remote_setup/