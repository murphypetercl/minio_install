



# minio.env.j2
  
---  
```

{{ ansible_managed | comment }}

# Minio local/remote volumes.
{% if groups['minio_cluster'] | length > 0 %}
# MINIO_VOLUMES="{{ groups['minio_cluster'] | join(' ') }}"
MINIO_VOLUMES="{% for host in groups['minio_cluster'] %}http://{{ host }}{{ minio_server_datadirs }}{% if not loop.last %} {% endif %}{% endfor %}"
{% else %}
MINIO_VOLUMES="{{ minio_server_install_dir_mounts | join(' ') }}"
{% endif %}
# Minio cli options.
MINIO_OPTS="--address {{ minio_server_addr }} {{ minio_server_opts }}"

{% if minio_access_key %}
# Access Key of the server.
MINIO_ACCESS_KEY="{{ minio_access_key }}"
{% endif %}
{% if minio_secret_key %}
# Secret key of the server.
MINIO_SECRET_KEY="{{ minio_secret_key }}"
{% endif %}

{{ minio_server_env_extra }}
  
```