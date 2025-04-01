# 1\. Setting up IP Addressing

We are setting up a mock corporate environment. The first thing I'm doing is setting up the IP addressing.

We have one ethernet going to the internet off my home router and another that is dedicated to the internal network for our lab environment

------------------------


Click the network icon then Network & Internet setting in the lower right corner

![](https://ik.imagekit.io/typeai/tr:w-1200,c-at_max/img_Ofpqza7lf7kUqBSDIz.png)

Select Change adapter options

<img src=https://ik.imagekit.io/typeai/tr:w-1200,c-at_max/img_Kf5xg3Fps6U1tEdK27.png width="500">

Decipher which ethernet is which by right clicking and pressing 'Status' > Details

- The ethernet that starts with 10.X.X.X is likely your home router. Rename that \_INTERNET\_

- The ethernet that starts with something like 169.X.X.X is likely the IP for the internal network. Rename than X\_Internal\_X

![](https://ik.imagekit.io/typeai/tr:w-1200,c-at_max/img_cZFteb1XzTfiPM3fLf.png)

Right click the Internal network and select Properties

Double click Internet Protocol Version 4 (TCP/IPv4)\\

Click 'Use the following IP address:'

Set the IP Address

Make the Subnet mask 255.255.255.0

- In a short explanation the '255' kinda locks in those numbers. We're no making a huge network so have less '255' is not necessary

We are not going to set a Default gateway because the Domain Controller (DC) is going to be the default gateway

Set the Preferred DNS server to a loopback address (127.0.0.1) or even to google (8.8.8.8)

![](https://ik.imagekit.io/typeai/tr:w-1200,c-at_max/img_6ki3kW4eYFdi2j5ECd.png)

Select Ok until you are exited out of all menus
