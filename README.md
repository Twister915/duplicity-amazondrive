
## Setup

This backend needs at least Duplicity 0.7+ and python-requests python-requests-oauthlib


```
# Linux
cp amazondrivebackend.py /usr/lib/python2.7/dist-packages/duplicity/backends/

# MacOS X
cp amazondrivebackend.py /Library/Frameworks/Python.framework/Versions/2.7/lib/python2.7/site-packages/duplicity/backends
```

On first usage you will need to open an URL in a browser and copy the resulting URL back into the tool to enable oauth access. The data will be stored in `~/.duplicity_amazondrive_oauthtoken.json`.


## Usage
```
duplicity source_path amazondrive:///backup/my_new_backup
ACD_OAUTH_PATH=/some/path/to/oauth_json_file.json duplicity source_path amazondrive:///backup/my_other_backup
```

# License

Same as Duplicity
