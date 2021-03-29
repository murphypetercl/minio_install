



# main.yml
  
---
## minio_server_install_volume_groups


Volume Group settings
...
  
```

vg_min:
  pv: /dev/sdd
  
```
|Where referenced|
| :--- |
|tasks/volumes.yml<br/>|

## minio_server_install_volumes
  
```

lv_min:
  drive: vg_min
  size: +100%FREE
  
```
## minio_server_install_dir_mounts


Directory for logical volume mount
...
  
```

/var/lib/minio:
  src: /dev/vg_min/lv_min
  
```
|Where referenced|
| :--- |
|tasks/volumes.yml<br/>templates/minio.env.j2<br/>|

## minio_server_datadirs


Minio server data directory
...
  
```

/var/lib/minio
...
  
```
|Type|Vault required|Where referenced|
| :--- | :--- | :--- |
|string|True|templates/minio.env.j2<br/>|

## minio_user


Minio user
...
  
```

minio
...
  
```
|Type|Vault required|Where referenced|
| :--- | :--- | :--- |
|string|True|tasks/directories.yml<br/>tasks/minio/users.yml<br/>templates/minio.init.j2<br/>templates/minio.service.j2<br/>|

## minio_group


Minio user group
...
  
```

minio
...
  
```
|Where referenced|
| :--- |
|tasks/directories.yml<br/>tasks/minio/minio.yml<br/>tasks/minio/users.yml<br/>templates/minio.service.j2<br/>|

## minio_server_download_base_url


Base URL to download minio from
...
  
```

https://dl.minio.io/server/minio/release/linux-amd64
...
  
```
|Where referenced|
| :--- |
|vars/main.yml<br/>|

## minio_server_bin


Minio server bin directory
...
  
```

/usr/local/bin/minio
...
  
```
|Where referenced|
| :--- |
|tasks/minio/minio.yml<br/>templates/minio.init.j2<br/>templates/minio.service.j2<br/>|

## minio_server_envfile


Path to the file containing the ENV variables for the Minio server
...
  
```

/etc/default/minio
...
  
```
|Where referenced|
| :--- |
|tasks/minio/minio.yml<br/>templates/minio.init.j2<br/>templates/minio.service.j2<br/>|

## minio_port


Minio server port
...
  
```

'9091'
  
```
|Where referenced|
| :--- |
|tasks/minio/firewall.yml<br/>vars/main.yml<br/>|

## minio_server_opts


Additional Minio server CLI options
...
  
```

''
  
```
|Where referenced|
| :--- |
|templates/minio.env.j2<br/>|

## minio_access_key


Minio access key
...
  
```

''
  
```
|Where referenced|
| :--- |
|templates/minio.env.j2<br/>|

## minio_secret_key


Minio secret key
...
  
```

''
  
```
|Where referenced|
| :--- |
|templates/minio.env.j2<br/>|

## minio_server_env_extra


Additional environment variables to be set in minio server environment
...
  
```

''
  
```
|Where referenced|
| :--- |
|templates/minio.env.j2<br/>|
