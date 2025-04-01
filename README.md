# 1. Setting up IP Addressing

We are setting up a mock corporate environment. The first thing we're doing is setting up the IP addressing.

We have one ethernet connection going to the internet off the home router and another that is dedicated to the internal network for our lab environment.

----------------------------------

Here's how to set it up:

1. Click the network icon then select "Network & Internet settings" in the lower right corner
![](https://ik.imagekit.io/typeai/tr:w-1200,c-at_max/img_Ofpqza7lf7kUqBSDIz.png)
2. Select "Change adapter options"
<img src=https://ik.imagekit.io/typeai/tr:w-1200,c-at_max/img_Kf5xg3Fps6U1tEdK27.png width=500px>
3. Identify which ethernet is which by right-clicking and selecting 'Status' > 'Details'

- The ethernet that starts with 10.X.X.X is likely your home router. Rename that to "*INTERNET*"
- The ethernet that starts with something like 169.X.X.X is likely the IP for the internal network. Rename that to "X\_Internal\_X"

![](https://ik.imagekit.io/typeai/tr:w-1200,c-at_max/img_cZFteb1XzTfiPM3fLf.png)

4. Right-click the Internal network and select "Properties"

5. Double-click "Internet Protocol Version 4 (TCP/IPv4)"

6. Click 'Use the following IP address:'

7. Configure the following settings:
    - Set the IP Address
    - Make the Subnet mask 255.255.255.0
      - Note: The '255' effectively locks in those numbers. Since we're not making a huge network, having fewer '255's is not necessary
    - Leave the Default gateway blank because the Domain Controller (DC) will serve as the default gateway
    - Set the Preferred DNS server to a loopback address (127.0.0.1) or to Google's DNS (8.8.8.8)

![](https://ik.imagekit.io/typeai/tr:w-1200,c-at_max/img_6ki3kW4eYFdi2j5ECd.png)

8. Select OK until you exit all menus
