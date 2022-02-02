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






