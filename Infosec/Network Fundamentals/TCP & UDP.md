## TCP

The [Transmission Control Protocol (TCP)](https://en.wikipedia.org/wiki/Transmission_Control_Protocol) is designed with reliability and gurantee in mind. This protocol need a constant connection for the transfert. Because of the processing like check if the paquets are received, it's lower than UDP.

|Advantages|Disadvantages|
|----------|-------------|
|Guarantees the accuracy of the data.|Requires a reliable connection between the two devices. If one small chunk of data is not received, then the entire chunk of data cannot be used.|
|Capable of synchronising two devices to prevent each other from being flooded with data.|A slow connection can bottleneck another device as the connection will be reserved on the receiving computer the whole time.|
|Performs a lot more processes for reliability.|TCP is significantly slower than UDP because more work has to be done by the devices using this protocol.|

TCP is used for file sharing or email sending for exemple or other things where the data need to be complete.

---

## UDP

The [User Datagram Protocol (UDP)](https://en.wikipedia.org/wiki/User_Datagram_Protocol) is less advanced than TCP, it just send the data and does not worry if the data is received. Consequently it's faster than TCP.


|Advantages|Disadvantages|
|----------|-------------|
|UDP is much faster than TCP.|UDP doesn't care if the data is received.|
|UDP leaves the application layer (user software) to decide if there is any control over how quickly packets are sent.|It is quite flexible to software developers in this sense.|
|UDP does not reserve a continuous connection on a device as TCP does.| This means that unstable connections result in a terrible experience for the user.|

UDP is used when lost paquets is not a problem, like video streaming or in [[LAN#ARP Protocol|ARP]] and [[LAN#DHCP Protocol|DHCP]].
