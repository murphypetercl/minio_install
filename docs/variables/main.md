
main.yml
========

Contents
========

* [Variables](#variables)
	* [main.yml](#mainyml)
		* [required_packages](#required_packages)
		* [remove_packages](#remove_packages)
		* [minio_server_download_url](#minio_server_download_url)
		* [minio_server_addr](#minio_server_addr)
  
---
# Variables
  
---
## main.yml
  
---
### required_packages
  
```

[]
  
```  
---
### remove_packages
  
```

[]
  
```  
---
### minio_server_download_url


URL to download minio from
...
  
```

'{{ minio_server_download_base_url }}/minio'
  
```  
---
### minio_server_addr


Minio server listen address
...
  
```

:{{ minio_port }}
...
  
```