



# main.yml
  
---
## minio_server_download_url


URL to download minio from
...
  
```

'{{ minio_server_download_base_url }}/minio'
  
```
|Where referenced|
| :--- |
|tasks/minio/minio.yml<br/>|

## minio_server_addr


Minio server listen address
...
  
```

:{{ minio_port }}
...
  
```
|Where referenced|
| :--- |
|templates/minio.env.j2<br/>templates/minio.service.j2<br/>|
