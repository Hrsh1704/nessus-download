# Nessus-download

**downloading process of nessus in kali.**

Firstly we need an nessus debian file for that. go to nessus website and download the file and whatever email address you are entered your regitration key is there.

```
https://www.tenable.com/products/nessus
```

After downloading go to that directory where file was download.
**ex:/home/kali/Dowmloads**

then use this command.

- PUT YOUR FILE NAME 👇
```
dpkg -i Nessus-10.9.2-ubuntu1604_amd64.deb
```
it will be take couple of seconds.

<img width="773" height="317" alt="image" src="https://github.com/user-attachments/assets/50621a29-e0d8-4e9b-8900-a41abf32c3d5" />

# Open browser on kali

change **NESSUS_HOSTNAME_OR_IP** to your ip_address.
 
```
https://YOUR_DEVICE_IP:8834/
```

### after type this command if it's shown you unable to connect then do it.

- check the service active or not through `status `.
- then we need to active it help of `start`.
- then enable the service help of `enable`.
- all commands are written in below.👇

**start the nessus service**
```
sudo systemctl start nessusd
```

**stop the nessus service**
```
sudo systemctl stop nessusd 
```

**to check status. is on or off**
```
sudo systemctl status nessusd
``` 
**if the status was active but service was off then use it**
```
sudo systemctl enable nessusd
```

### after starting the service relod the page now it's shown you an option like ` advanvce ` click on it and then click on `accept risk and continue `

now you can see the nessus page.
**like this**
<img width="318" height="355" alt="image" src="https://github.com/user-attachments/assets/91b049dc-99fe-4ae6-8c8f-316cd5541e34" />
- do not check on `register ofline`
- click on continue
- 


## if you forgot password or process will not work then use this command for compltely remove nessus and reinstall it.
```
sudo systemctl stop nessusd
sudo rm -rf /opt/nessus
sudo apt remove --purge nessus*
sudo apt autoremove
```

