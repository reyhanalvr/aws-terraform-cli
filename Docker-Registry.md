## Install Docker Private Registry dengan Harbor

```
https://goharbor.io/docs/2.0.0/install-config/
```


### Download latest version Harbor dari Git repository.

```
curl -s https://api.github.com/repos/goharbor/harbor/releases/latest | grep browser_download_url | cut -d '"' -f 4 | grep '\.tgz$' | wget -i -
```

![image](https://github.com/user-attachments/assets/4154d0ea-0832-4388-929a-728ffa0e4868)

Setting konfigurasi harbor di harbor.yml

![image](https://github.com/user-attachments/assets/d04606c7-f4f0-48a8-b290-0f2d6e476976)

Jalankan Script yang sudah disediakan oleh harbor

`./install.sh`

![image](https://github.com/user-attachments/assets/4cfe319e-f086-4da6-a819-c757d030c6ca)


Jika sudah terdeploy, masuk ke dashboard harbor

![image](https://github.com/user-attachments/assets/f661cdb7-1d45-4268-b38e-080aaa852a3c)

Buat projects baru dan push image ke Docker Registry 

![image](https://github.com/user-attachments/assets/012f4889-0a05-4e8c-b985-3e2bf344a9c9)
