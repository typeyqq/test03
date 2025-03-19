# An Industrial Internet Security Assessment Model Based on a Selectable Confidence Rule Base
This project is a full stack instant messaging project implemented on the Windows 11 system, supporting functions such as adding friends, friend communication, and displaying chat records
Yes, simulate WeChat layout and use QSS to optimize the interface. The backend adopts a distributed design, divided into Gateserver gateway services and multiple chatserver chat services,
There are four service modules: Status Server status service and Verifyserver verification service. The data storage adopts MySQL service and is based on
The mysqlconnector library encapsulates connection pools, while encapsulating Redis connection pools as cache databases and gRPC connection pools to ensure concurrent access across multiple services
Ask.
Main job: Front end implementation: 1 Implement bubble chat dialog box based on QT, implement friend list through QListwidget, use GridLayout and QPainter
Encapsulate the bubble chat box component and encapsulate HTTP and TCP services based on the network module in QT.
2. Support adding friends, friend communication, chat history display and other functions, imitating WeChat layout and using QSS optimized interface.
• Backend implementation: 3 Adopting a distributed design, it is divided into Gateserver gateway service, multiple Chatserver chat services, and Status Server status service
And Verifyserver verification service. Each service communicates through GRPC and supports disconnection and reconnection.
4. When the user logs in, the GateServer will query the Status Server for available ChatServers
And choose services with lighter loads to achieve load balancing. ChatServer uses the ASIO library to implement reliable long-term connections based on the TCP protocol
Receive and forward messages using asynchronous communication. Using multi-threaded mode to encapsulate the io_comtext pool to improve concurrency performance.
• 5.  The data storage adopts the mysqI service and encapsulates the connection pool based on the mysqlconnector library, while encapsulating the Redis connection pool to process cached data
GRPC connection pool ensures concurrent access to multiple services.