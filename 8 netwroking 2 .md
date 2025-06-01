<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
 
</head>
<body>

  <h1>📅Linux - Networking Basics Part 2🚀</h1>
  <p><strong>Topic:</strong> <em>Networking Basics Part 2 – Intermediate to Advanced Concepts</em></p>

  <h2>🌐 Key Advanced Networking Concepts</h2>

  <h3>🔄 1. NAT (Network Address Translation)</h3>
  <p>Used to translate private IPs (used in LANs) to public IPs (used on the internet). Essential when deploying internal services externally.</p>
  <ul>
    <li><strong>SNAT:</strong> Source NAT, modifies source address.</li>
    <li><strong>DNAT:</strong> Destination NAT, modifies destination address (used in port forwarding).</li>
  </ul>

  <h3>🔁 2. Port Forwarding</h3>
  <p>Maps traffic from a public-facing port to an internal IP:port combination.</p>
  <pre><code># Example using iptables:
sudo iptables -t nat -A PREROUTING -p tcp --dport 8080 -j DNAT --to-destination 192.168.1.10:80</code></pre>

  <h3>📡 3. DHCP (Dynamic Host Configuration Protocol)</h3>
  <p>Dynamically assigns IP addresses, DNS servers, gateway info to clients.</p>

  <h3>🌍 4. DNS Internals</h3>
  <ul>
    <li><strong>A Record:</strong> Maps domain to IPv4 address</li>
    <li><strong>AAAA Record:</strong> Maps domain to IPv6</li>
    <li><strong>CNAME:</strong> Canonical name, alias for another domain</li>
    <li><strong>MX Record:</strong> Mail exchange record</li>
  </ul>
  <pre><code># Use dig to query DNS:
dig A google.com</code></pre>

  <h3>⚖️ 5. Load Balancing</h3>
  <p>Distributes traffic across multiple backend servers. Helps with scaling and fault tolerance.</p>
  <ul>
    <li><strong>Round Robin:</strong> Evenly distributes traffic</li>
    <li><strong>Least Connections:</strong> Chooses server with fewest active connections</li>
    <li><strong>NGINX Example:</strong></li>
  </ul>
  <pre><code>upstream backend {
  server 192.168.1.101;
  server 192.168.1.102;
}
server {
  listen 80;
  location / {
    proxy_pass http://backend;
  }
}</code></pre>

  <h3>🔄 6. Reverse Proxy</h3>
  <p>Acts on behalf of servers to handle client requests (e.g., SSL termination, load balancing).</p>

  <h3>🛡️ 7. Firewalls and Security</h3>
  <p>Filters traffic based on rules. Can restrict inbound/outbound packets.</p>
  <ul>
    <li><strong>UFW:</strong> Simplified firewall on Ubuntu</li>
    <li><strong>iptables:</strong> Full-featured Linux firewall tool</li>
  </ul>
  <pre><code># Allow SSH and HTTP
sudo ufw allow 22
sudo ufw allow 80
sudo ufw enable</code></pre>

  <h3>📊 8. Monitoring Traffic</h3>
  <ul>
    <li><code>iftop</code> – Live bandwidth usage</li>
    <li><code>vnstat</code> – Network traffic statistics</li>
    <li><code>tcpdump</code> – Capture packets</li>
  </ul>
  <pre><code>sudo tcpdump -i eth0 tcp port 443</code></pre>

  <h3>📶 9. TCP vs UDP (Comparison)</h3>
  <table border="1">
    <tr><th>Feature</th><th>TCP</th><th>UDP</th></tr>
    <tr><td>Connection</td><td>Connection-oriented</td><td>Connectionless</td></tr>
    <tr><td>Reliability</td><td>Reliable, with retransmissions</td><td>Unreliable, no retransmit</td></tr>
    <tr><td>Use Case</td><td>Web, Email, SSH</td><td>DNS, Streaming, VoIP</td></tr>
  </table>

  <h3>📂 10. Useful Network Files</h3>
  <ul>
    <li><code>/etc/hosts</code> – Static local DNS entries</li>
    <li><code>/etc/network/interfaces</code> – Interface config (Debian-based)</li>
    <li><code>/etc/resolv.conf</code> – DNS resolver config</li>
  </ul>

  <h3>🔍 11. Common Tools Summary</h3>
  <ul>
    <li><code>ping</code> – Check host reachability</li>
    <li><code>netstat</code>, <code>ss</code> – Show socket stats</li>
    <li><code>traceroute</code> – Show route path</li>
    <li><code>nmap</code> – Scan open ports</li>
    <li><code>dig</code> – DNS resolution</li>
  </ul>

  <h2>🔧 Real-World DevOps Use Case</h2>
  <p>Set up a secure web server with:</p>
  <ul>
    <li>Static IP on private subnet (192.168.x.x)</li>
    <li>NAT Gateway for internet access</li>
    <li>Firewall rules only allowing SSH, HTTP/HTTPS</li>
    <li>DNS entry configured via Route53 (or Azure DNS)</li>
  </ul>

  <h2>🧠 Key Takeaways</h2>
  <ul>
    <li>Understanding NAT, firewall rules, and DNS is key to exposing and securing services</li>
    <li>Monitoring and analyzing traffic helps with security and performance</li>
    <li>Tools like <code>tcpdump</code> and <code>nmap</code> are essential for debugging</li>
  </ul>

  <h2>📍 What’s Next (Part 3 Preview)</h2>
  <ul>
    <li>Cloud Networking (VPC/VNet, NSG, Subnets)</li>
    <li>Zero Trust Networking & VPN</li>
    <li>Service Mesh and Network Policies (Kubernetes)</li>
    <li>DNS as Code (using Terraform or Azure CLI)</li>
  </ul>

</body>
</html>
