<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">

</head>
<body>

  <h1>📅Linux - Networking Basics🚀</h1>


  <h2>🌐 What is Networking?</h2>
  <p>Networking is the practice of connecting computers and devices to share data, services, and resources. As a DevOps engineer, understanding how data flows between systems is critical for automation, troubleshooting, and security.</p>

  <h2>🧩 Key Networking Concepts</h2>
  <ul>
    <li><strong>IP Addressing:</strong> Logical address assigned to a device (e.g., <code>192.168.1.10</code>). IPv4 and IPv6 are two types.</li>
    <li><strong>MAC Address:</strong> Hardware address assigned to a NIC (Network Interface Card). Example: <code>00:1B:44:11:3A:B7</code></li>
    <li><strong>Private vs Public IP:</strong> Private IPs are used in internal networks, public IPs are internet-routable.</li>
    <li><strong>Subnet Mask:</strong> Determines network and host portions. Example: <code>255.255.255.0</code> (Class C network)</li>
    <li><strong>Default Gateway:</strong> The router address used to access external networks.</li>
  </ul>

  <h2>📦 Protocols Every DevOps Engineer Should Know</h2>
  <ul>
    <li><strong>TCP/IP:</strong> Foundation of internet communication. TCP ensures reliable delivery, IP handles addressing.</li>
    <li><strong>DNS (Port 53):</strong> Translates domain names to IP addresses.</li>
    <li><strong>SSH (Port 22):</strong> Secure access to remote servers.</li>
    <li><strong>HTTP/HTTPS (Ports 80/443):</strong> Web communication protocols.</li>
    <li><strong>FTP/SFTP:</strong> File transfer between systems.</li>
  </ul>

  <h2>🔧 Common Networking Tools & Commands</h2>
  <ul>
    <li><code>ip a</code> – Show IP addresses of interfaces</li>
    <li><code>ping &lt;host&gt;</code> – Test connectivity</li>
    <li><code>traceroute &lt;host&gt;</code> – Trace route taken to a host</li>
    <li><code>netstat -tulnp</code> – Show open ports and listening services</li>
    <li><code>nmap &lt;host&gt;</code> – Network scanner for open ports</li>
    <li><code>curl http://example.com</code> – Transfer data from or to a server</li>
    <li><code>dig google.com</code> – Query DNS servers for domain information</li>
    <li><code>ss -tuln</code> – Faster alternative to netstat</li>
  </ul>

  <h2>📘 OSI Model (7 Layers of Networking)</h2>
  <ol>
    <li><strong>Physical:</strong> Hardware (cables, switches)</li>
    <li><strong>Data Link:</strong> MAC addressing, Ethernet</li>
    <li><strong>Network:</strong> IP addressing, routing</li>
    <li><strong>Transport:</strong> TCP/UDP ports and reliable delivery</li>
    <li><strong>Session:</strong> Establishing and managing sessions</li>
    <li><strong>Presentation:</strong> Data encoding, encryption</li>
    <li><strong>Application:</strong> End-user services (HTTP, DNS, etc.)</li>
  </ol>

  <h2>🔐 Important Port Numbers</h2>
  <ul>
    <li><code>22</code> – SSH</li>
    <li><code>80</code> – HTTP</li>
    <li><code>443</code> – HTTPS</li>
    <li><code>21</code> – FTP</li>
    <li><code>53</code> – DNS</li>
    <li><code>25</code> – SMTP (Email)</li>
    <li><code>3306</code> – MySQL</li>
    <li><code>6379</code> – Redis</li>
  </ul>

  <h3>🧠 Key Takeaway:</h3>
  <p>"Networking is the foundation of system communication in DevOps. Without understanding IPs, ports, protocols, and tools — infrastructure management and automation will be incomplete."</p>

  <h2>📍 What's Next?</h2>
  <ul>
    <li>Explore <strong>firewalls</strong> like <code>ufw</code> and <code>iptables</code></li>
    <li>Understand <strong>NAT</strong> and <strong>port forwarding</strong></li>
    <li>Use <strong>tcpdump</strong> and <strong>wireshark</strong> to inspect packets</li>
    <li>Practice SSH hardening and secure remote access</li>
    <li>Learn about <strong>load balancing</strong> and <strong>reverse proxies</strong> (Nginx/HAProxy)</li>
  </ul>

</body>
</html>
