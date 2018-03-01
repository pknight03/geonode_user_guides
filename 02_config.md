# Config

## Set the correct GeoServer Proxy URL value

If you are unable to log in to GeoServer the default username is admin with geoserver as the password. 

`Change this ASAP and update local_settings.py.`

Navigate to GeoServer from the main GeoNode page. Login and click on Global in the Settings section

![geoserver_settings_global.png](https://github.com/BrcMapsTeam/geonode_user_guides/blob/master/img/geoserver_settings_global.png "geoserver_settings_global.png")

Change the Proxy Base URL, changing localhost:8080 to your HOSTNAME or IP address

![geoserver_settings_global_url.png](https://github.com/BrcMapsTeam/geonode_user_guides/blob/master/img/geoserver_serttings_global_url.PNG "geoserver_settings_global_url.png")

## Configure Printing Module

This will edit the printing options for Geonode

Navigate to, the GeoServer Data directory and edit the file `/usr/share/geoserver/data/printing/config.yaml`

1. To change the dpi options edit the first section. In the below example, I have only allopwed 150 and 300dpi prints.

![printing_module_config_dpi_1.PNG](https://github.com/BrcMapsTeam/geonode_user_guides/blob/master/img/printing_module_config_dpi_1.PNG "printing_module_config_dpi_1.PNG")

![printing_module_config_dpi.PNG](https://github.com/BrcMapsTeam/geonode_user_guides/blob/master/img/printing_module_config_dpi.PNG "printing_module_config_dpi.PNG")

2. Ensure that the IP or HOSTNAME is listed. For example:

```
hosts:
  - !dnsMatch
    host: YOUR_IP_ADDRESS
    port: 80
```

---








image an text credit: geonode.org and contributors