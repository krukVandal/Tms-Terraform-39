# Ознакомиться с основами инфраструктуры как код и практическим применением Terraform для управления инфраструктурой.

1. Infrastructure as Code — это подход, когда инфраструктуру описывают в виде кода (файлы конфигурации), а не создают вручную в консоли облачного провайдера.

2. Установил terraform с официального репозитория и проверил версию

<img width="988" height="549" alt="image" src="https://github.com/user-attachments/assets/eb0d06cf-7380-40d9-9fde-7f7fed8f6650" />

3. Создал структуру проекта.

<img width="992" height="558" alt="image" src="https://github.com/user-attachments/assets/af4c78f2-3940-4d95-899c-ea88bd434cb9" />

4-9. Первый делом регистрирую провайдера и добавляю переменные, создаю сеть dem-net, далее создаю подсеть dem-subnet, следующим шагом создаю секьюрити группу и добавляю правила в группу dem-sg, выделил белыми квадратами сначала пытался запихивать туда токен, но он быстро протухает, создал статический ключ и положил его в проект и подтянул в переменную

<img width="1869" height="889" alt="image" src="https://github.com/user-attachments/assets/3936aa7f-4eef-4c14-ac46-1c1b08c98052" />

terraform plan и получил 5 добавляемых ресурсов, затем terraform apply для разворачивания инфраструктуры. 

<img width="1886" height="1009" alt="image" src="https://github.com/user-attachments/assets/00e5a2bf-536f-4a10-9e32-0e029cb10337" />

Командами cli ниже на скриншоте проверил что ресурсы появились в облаке

<img width="1231" height="659" alt="image" src="https://github.com/user-attachments/assets/fc63bd26-af4a-4326-9480-c01e79353cba" />

10-1. Изменил cidr блок и получил 1 change с последующим применением

<img width="1844" height="983" alt="image" src="https://github.com/user-attachments/assets/a7879fb8-d476-420c-82f3-34e39c6b6b59" />

10-2. Применил terraform destroy для сворачивания инфраструктуры
<img width="868" height="1018" alt="image" src="https://github.com/user-attachments/assets/85296b91-7270-4ad3-8903-b13715a64184" />






