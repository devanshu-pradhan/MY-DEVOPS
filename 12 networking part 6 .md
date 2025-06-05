<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  
</head>
<body>

  <h1>🌐 Networking Basics – Part 6</h1>
  <p><strong>Focus:</strong> DNS Resolution & Caching, Bandwidth Monitoring, Troubleshooting Tools, Static & Dynamic Routing</p>

  <!-- 1. DNS -->
  <h2>1️⃣ Deep DNS Resolution & Caching</h2>
  <p>DNS translates human-readable host names to IP addresses. Understanding each step helps diagnose latency or resolution failures.</p>
  <ol>
    <li><strong>Stub Resolver</strong> – Client library in the OS (e.g., <code>glibc</code>) sends a query.</li>
    <li><strong>Recursive Resolver</strong> – Usually your ISP or a public resolver (8.8.8.8) that performs iterative look-ups.</li>
    <li><strong>Root Name Server</strong> – Directs to TLD servers (.com, .org, etc.).</li>
    <li><strong>TLD Server</strong> – Points to authoritative server for the domain.</li>
    <li><strong>Authoritative Server</strong> – Returns the final A/AAAA/CNAME/MX/etc. record.</li>
  </ol>
  <pre><code># Query an authoritative answer
dig +trace example.com

# View local resolver cache (systemd-resolved)
resolvectl statistics
resolvectl query example.com</code></pre>
  <p><em>Tip for DevOps:</em> Internal caching resolvers (e.g., dnsmasq, CoreDNS) reduce latency and external DNS traffic.</p>

  <!-- 2. Bandwidth monitoring -->
  <h2>2️⃣ Bandwidth Monitoring Tools</h2>
  <ul>
    <li><strong>iftop</strong> – Real-time per-connection bandwidth usage.</li>
    <li><strong>bmon</strong> – Console bandwidth monitor with multiple interfaces.</li>
    <li><strong>iperf / iperf3</strong> – Actively measure maximum TCP/UDP throughput between two hosts.</li>
  </ul>
  <pre><code># Live bandwidth on interface eth0
sudo iftop -i eth0

# Test raw throughput (server)
iperf3 -s
# ...and from client
iperf3 -c <server-ip> -P 4   # 4 parallel streams
</code></pre>

  <!-- 3. Troubleshooting utilities -->
  <h2>3️⃣ Core Troubleshooting Utilities</h2>
  <ul>
    <li><strong>tcpdump</strong> – Packet capture for CLI inspection.</li>
    <li><strong>wireshark</strong> – GUI packet analyzer (deep dive into protocols).</li>
    <li><strong>ss / netstat</strong> – List open sockets and their states.</li>
    <li><strong>mtr</strong> – Combines ping + traceroute for path quality over time.</li>
  </ul>
  <pre><code># Capture HTTP traffic on eth0
sudo tcpdump -i eth0 tcp port 80 -nn

# Continuous path quality to 8.8.8.8
mtr 8.8.8.8

# Current listening ports
ss -tuln
</code></pre>

  <!-- 4. Routing -->
  <h2>4️⃣ Static & Dynamic Routing</h2>
  <h3>Static Routing</h3>
  <p>Administrator defines fixed routes. Simple but manual maintenance.</p>
  <pre><code># Add static route (Linux)
sudo ip route add 10.20.30.0/24 via 192.168.1.1 dev eth0</code></pre>

  <h3>Dynamic Routing Protocols</h3>
  <ul>
    <li><strong>RIP</strong> – Legacy distance-vector (hop count).</li>
    <li><strong>OSPF</strong> – Link-state, intra-domain, quick convergence.</li>
    <li><strong>BGP</strong> – Path-vector, primary protocol of the Internet.</li>
  </ul>
  <p>For labs or small private networks you can run <strong>FRRouting</strong> (fork of Quagga) or <strong>Bird</strong> to experiment:</p>
  <pre><code># Example OSPF area config snippet (FRRouting zebra.conf)
router ospf
  network 192.168.1.0/24 area 0
</code></pre>
  <p><em>Light DevOps link:</em> Dynamic routing becomes crucial when building highly-available multi-site clusters or hybrid cloud links.</p>

  <!-- Summary -->
  <h2>🧠 Quick Summary</h2>
  <ul>
    <li><strong>DNS flow</strong> → root → TLD → authoritative; caches cut lookup time.</li>
    <li>Use <code>iftop</code>, <code>bmon</code>, <code>iperf3</code> for bandwidth visibility.</li>
    <li><code>tcpdump</code> + <code>wireshark</code> = packet-level troubleshooting power.</li>
    <li>Static routes are simple; dynamic protocols scale networks automatically.</li>
  </ul>

  <!-- Next preview -->
  <h2>📍 What’s Next? (Part 7 Preview)</h2>
  <ul>
    <li>📦 Packet filtering deep dive (stateful vs stateless)</li>
    <li>🔄 QoS and traffic shaping (tc, HTB)</li>
    <li>🔔 SNMP for network monitoring</li>
    <li>🔐 TLS/SSL basics for secure transport</li>
  </ul>

</body>
</html>
