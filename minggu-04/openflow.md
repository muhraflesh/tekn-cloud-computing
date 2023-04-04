OpenFlow
----------

> Step 1: Installing required Software

Untuk melakukan installasi Virtual Machine Image dapat didownload pada : </br>
https://github.com/mininet/mininet/releases/download/2.2.2/mininet-2.2.2-170321-ubuntu-14.04.4-server-amd64.zip


> Step 2: Setup Virtual Machine

Jalankan VirtualBox, lalu pilih File->Import Appliance dan pilih image .ovf yang telah diunduh.

![1](openflow-01.png)

Selanjutnya, setelah klik import, lakukan setting pada network adapter 2 dengan memilih host-only adapter, seperti berikut :

![2](openflow-02.png)

Kemudian jalankan virtualbox image dan login menggunakan username dan password mininet

![3](openflow-03.png)

Setting interface dengan perintah :

![4](openflow-04.png)

Setting up Port Forwarding

![5](openflow-05.png)


> Step 3: SSH Connections after set up Port Forwarding

Pada windows jalankan perintah

![9](openflow-06.png)

