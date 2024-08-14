# Minio

### Instalar o Minio no Kubernetes:

- `git clone git@github.com:diegofnunesbr/minio.git`
- `cd minio`
- `helm install --create-namespace minio -n minio .`

### Configurar o Minio no arquivo hosts do Windows:

- `sudo tee -a /mnt/c/Windows/System32/drivers/etc/hosts <<< "$(ifconfig eth0 | grep 'inet ' | awk '{print $2}') minio.local"`

### Criar bucket no Minio:

- `mc mb myminio/velero`

### Exibir bucket no Minio:

- `mc ls myminio velero`

### Remover bucket no Minio:

- `mc rb myminio/velero --force`

### Remover o Minio no Kubernetes:

- `helm uninstall minio -n minio`
