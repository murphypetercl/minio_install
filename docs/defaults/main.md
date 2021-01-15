
main.yml
========

Contents
========

* [Variables](#variables)
	* [main.yml](#mainyml)
		* [minio_server_install_volume_groups](#minio_server_install_volume_groups)
		* [minio_server_install_volumes](#minio_server_install_volumes)
		* [minio_server_install_dir_mounts](#minio_server_install_dir_mounts)
		* [minio_server_datadirs](#minio_server_datadirs)
		* [minio_user](#minio_user)
		* [minio_group](#minio_group)
		* [minio_server_download_base_url](#minio_server_download_base_url)
		* [minio_server_bin](#minio_server_bin)
		* [minio_server_envfile](#minio_server_envfile)
		* [minio_port](#minio_port)
		* [minio_server_opts](#minio_server_opts)
		* [minio_access_key](#minio_access_key)
		* [minio_secret_key](#minio_secret_key)
		* [minio_server_env_extra](#minio_server_env_extra)
  
---
# Variables
  
---
## main.yml
  
---
### minio_server_install_volume_groups


Volume Group settings
...
  
```

vg_min:
  pv: /dev/sdd
  
```  
---
### minio_server_install_volumes


Logical volume variable settings
...
  
```

lv_min:
  drive: vg_min
  size: +100%FREE
  
```  
---
### minio_server_install_dir_mounts


Directory for logical volume mount
...
  
```

/var/lib/minio:
  src: /dev/vg_min/lv_min
  
```  
---
### minio_server_datadirs


Minio server data directory
...
  
```

/var/lib/minio
...
  
```  
---
### minio_user


Minio user
...
  
```

minio
...
  
```  
---
### minio_group


Minio user group
...
  
```

minio
...
  
```  
---
### minio_server_download_base_url


Base URL to download minio from
...
  
```

https://dl.minio.io/server/minio/release/linux-amd64
...
  
```  
---
### minio_server_bin


Minio server bin directory
...
  
```

/usr/local/bin/minio
...
  
```  
---
### minio_server_envfile


Path to the file containing the ENV variables for the Minio server
...
  
```

/etc/default/minio
...
  
```  
---
### minio_port


Minio server port
...
  
```

'9091'
  
```  
---
### minio_server_opts


Additional Minio server CLI options
...
  
```

''
  
```  
---
### minio_access_key


Minio access key
...
  
```

''
  
```  
---
### minio_secret_key


Minio secret key
...
  
```

''
  
```  
---
### minio_server_env_extra


Additional environment variables to be set in minio server environment
...
  
```

''
  
```