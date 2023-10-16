# SYSTEM-DESIGN

System Design Concepts

## Security

[OWASP (Open Web Application Security Project) Top 10 Vulnerabilities](security/README.md#owasp-open-web-application-security-project-top-10-vulnerabilities)

[Content-Security-Policy (CSP) Headers](security/README.md#content-security-policy-csp-headers)

## API Design

[API Security Best Practices](security/README.md#api-security-best-practices)

## Components of System Design

- DNS

DNS is a fundamental technology used on the internet to translate human-friendly domain names (like
www.example.com) into IP addresses (like 192.0.2.1), which computers use to identify each other on the network.

Examples - Amazon Route 53, Google Cloud DNS, Azure DNS, and Cloudflare DNS

- CDN

CDN is a network of distributed servers strategically placed around the world, working together to deliver web content, such as images, videos, and other resources, to users from a server that is geographically closer to them.

Examples - Amazon CloudFront, Google Cloud CDN, Cloudflare CDN, Azure Content Delivery Network(CDN)

- Load Balancer

A Load Balancer is a crucial component in distributing incoming network traffic across multiple servers to ensure optimal resource utilization, minimize response time, and prevent overload.

- Web / Application Servers

A Web/Application Server is a specialized software designed to host and manage web applications, providing a platform for processing and delivering content over the internet

- Microservices

Microservices work by breaking down a software application into small, independent services that can be developed, deployed, and scaled individually. These services communicate with each other through well-defined APIs, and together they create a larger application.

- Blob/Object Storage

Storage is a type of data storage used to store and manage unstructured data, such as images, videos, documents, and more, in its native format.

Examples - Amazon S3, Google Cloud Storage, Azure Blob Storage

- Proxy/Reverse Proxy

A proxy serves as an intermediary between a client and a destination server, enabling clients to make requests indirectly through the proxy server. Proxies offer various benefits, including security, privacy, and performance optimization.

https://github.com/krishnamohanathota/DEVOPS#forward-proxy--reverse-proxy

- Database (SQL or NoSQL)

A database is a structured collection of data organized for efficient storage, retrieval, and manipulation. It serves as a digital repository that stores and manages information, allowing users and applications to interact with data.

- Message Queues

A message queue is a communication tool that lets different software parts send and receive messages asynchronously. It helps components exchange data without being connected in real time, enhancing scalability and reliability in applications.

Examples - Apache Kafka, RabbitMQ, Apache ActiveMQ, AWS SQS, Google Cloud Pub/Sub, Azure Service Bus

- Cache at various levels (Client side, CDN, Server side, Database side, Application level caching)

The cache is like a super-fast memory that stores frequently used data, making it quicker to access.

Examples - Redis, Memcached, Amazon ElastiCache, Google Cloud Memorystore, Azure Cache for Redis

![](/images/SystemDesign-Components.png)

## Polling vs WebHook vs WebSockets

### Polling

Polling is a technique used by clients to obtain data from the server by making HTTP requests at regular intervals. It is a simple and effective way to receive data from the server, but it has some drawbacks.

- It is inefficient as it requires the client to continuously poll the server for new data.
- It is not real-time as the client has to wait for the next poll to receive new data.
- It is not scalable as it generates a lot of unnecessary requests to the server.

### WebHook

Webhooks are a way for applications to provide other applications with real-time information. They are automated messages sent from apps when something happens. They have a message—or payload—and are sent to a unique URL—essentially like an app's phone number or address. When a webhook is triggered, the app sends a POST request to the URL, which then sends the payload to the app.

### WebSockets

WebSockets are a communication protocol that provides a persistent connection between a client and a server. It allows the server to send data to the client without the client having to request it. It is a full-duplex communication channel that operates over a single TCP connection.

![](/images/polling-webhook-websocket.gif)
