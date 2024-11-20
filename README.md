

## 1. Buka Service IAM 
![image](https://github.com/user-attachments/assets/4b0ba77f-c3d5-4ce1-b151-2e1e4875dbc1)

## 2. Buat user baru `User -> Create User`

![image](https://github.com/user-attachments/assets/2c131f1e-bbef-401d-8b2d-bee6c707fc58)

## 3. Klik IAM User yang terbuat 
![image](https://github.com/user-attachments/assets/43bd0fd7-ff11-4341-9f86-07bfe1229834)

Pada Security Credentials pilih Create Access Key

![image](https://github.com/user-attachments/assets/2b192d8d-439e-4e76-8b2f-d662d51d17be)

## 4. Install AWS Cli 

### Masukkan Access Key dan Secret Key yang sudah dibuat

Pakai command berikut

```
aws configure
```
![image](https://github.com/user-attachments/assets/ddf75f4f-632d-4567-a6c1-f0fac591aaee)

Untuk melihat atau mengedit konfigurasi AWS CLI secara manual, buka file konfigurasi:

```
~/.aws/credentials (untuk Access Key ID dan Secret Access Key)
~/.aws/config (untuk region dan output format)
```

5. Terraform Command

```
Terraform init
Terraform plan
Terraform apply
Terraform destroy
```
