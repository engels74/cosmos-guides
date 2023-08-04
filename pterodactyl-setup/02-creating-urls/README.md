# 02) Creating URLs

Now we must create reverse proxied urls for our two main containers, the `pt-panel` and `pt-wings`. Fortunately, Cosmos Server makes it very simple.

We only need to tweak the `pt-wings` a little to get it to work properly.

### Why use reverse proxied URLs?

Using reverse proxied URLs can be more secure than using the public IP and port assigned to the service you want to expose to the internet for several reasons:

1. **Reduced attack surface:** By using a reverse proxy, you can limit the number of open ports exposed to the internet, reducing the attack surface. For example, instead of exposing each service on its own port, you can use a reverse proxy to expose all services on port 443 (HTTPS) or 80 (HTTP) and use URL routing to direct traffic to the appropriate service.
2. **SSL termination:** SSL/TLS provides end-to-end encryption between the client and server, but if the server is directly exposed to the internet, it must handle SSL/TLS termination. This means the server has to manage the SSL/TLS decryption process, increasing the risk of exposing the private key. By using a reverse proxy, you can terminate the SSL/TLS connection at the proxy, reducing the risk of exposing the private key.
3. **Authentication and authorization:** Reverse proxies can provide authentication and authorization mechanisms, such as user-based access control and two-factor authentication, that can add an additional layer of security to your services.
4. **Load balancing and scalability:** Reverse proxies can also provide load balancing and scalability capabilities, allowing you to distribute incoming traffic across multiple servers and services.

Overall, reverse proxies can provide an additional layer of security and functionality to your services, making them a valuable addition to any security architecture.

As an addition, we can utilize Cosmos Server built-in [SmartShield](https://github.com/azukaar/Cosmos-Server#what-is-the-smartshield)!

### On to the next step!
