# Steps
Repo containing steps to perform various activities


## Using Drozer inside Docker

1. Pull the latest `drozer` image from docker. [Checkout](https://hub.docker.com/r/fsecurelabs/drozer)
2. Connect android device with machine.
3. Start the drozer app in device.
4. Perform `port forwarding`.  
```shell
adb forward tcp:31415 tcp:31415
```
5. Find the `IP Address` of device using below command. 
```shell
 adb shell
 ifconfig
```
6. Run the image. `docker run -it fsecurelabs/drozer`
7. Runt he drozer. `drozer console connect --server device_ip:31415`
