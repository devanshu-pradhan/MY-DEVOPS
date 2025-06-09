<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  
</head>
<body>

  <h1>🌐 Networking Basics – Part 9</h1>
  <p><strong>Focus:</strong> Network Security, ARP/DHCP/ICMP/NAT Protocols, Wireless Networking</p>

  <!-- 1. Network Security Best Practices -->
  <h2>🔐 1. Network Security Best Practices</h2>
  <ul>
    <li>Implement perimeter and internal firewalls.</li>
    <li>Use IDS/IPS (e.g., <strong>Snort</strong>, <strong>Suricata</strong>) to detect & prevent intrusions.</li>
    <li>Apply the principle of least privilege (PoLP) to devices and users.</li>
    <li>Regularly patch network firmware and OS.</li>
    <li>Segment networks using VLANs or subnets to isolate sensitive areas.</li>
  </ul>
  <pre><code># Basic iptables rule to drop traffic from suspicious IP
sudo iptables -A INPUT -s 203.0.113.5 -j DROP</code></pre>

  <!-- 2. ARP (Address Resolution Protocol) -->
  <h2>🔄 2. ARP – Address Resolution Protocol</h2>
  <ul>
    <li>Resolves IP addresses to MAC addresses on local networks.</li>
    <li>Works at Layer 2 (Data Link Layer).</li>
    <li>Vulnerable to ARP spoofing/poisoning attacks (use static ARP or dynamic ARP inspection).</li>
  </ul>
  <pre><code># View ARP cache
arp -a</code></pre>

  <!-- 3. DHCP (Dynamic Host Configuration Protocol) -->
  <h2>📥 3. DHCP – Dynamic Host Configuration Protocol</h2>
  <ul>
    <li>Assigns IP addresses to devices automatically.</li>
    <li>Uses UDP ports 67 (server) and 68 (client).</li>
    <li>Supports DNS, gateway, lease time, etc.</li>
  </ul>
  <pre><code># View current DHCP lease (example for Linux)
cat /var/lib/dhcp/dhclient.eth0.leases</code></pre>

  <!-- 4. ICMP (Internet Control Message Protocol) -->
  <h2>📡 4. ICMP – Internet Control Message Protocol</h2>
  <ul>
    <li>Used for diagnostics (e.g., <code>ping</code>, <code>traceroute</code>).</li>
    <li>Type 0 = Echo Reply, Type 8 = Echo Request.</li>
    <li>Can be blocked to avoid ping sweeps and denial-of-service vectors.</li>
  </ul>
  <pre><code># Test connectivity using ICMP
ping 8.8.8.8</code></pre>

  <!-- 5. NAT (Network Address Translation) -->
  <h2>🌍 5. NAT – Network Address Translation</h2>
  <ul>
    <li>Maps private IPs to public IPs for internet access.</li>
    <li>Hides internal IP structure and conserves IPv4 addresses.</li>
    <li>Types: Static NAT, Dynamic NAT, PAT (Port Address Translation).</li>
  </ul>
  <pre><code># View current NAT table (iptables example)
sudo iptables -t nat -L</code></pre>

  <!-- 6. Wireless Networking -->
  <h2>📶 6. Wireless Networking Concepts</h2>
  <ul>
    <li><strong>Frequencies:</strong> 2.4GHz (long range, more interference) vs 5GHz (faster, shorter range).</li>
    <li><strong>Channels:</strong> Overlapping channels can cause interference; use non-overlapping ones.</li>
    <li><strong>WPA3</strong> is the latest secure encryption standard; avoid WEP/WPA1.</li>
    <li>Use strong passphrases, disable WPS, and regularly rotate keys.</li>
  </ul>
  <pre><code># Scan for available Wi-Fi networks
nmcli device wifi list</code></pre>

  <!-- 7. Summary -->
  <h2>🧠 Summary</h2>
  <ul>
    <li>Follow layered security – firewall + segmentation + patching.</li>
    <li>Understand ARP, DHCP, ICMP for troubleshooting and protection.</li>
    <li>Use NAT to connect private networks to the internet securely.</li>
    <li>Wireless networking should balance speed, range, and security.</li>
  </ul>

  <!-- 8. What's Next -->
  <h2>📍 What’s Next? (Part 10 Preview)</h2>
  <ul>
    <li>🔄 IPv6 Concepts and Configuration</li>
    <li>🧱 Network Load Balancing Techniques</li>
    <li>🕸️ Mesh Networks and SDN (Software Defined Networking)</li>
    <li>💡 Final Revision: Cheatsheet + Interview Setups</li>
  </ul>

</body>
</html>
