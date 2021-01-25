



# main.yml
  
---
## minio_server_download_url


URL to download minio from
...
  
```

'{{ minio_server_download_base_url }}/minio'
  
```  
**<font color="green">Where Referenced</font>**  
tasks/minio/minio.yml
## minio_server_addr


Minio server listen address
...
  
```

:{{ minio_port }}
...
  
```  
**<font color="green">Where Referenced</font>**  
templates/minio.env.j2  
templates/minio.service.j2