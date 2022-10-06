## Open System Interconnection (OSI) Model

### What is OSI Model

The [OSI Model](https://en.wikipedia.org/wiki/OSI_model) is an absolute fundamental model used in networking. This model provide a framework dictating how all networked device will send, received and interpret data. The main benefit of OSI Model is that it make it possible to standardize the connection between devices.

OSI Model is represented by seven layers who has differents responsabilities, the layer seven is the most high level and the first  is the most low level. The diagram below is a representation of the layers (from seven to one) and the names of the for each layer data units:

![OSI](images/OSI_Model.png)

|Level|Name|Description|
|-----|----|-----------|
|7|Application|How the user interact with data such as  browsers or email client.|
|6|Presentation|Standardisation of the data. This layer acts as a translator for data to and from the application layer. Security features like data encryption (HTTPS for exemple) occur at this layer.|
|5|Session|Create a unique connection (called session when the connection is established) to the computer that the data is destinated for. Then divide the data in small chunk called "packets". It is beneficial because if the connection is lost, we don't need to sent all the data a second time.|
|4|Transport|Data is sent with [[TCP & UDP#TCP\|TCP]] or [[TCP & UDP#UDP\|UDP]] according to the type of data.|
|3|Network|Where the routing and the re-assembly take place. Determine the better path data should take to reach the device using [OSPF (Open Shortest Path First)](https://en.wikipedia.org/wiki/Open_Shortest_Path_First) and [RIP (Routing Information Protocol)](https://en.wikipedia.org/wiki/Routing_Information_Protocol).|
|2|Data Link|Ensure proper transmission and check for errors using [[Intro#Identifying devices on a network\|MAC addresses]] and [LLC (Logical Link Control)](https://en.wikipedia.org/wiki/Logical_link_control)|
|1|Physical||
