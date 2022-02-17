---
sidebar_position: 15
---

# Changelog
### v2.0.10
:::info
If the startup fails after the update, the error `create temp dir error: mkdir : no such file or directory` is reported, and the value of `temp_dir` in the configuration file can be changed from empty to `data/temp`. which is:
````json
{
  "address": "0.0.0.0",
  "port": 5244,
  "assets": "",
  "database": {
    "type": "sqlite3",
    "user": "",
    "password": "",
    "host": "",
    "port": 0,
    "name": "",
    "table_prefix": "x_",
    "db_file": "data/data.db",
    "ssl_mode": "disable"
  },
  "scheme": {
    "https": false,
    "cert_file": "",
    "key_file": ""
  },
  "cache": {
    "expiration": 60,
    "cleanup_interval": 120
  },
  "temp_dir": "data/temp" <--- here
}
````
:::
- Music playlist sorting and scrolling [#529](https://github.com/Xhofe/alist/discussions/529)
- Frontend supports hiding files via regular expressions [#464](https://github.com/Xhofe/alist/discussions/464)
- Music playback remember volume [#549](https://github.com/Xhofe/alist/issues/549)
- IPA file installation
- Fixed some loading issues
- Fixed the problem that the video list cannot be scrolled beyond the screen
- Account load balancing
- Fix the problem that the temporary directory is not created at the first startup
- Favicon redirect [#512](https://github.com/Xhofe/alist/issues/512)
- Added default data when adding an account
- Fix webdav visitor's hidden account [#522](https://github.com/Xhofe/alist/issues/522)
- Fixed Baidu token leak problem
- Fix the issue that the upload file of Tianyi Cloud Disk contains special compliance [#527](https://github.com/Xhofe/alist/issues/527)
- Support WebDav direct proxy to support clients that do not support 302 follower
- Set timeout for api request [#535](https://github.com/Xhofe/alist/issues/535)
- Custom temporary directory [#519](https://github.com/Xhofe/alist/issues/519)
- Support empty password (to prevent login after changing to empty)
- Quark network disk support (transfer only)
- s3 add S3ForcePathStyle option [#551](https://github.com/Xhofe/alist/issues/551)
- Fix and Caiyun can't delete directory
  
### v2.0.9
- GBK encoding support for text files [#469](https://github.com/Xhofe/alist/discussions/469)
- Cancel to get whether to log in when the management password is empty
- Fix FTP disconnects after a long time of inactivity [#462](https://github.com/Xhofe/alist/issues/462)
- S3 object storage custom acceleration domain name [#362](https://github.com/Xhofe/alist/discussions/362)
- Yandex.Disk storage support [#443](https://github.com/Xhofe/alist/discussions/443)
- Fixed the download problem of Lansuo Cloud (adapted to the changes of the blue-sound cloud download page)
- Baidu network disk storage support
- The issue of uploading empty files in webdav under Windows [#376](https://github.com/Xhofe/alist/issues/376)
- Random initial admin password [#467](https://github.com/Xhofe/alist/discussions/467)
- Modify the default logo
  
### v2.0.8
:::caution
There is a problem with the cdn of zhimg, please switch to jsdelivr or local, see [assets](./setting/config.md)
:::
> #### v2.0.8
> - fix webdav
> - fix ftp conn not store

- Add copy on web page
- Fix folder icon issue
- Added loading for some operations
- Fix Tianyi cloud disk sorting problem (using local sorting) [#407](https://github.com/Xhofe/alist/issues/407)
- Teambition upload
- Added OCR to identify Tianyi cloud disk verification code
- Fixed a security vulnerability in local storage, please update if using local storage
- Use tempFile instead of TeeReader when partially storing uploaded files, reducing memory usage and avoiding OOM
- Fix 123 cloud disk upload bug [#449](https://github.com/Xhofe/alist/issues/449)
- Tianyi cloud disk chunk upload [#358](https://github.com/Xhofe/alist/issues/358)
- Removed Text function that could cause OOM

### v2.0.7
- Fix bugs that users do not exist in operations such as uploading to Caiyun [#365](https://github.com/Xhofe/alist/issues/365) [#373](https://github.com/Xhofe/alist/ issues/373)
- Fix the memory leak when using the local proxy to transfer
- Fix GoogleDrive cannot load text files such as Readme.md [#379](https://github.com/Xhofe/alist/issues/379)
- Adapt to different domain names of Lansuo Cloud
- Hide s3 placeholder empty files
- Prevent MediaTrack from creating a new folder with the same name
- Supports all storage to extract folders to the front
- New folder, rename and move on the web side
- Added sslmode configuration for postgres
- Fixed that files cannot be obtained when webdav is encrypted
- Added prebuilt of musl-libc
- Fixed the movement of 123 cloud disks
- Fix the mismatch caused by the path change when the file is not loaded
- Display upload speed and remaining time
- Fixed that the administrator login cannot be previewed when the password is empty

### v2.0.6
- Fix some typos [#348](https://github.com/Xhofe/alist/discussions/348)
- Fix the bug that the user of Caiyun does not exist [#338](https://github.com/Xhofe/alist/issues/338)
- Changed the Spinner of the homepage
- Added account copy and paste
- Remove the error message when the password is empty
- Added cdn of unpkg.zhimg.com
-Fixed that WebDAV cannot create new folders for minute and second frames [#351](https://github.com/Xhofe/alist/discussions/351)
- Unhide files for logged in users [#343](https://github.com/Xhofe/alist/discussions/343)
- Fixed the problem that FTP cannot be downloaded
- Disable root deletion
- Fix the problem that GoogleDrive local proxy video cannot be jumped to play [#334](https://github.com/Xhofe/alist/discussions/334)

### v2.0.5

- Fixed the judgment of using token or password when copying the straight chain
- Solve the empty div brought by react-viewer
- Added pagination support (optional load all, load more, autoload more, pagination) [#257](https://github.com/Xhofe/alist/discussions/257)
- Subtitles added responsive
- Fixed the problem that the name of the path navigation bar is invalid when the name is repeated
- epub, flv preview support
- Add delete confirmation
- Fixed specified cache cleanup when file modification occurs
- Added 123 disks and Tianyi cloud disk upload
- New drivers: Teambition, Mediatrack and 139Yun
- Update config file when modifying config file structure
- Fixed bug when proxying local files with other servers
- Fix the get empty page that appears when saving Tianyi cloud disk repeatedly
- Upload and delete multiple files on the web
- Remove custom header and body content managed in the background

### v2.0.4

> #### v2.0.4-fix2
> - Markdown image display problem
> - Fix the error of alist storage
> - The background color of the uploaded component when it is dark
> - Customize Home emoji
> - Fixed getting wrong content-type when uploading web
> #### v2.0.4-fix
> - Fix the interpretation error of whether it can be uploaded

- Added wav audio preview
- Support hide account
- Remove the `.` and `..` directories returned by FTP storage
- Add WebDAV guest account
- Set the grouping
- Support onedrive, GoogleDrive, PikPak WebDAV writing
- Added lightning disk storage support [#234](https://github.com/Xhofe/alist/discussions/234)
- Use local sorting for storage that does not support sorting
- GoogleDrive storage increase preview image
- S3 storage protocol support [#211](https://github.com/Xhofe/alist/discussions/211)
- Custom cache time
- WebDAV storage support
- Support artplayer on mobile
- Video list playback (can be switched automatically)
- File packaging zip download
- Add right-click menu, support multiple selection
- Replace markdown components to solve some preview issues [#185](https://github.com/Xhofe/alist/issues/185)
- Use the preview image of react-viewer navigation bar [#212](https://github.com/Xhofe/alist/issues/212)
- Optimize path component style
- Support web page upload files (you can set the directory to allow visitors to upload,and please be aware: all uploads go to the server)

### v2.0.3
- Modify pdf preview to pdfjs
- For music covers with preview images, display as preview images
- Video subtitle support (automatically search the first one in the same directory as the name of the video file name and the extension is `srt, vtt, ass`)
- Modified the code of the internationalization part
- Fix the bug in the FTP download part
- Support API proxy (for PikPak and GoogleDrive)
- Solve the 403 problem caused by the IP limit of the 123Pan
- Modified the default custom style
- Fixed the endless loop caused by PikPak refresh token
- Added the option of using local front-end js files
- Modify the default icon color
- Modified the agent field, the original agent will be invalid

### v2.0.2
:::caution
Modified the onedrive type field, you need to reselect the onedrive type in the background.
There are bugs in this version of PikPak, please update.
:::
- Fix the issue of thumbnails being cropped during multi-image preview [#212](https://github.com/Xhofe/alist/issues/212)
- Fixed an abnormal request after clicking on the browse image to return directly to the previous layer [#212](https://github.com/Xhofe/alist/issues/212)
- Fix the problem that the visitor password cannot be used to view files after logging in to the background with the wrong password
- Fix the problem that the password is not added when requesting the preview interface
- Fix the issue that the Aliist storage policy and folder do not take effect
- Fix the problem that the proxy signatures of cloudflare workers do not match
- Support local file proxy
- Partial WebDAV writing support for Tianyi Cloud Disk and 123 Cloud Disk
- Fix the problem that the refresh_token obtained by onedrive is empty (not tested)
- New storage: FTP
- New storage: PikPak

### v2.0.1
:::caution
The previous custom styles and custom scripts will be invalid, but they will still be visible in the background settings, which can be reset in the custom header and custom body.
:::
- The straight chain password is added to the file name to add salt
- Optimize the code structure of the direct chain encryption part
- Fix the problem that overlay components are covered by markdown components
- Remove the previous custom styles and custom scripts, and change to custom heads and custom bodies
- Remove the 100% height limit on the homepage
- Modify the build target of vite to es2015 to improve browser compatibility
- Add salt to the background password
- The file list no longer requires a password after logging in to the background
- Fix the encoding problem when the file name contains% (try not to include %, it will report an error when refreshing)
- Allow deletion of outdated settings
- WebDAV: New Local storage/Aliyundrive supports uploading, moving, creating folders, and deleting
- Support adding Aliist abstract as a driver
- Support using cloudflare worker to transfer download files
- Fix that the local file named `index.html` cannot be previewed
- Support `webm` suffix video preview
- Optimized the code structure and abstracted multiple methods
- Modify the proxy settings of the account, all traffic will go to the server after opening

### v2.0.0
- Repair the check parent folder password failure on Windows
- Optimize code structure
- Onedrive adds thumbnail
- Fix Windows Sharepoint directory problem
- Add Googledrive default root directory
- Support Lanzou Cloud (cookie and URL)
- Fix onedrive sorting problem
- https support
- Add WebDAV transfer options
- Fix the style problem when the file name is too long
- The front-end password input monitors the carriage return event

### v2.0.0-beta7
- Fix the problem that the http connection may not end
- Fixed the issue of missing files when the number of onedrive files is greater than 200
- Attempt to fix the issue that the login page of 189 Cloud Disk is empty [#169](https://github.com/Xhofe/alist/issues/169)
- Add local file sorting [#170](https://github.com/Xhofe/alist/issues/170)
- Fixed the problem of an infinite loop when checking the password of the parent directory under Windows
- Upgrade the markdown component to solve the link rendering problem in the title [#165](https://github.com/Xhofe/alist/issues/165)
- Add the function of switching the logo while switching the theme [#163](https://github.com/Xhofe/alist/issues/163)
- Optimize some back-end styles
- Rewrite the document, yes, it is this document
- Fixed the problem of incorrect password when the password of the current folder is different from that of the parent folder and the folder password check is turned on
- Refactored the Driver part to make the structure clearer
- WebDAV support (read-only)

### v2.0.0-beta6
- Fixed the pointer pointing error when adding an account when restarting
- When deleting an account, delete it from the memory account table at the same time
- Fix the status display of multiple network disks
- Add Tianyi cloud disk support
- Fix the path problem of onedrive under Windows
- Add text preview in gbk format
- Added the backend to view the current password when the password is forgotten
- Cancel useless file caching
- Modify proxy interface
- Add GoogleDrive support
- Add 123 cloud disk support
- Add straight chain password check [#160](https://github.com/Xhofe/alist/issues/160)

### v2.0.0-beta5
:::caution
Because the database has changed the primary key, this version is incompatible with the previous version and needs to be reinstalled.
:::
- Audio add m4a playback [#155](https://github.com/Xhofe/alist/issues/155)
- Simplified setting modification method
- docker add data directory mapping
- The backend is switched from `go-fiber` to `gin`
- Fix the problem of transfer download
- Modify the database primary key
- Add check parent directory password [#157](https://github.com/Xhofe/alist/issues/157)
- Add custom styles/scripts
- Fix the bug that the list is not filtered when playing music
- Add class names to components to facilitate custom styles

### v2.0.0-beta4
- When deleting an account, delete the scheduled task at the same time
- Add markdown theme settings
- Fix that the direct link cannot be downloaded when the path contains +
- Add docker automatic build
- Fix the reminder that an error occurred when clearing the cache
- Add file download button
- Fix the reminder when turning pages
- Fix mysql key keyword issue [#151](https://github.com/Xhofe/alist/issues/151)

### v2.0.0-beta3
- Fix the bug that the meta added in beta1 cannot be deleted
- Cancel the cache when the folder is empty
- Fix the status display problem of onedrive
- Add front-end static file cdn
- Lazy loading of some components
- Fix the bug that the setting does not take effect for the first time due to slow loading
- Fix the bug that cannot be copied in http protocol
- Add direct links to all files in the copied directory
- Add some tooltips to the buttons

### v2.0.0-beta2
- Fix path is not formatted when adding meta
- The readme setting of the homepage when adding multiple accounts
- Fix the bug that the setting modification cannot be entered
- Fix background management title error

### v2.0.0-beta
- Initial release of v2