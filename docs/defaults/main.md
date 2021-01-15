
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
  
```

vg_min:
  pv: /dev/sdd
  
```  
---
### minio_server_install_volumes
  
```

lv_min:
  drive: vg_min
  size: +100%FREE
  
```  
---
### minio_server_install_dir_mounts
  
```

/var/lib/minio:
  src: /dev/vg_min/lv_min
  
```  
---
### minio_server_datadirs
  
```

/var/lib/minio
...
  
```  
---
### minio_user
  
```

minio
...
  
```  
---
### minio_group
  
```

minio
...
  
```  
---
### minio_server_download_base_url
  
```

https://dl.minio.io/server/minio/release/linux-amd64
...
  
```  
---
### minio_server_bin
  
```

/usr/local/bin/minio
...
  
```  
---
### minio_server_envfile
  
```

/etc/default/minio
...
  
```  
---
### minio_port
  
```

'9091'
  
```  
---
### minio_server_opts
  
```

''
  
```  
---
### minio_access_key
  
```

''
  
```  
---
### minio_secret_key
  
```

''
  
```  
---
### minio_server_env_extra
  
```

''
  
```