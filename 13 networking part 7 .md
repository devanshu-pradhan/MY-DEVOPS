<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
 
</head>
<body>

  <h1>🌐 Networking Basics – Part 7</h1>
  <p><strong>Focus:</strong> Packet Filtering, QoS, SNMP, TLS/SSL</p>

  <h2>🧱 1. Packet Filtering: Stateless vs Stateful</h2>
  <p>Packet filtering is the foundation of firewalls and is used to allow or block traffic.</p>

  <h3>🔸 Stateless Filtering</h3>
  <ul>
    <li>Does not track the state of connections.</li>
    <li>Each packet is checked individually.</li>
    <li>Faster, but less secure.</li>
  </ul>
  <pre><code># Example: Block incoming SSH
sudo iptables -A INPUT -p tcp --dport 22 -j DROP</code></pre>

  <h3>🔹 Stateful Filtering</h3>
  <ul>
    <li>Tracks the state of connections (e.g., NEW, ESTABLISHED).</li>
    <li>Allows return traffic automatically.</li>
    <li>More secure and dynamic.</li>
  </ul>
  <pre><code># Allow established connections only
sudo iptables -A INPUT -m conntrack --ctstate ESTABLISHED,RELATED -j ACCEPT</code></pre>

  <h2>🚦 2. QoS (Quality of Service) and Traffic Shaping</h2>
  <p>QoS helps manage bandwidth and prioritize network traffic.</p>

  <h3>🌀 Traffic Shaping</h3>
  <ul>
    <li>Controls upload/download speeds to avoid congestion.</li>
    <li>Implemented using `tc` (traffic control) in Linux.</li>
  </ul>
  <pre><code># Limit eth0 to 1Mbps using HTB
sudo tc qdisc add dev eth0 root handle 1: htb default 30
sudo tc class add dev eth0 parent 1: classid 1:1 htb rate 1mbit</code></pre>

  <h3>📊 Prioritizing Traffic</h3>
  <ul>
    <li>Can assign higher priority to VoIP or video traffic.</li>
    <li>Done via DSCP, classful queuing, or filters.</li>
  </ul>

  <h2>📡 3. SNMP (Simple Network Management Protocol)</h2>
  <p>Used for monitoring and managing network devices.</p>
  <ul>
    <li>Works on UDP port 161.</li>
    <li>SNMPv1/v2c are less secure (community string-based).</li>
    <li>SNMPv3 adds encryption and authentication.</li>
  </ul>
  <pre><code># Check SNMP data from a device
snmpwalk -v2c -c public 192.168.1.1</code></pre>

  <h3>Common Use Cases:</h3>
  <ul>
    <li>Monitor switch/router health, interface stats.</li>
    <li>Automate alerts for threshold breaches.</li>
  </ul>

  <h2>🔐 4. TLS/SSL for Secure Communication</h2>
  <p>TLS (Transport Layer Security) ensures privacy and integrity for data in transit.</p>
  <ul>
    <li>Replaces SSL; current version is TLS 1.3.</li>
    <li>Used in HTTPS, SMTP, FTPS, etc.</li>
    <li>Based on public-key cryptography and session keys.</li>
  </ul>

  <h3>🔍 Verify TLS on a Site</h3>
  <pre><code># Test certificate and TLS handshake
openssl s_client -connect example.com:443</code></pre>

  <h3>📌 Common TLS Terms</h3>
  <ul>
    <li><strong>CA:</strong> Certificate Authority</li>
    <li><strong>CSR:</strong> Certificate Signing Request</li>
    <li><strong>PEM:</strong> Format for storing certificates</li>
  </ul>

  <h2>🧠 Summary</h2>
  <ul>
    <li><strong>Stateless filters</strong> are fast, <strong>stateful filters</strong> are smarter.</li>
    <li><strong>QoS</strong> helps prevent congestion and prioritize traffic.</li>
    <li><strong>SNMP</strong> gives visibility into device health & performance.</li>
    <li><strong>TLS</strong> secures internet traffic and API communication.</li>
  </ul>

  <h2>📍 What’s Next? (Part 8 Preview)</h2>
  <ul>
    <li>🛰️ Advanced Routing Protocols (OSPF, BGP deep dive)</li>
    <li>📦 Linux Kernel Networking Internals</li>
    <li>🧩 Understanding VPNs and tunneling</li>
    <li>📡 Real-world network design examples</li>
  </ul>

</body>
</html>
