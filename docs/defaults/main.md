



# main.yml
  
---
## minio_server_install_volume_groups


Volume Group settings
...
  
```

vg_min:
  pv: /dev/sdd
  
```  
**<font color="green">Where Referenced</font>**  
tasks/volumes.yml
## minio_server_install_volumes


Logical volume variable settings
...
  
```

lv_min:
  drive: vg_min
  size: +100%FREE
  
```  
**<font color="green">Where Referenced</font>**  
tasks/main.yml  
tasks/volumes.yml
## minio_server_install_dir_mounts


Directory for logical volume mount
...
  
```

/var/lib/minio:
  src: /dev/vg_min/lv_min
  
```  
**<font color="green">Where Referenced</font>**  
tasks/volumes.yml  
templates/minio.env.j2
## minio_server_datadirs


Minio server data directory
...
  
```

/var/lib/minio
...
  
```  
**<font color="green">Where Referenced</font>**  
templates/minio.env.j2
## minio_user


Minio user
...
  
```

minio
...
  
```  
**<font color="green">Where Referenced</font>**  
tasks/directories.yml  
tasks/minio/users.yml  
templates/minio.init.j2  
templates/minio.service.j2
## minio_group


Minio user group
...
  
```

minio
...
  
```  
**<font color="green">Where Referenced</font>**  
tasks/directories.yml  
tasks/minio/minio.yml  
tasks/minio/users.yml  
templates/minio.service.j2
## minio_server_download_base_url


Base URL to download minio from
...
  
```

https://dl.minio.io/server/minio/release/linux-amd64
...
  
```  
**<font color="green">Where Referenced</font>**  
vars/main.yml
## minio_server_bin


Minio server bin directory
...
  
```

/usr/local/bin/minio
...
  
```  
**<font color="green">Where Referenced</font>**  
tasks/minio/minio.yml  
templates/minio.init.j2  
templates/minio.service.j2
## minio_server_envfile


Path to the file containing the ENV variables for the Minio server
...
  
```

/etc/default/minio
...
  
```  
**<font color="green">Where Referenced</font>**  
tasks/minio/minio.yml  
templates/minio.init.j2  
templates/minio.service.j2
## minio_port


Minio server port
...
  
```

'9091'
  
```  
**<font color="green">Where Referenced</font>**  
tasks/minio/firewall.yml  
vars/main.yml
## minio_server_opts


Additional Minio server CLI options
...
  
```

''
  
```  
**<font color="green">Where Referenced</font>**  
templates/minio.env.j2
## minio_access_key


Minio access key
...
  
```

''
  
```  
**<font color="green">Where Referenced</font>**  
templates/minio.env.j2
## minio_secret_key


Minio secret key
...
  
```

''
  
```  
**<font color="green">Where Referenced</font>**  
templates/minio.env.j2
## minio_server_env_extra


Additional environment variables to be set in minio server environment
...
  
```

''
  
```  
**<font color="green">Where Referenced</font>**  
templates/minio.env.j2