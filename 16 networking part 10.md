<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">

</head>
<body>

  <h1>🌐 Networking Basics – Part 10 (Final)</h1>
  <p><strong>Focus:</strong> IPv6, Load Balancing, Mesh & SDN, Revision Cheatsheet</p>

  <!-- 1. IPv6 -->
  <h2>1️⃣ IPv6 – The Future of IP</h2>
  <ul>
    <li>128-bit addressing (e.g., <code>2001:0db8:85a3::8a2e:0370:7334</code>).</li>
    <li>No need for NAT – every device gets a globally unique IP.</li>
    <li>Uses <strong>Link-Local</strong> and <strong>Global Unicast</strong> addresses.</li>
    <li>Supports auto-configuration (SLAAC) and DHCPv6.</li>
  </ul>
  <pre><code># Check IPv6 address on Linux
ip -6 addr

# Ping IPv6 address
ping6 google.com</code></pre>

  <!-- 2. Load Balancing -->
  <h2>2️⃣ Network Load Balancing</h2>
  <ul>
    <li>Distributes traffic across multiple servers or paths.</li>
    <li><strong>Layer 4 (Transport):</strong> Based on TCP/UDP ports (e.g., HAProxy, Nginx).</li>
    <li><strong>Layer 7 (Application):</strong> Based on content (URLs, cookies).</li>
    <li>Helps achieve high availability and horizontal scaling.</li>
  </ul>
  <pre><code># Simple example (HAProxy config)
frontend http_front
 bind *:80
 default_backend http_back

backend http_back
 balance roundrobin
 server web1 192.168.1.10:80 check
 server web2 192.168.1.11:80 check</code></pre>

  <!-- 3. Mesh Networks & SDN -->
  <h2>3️⃣ Mesh Networks & SDN</h2>
  <h3>🔗 Mesh Networking</h3>
  <ul>
    <li>All nodes connect directly and dynamically with each other.</li>
    <li>Used in IoT, community networks, disaster recovery setups.</li>
    <li>Supports self-healing and redundant paths.</li>
  </ul>

  <h3>🧠 SDN – Software Defined Networking</h3>
  <ul>
    <li>Separates control plane (logic) from data plane (packet forwarding).</li>
    <li>Allows centralized network management via SDN controllers (e.g., OpenDaylight).</li>
    <li>Popular in cloud environments and data centers.</li>
  </ul>
  <pre><code># Example SDN tool: Mininet (simulate SDN networks)
sudo mn --topo=tree,depth=2 --controller=remote</code></pre>

  <!-- 4. Final Revision Tips -->
  <h2>📚 Final Revision Tips</h2>
  <ul>
    <li>📄 Create a visual cheat sheet (OSI layers, port numbers, protocols).</li>
    <li>🧠 Practice CLI tools: <code>ping</code>, <code>traceroute</code>, <code>netstat</code>, <code>ip</code>, <code>ss</code>.</li>
    <li>🛠️ Use <strong>Wireshark</strong> to analyze packets and protocols.</li>
    <li>💬 Explain concepts to yourself or others out loud for clarity.</li>
  </ul>

  <!-- 5. Cheat Sheet -->
  <h2>🧾 Interview-Level Networking Cheat Sheet</h2>
  <ul>
    <li><strong>Common Ports:</strong> HTTP (80), HTTPS (443), DNS (53), SSH (22), FTP (21)</li>
    <li><strong>OSI Layers:</strong> Application → Physical (7 to 1)</li>
    <li><strong>IP Address Classes:</strong> A (1–126), B (128–191), C (192–223)</li>
    <li><strong>CIDR:</strong> /24 = 255.255.255.0, /16 = 255.255.0.0</li>
    <li><strong>Tools:</strong> <code>ip</code>, <code>nmap</code>, <code>netstat</code>, <code>dig</code>, <code>tcpdump</code></li>
    <li><strong>Basic Concepts:</strong> Subnetting, NAT, DHCP, DNS, VLANs, Routing, VPNs</li>
  </ul>

  <!-- 6. What's Next -->
  <h2>🚀 What's Next?</h2>
  <ul>
    <li>✨ Start building your <strong>Networking + DevOps Labs</strong> using Linux + Docker + Wireshark.</li>
    <li>📁 Push your notes and mini-projects to GitHub.</li>
    <li>🧑‍💻 Practice troubleshooting on Linux CLI.</li>
    <li>📚 Begin exploring <strong>Cloud Networking (Azure/AWS)</strong>.</li>
  </ul>

  <p><strong>Well done!</strong> You've completed the Networking Basics journey. 🎓💻</p>

</body>
</html>
