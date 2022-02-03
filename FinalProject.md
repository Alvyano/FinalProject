# **Modul 4 Practicum Report**

### By : Alvyano Rizqilla & Difa Taufiqurahman

----

LXC yang kita perlukan adalah :

* 6 LXC ubuntu 20.04 PHP 7.4
* 2 LXC debian 10 PHP 5.6
* 1 LXC debian 10 mariadb server

![1](https://user-images.githubusercontent.com/80197844/152252304-7bc2f982-1ba1-4496-a12b-8be3bb8d4075.PNG)
install open ssh server di semua lxc
```
apt install openssh-server
```

nano /etc/hosts

![2](https://user-images.githubusercontent.com/80197844/152252485-b653ac43-7606-44a1-920e-d574abd19e09.PNG)
```
Ci
```

lalu kita buat Ansible codeiginiter dengan nama install-ci.yml yang berisi domain container yang kita gunakan

![4 ci](https://user-images.githubusercontent.com/80197844/152252721-c2a2045a-0543-4e4a-af20-78c586795a9a.PNG)

Buat direktori handlers, tasks dan templates

app/handlers

![app 1](https://user-images.githubusercontent.com/80197844/152253398-2b55876c-ffe0-4167-a06d-621720757543.PNG)

app/tasks

![app 2](https://user-images.githubusercontent.com/80197844/152253416-f193834b-b61d-4512-8fc2-8d5956066ffa.PNG)

app/templates

![app 3](https://user-images.githubusercontent.com/80197844/152253429-d68dcdcd-5c04-4a6a-83f5-e920a5036817.PNG)

Hasil Ansible Ci

![Ansible ci](https://user-images.githubusercontent.com/80197844/152254352-24c41c98-0e02-439e-a56d-2e531c70e747.jpeg)


lalu kita akses http://kelompok09.fpsas/app
![codelgniter website](https://user-images.githubusercontent.com/80197844/152253955-cecfa7c1-d452-4866-ba35-f96b95c84dbe.PNG)

```
Laravel
```
Set domain pada Laravel dengan membuat install-laravel.yml
![install laravel yml](https://user-images.githubusercontent.com/80197844/152254169-b2a8971b-d857-4b12-bdb5-508616da3d4e.PNG)

php handlers

![php 1](https://user-images.githubusercontent.com/80197844/152254249-2a4bcb38-2d23-4b12-ada8-a7b3c8557dff.PNG)

php tasks

![php 2](https://user-images.githubusercontent.com/80197844/152254273-133ce0a7-de00-407d-b2ba-9a276c16ba71.PNG)

laravel handlers

![lv 1](https://user-images.githubusercontent.com/80197844/152255088-0f9c5dce-341e-438b-8980-c03cebcdd4d2.PNG)

laravel tasks

![lv 2](https://user-images.githubusercontent.com/80197844/152255131-a35f67ee-8cb5-4ed5-9fbc-babc9b0d4a83.PNG)

laravel env.templates

![lv 3 env templates](https://user-images.githubusercontent.com/80197844/152255217-ad83114c-60ba-4851-8591-2effc58db45a.PNG)

laravel .conf

![lv 4 lv conf](https://user-images.githubusercontent.com/80197844/152255469-ea917962-87e2-40c7-a241-4b3bca9e47ce.PNG)

laravel www.conf

![lv 5 www conf](https://user-images.githubusercontent.com/80197844/152255484-7ba53e39-4d40-4a73-8834-d05c032e6c47.PNG)

ansible laravel

![ansible laravel 1](https://user-images.githubusercontent.com/80197844/152255568-69ec9d5e-b4c3-401c-adad-ad93da8ed54e.PNG)
![ansible laravel 2 ](https://user-images.githubusercontent.com/80197844/152255583-d6a24000-465c-45a4-9add-22555b3e87df.PNG)

lalu kita akses laravel nya http://kelompok09.fpas/ 

![laravel website](https://user-images.githubusercontent.com/80197844/152255618-36ea71f0-6c44-4e6c-b17a-316996dee744.PNG)

```
Yii
```
install-yi.yml

![install yii yaml](https://user-images.githubusercontent.com/80197844/152255856-d157d5dc-a2d9-4957-93e9-e68ba5688d14.PNG)

yii handlers

![yii 1](https://user-images.githubusercontent.com/80197844/152255916-3c9da8fd-5a7e-4748-8f29-4dd59d8527a6.PNG)

yii tasks

![yii 2](https://user-images.githubusercontent.com/80197844/152255941-f5fc4d68-a14c-4382-a40f-701d78a01f5c.PNG)

yii. conf

![yii 3](https://user-images.githubusercontent.com/80197844/152256100-0f00c3a3-cb9f-4e9c-8226-04db85817f54.PNG)

Hasil Ansible yii

![ansible yii](https://user-images.githubusercontent.com/80197844/152256129-58479f08-b8c4-4433-a3ed-9a382b58eeb4.PNG)
![ansible yii 2 ](https://user-images.githubusercontent.com/80197844/152256141-eb6b8f6a-cea4-40f1-96e4-3ea5becfc882.PNG)

lalu kita jalankan yii http://kelompok09.fpas/product

![yii website](https://user-images.githubusercontent.com/80197844/152256320-13157e4d-33bb-409c-b671-69c41899ba08.PNG)

```
lxc database
```
insttal-mariadb.yml

![install mariadb yaml](https://user-images.githubusercontent.com/80197844/152256509-4384e6f0-8dea-4ec6-bc30-3f077ad38208.PNG)


db handlers

![db 1](https://user-images.githubusercontent.com/80197844/152256560-f8716fc3-11b9-4b5e-b445-de0076259fa1.PNG)

db tasks

![db 2](https://user-images.githubusercontent.com/80197844/152256578-f24faec9-de09-438d-9d41-7877e6b734f1.PNG)

db templates my.cnf

![db 3](https://user-images.githubusercontent.com/80197844/152256691-4189fa35-d970-482f-9124-25005355ee09.PNG)

lalu kita jalankan DB dan database dapat dijalankan dan tersambung dengan YII

![php mya admin 1](https://user-images.githubusercontent.com/80197844/152257024-b02e8a18-622d-48b6-b06a-ccd7208bb284.PNG)

![php mya admin 2](https://user-images.githubusercontent.com/80197844/152257053-0535d238-0fcf-4ae7-a43c-7f24b11c7d9f.PNG)

```
wp
```
install wp.yml


![install wp yml](https://user-images.githubusercontent.com/80197844/152294147-a20ba45a-bfee-466b-8507-9afcdb57ad6b.PNG)

```
wp handlers
```

![wp 1](https://user-images.githubusercontent.com/80197844/152295956-643904d3-9f48-4890-937a-74f37d24b965.PNG)

wp tasks

![wp 2](https://user-images.githubusercontent.com/80197844/152295976-2b9f484d-267e-4806-98b5-402d1b7a4bad.PNG)

wp templates wp.conf

![wp 3](https://user-images.githubusercontent.com/80197844/152295995-3f441f02-db92-4856-b8f8-270e5e3cb2da.PNG)

wp templates wp.local

![wp 4](https://user-images.githubusercontent.com/80197844/152298050-6191187f-11de-40a3-b6a5-e8d3ef1128e6.PNG)

Hasil Ansible wp

![ansible wp](https://user-images.githubusercontent.com/80197844/152298291-e9115d40-5dcb-4c2d-9c88-565068909930.PNG)

![ansible wp 2 ](https://user-images.githubusercontent.com/80197844/152304458-5ae2d3e7-0189-4c8b-8405-d284d9a79385.PNG)


lalu kita jalankan wp

![wp website](https://user-images.githubusercontent.com/80197844/152298092-f15d40bd-f912-4616-8489-d00910fdf61f.PNG)

```
set host utama
```
nano /etc/hosts
![2](https://user-images.githubusercontent.com/80197844/152257263-7ae134e0-de0a-456e-b11a-ff8a78793568.PNG)

```
Host Grouping
```
lakukan grouping pada host untuk memfokuskan lxc sesuai yang diperlukan

![3](https://user-images.githubusercontent.com/80197844/152257443-88304b3c-1315-40c8-9674-7f17e02a7d64.PNG)


















