<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  
</head>
<body>

  <h1>📘 Networking Basics – Part 4</h1>
  <p><strong>Focus:</strong> TCP/IP Stack, ICMP, ARP, DHCP, and IPv6</p>

  <h2>1️⃣ TCP/IP Stack Explained</h2>
  <p>The TCP/IP model has four main layers that define how data is transmitted:</p>
  <ul>
    <li><strong>Application Layer:</strong> Where user applications like HTTP, FTP, DNS operate.</li>
    <li><strong>Transport Layer:</strong> Provides communication reliability. Uses TCP or UDP.</li>
    <li><strong>Internet Layer:</strong> Handles logical addressing and routing using IP.</li>
    <li><strong>Network Access Layer:</strong> Deals with physical transmission (e.g., Ethernet).</li>
  </ul>

  <h2>2️⃣ ICMP (Internet Control Message Protocol)</h2>
  <p>Used for sending diagnostic or control messages. Common tools that use ICMP include:</p>
  <ul>
    <li><strong>ping:</strong> Checks if a host is reachable.</li>
    <li><strong>traceroute:</strong> Displays the path to a host.</li>
  </ul>
  <pre><code># Test connectivity
ping 8.8.8.8

# Trace route to a host
traceroute google.com</code></pre>

  <h2>3️⃣ ARP (Address Resolution Protocol)</h2>
  <p>ARP maps an IP address to a MAC address within a local network. It is essential for devices to communicate in the same LAN.</p>
  <pre><code># View ARP table
arp -a

# Using ip command
ip neigh show</code></pre>

  <h2>4️⃣ DHCP (Dynamic Host Configuration Protocol)</h2>
  <p>DHCP automatically assigns IP addresses and network parameters to devices on a network.</p>
  <ul>
    <li><strong>DHCP Discover</strong>: Client requests IP.</li>
    <li><strong>DHCP Offer</strong>: Server offers an IP.</li>
    <li><strong>DHCP Request</strong>: Client accepts IP.</li>
    <li><strong>DHCP ACK</strong>: Server confirms assignment.</li>
  </ul>
  <pre><code># Release and renew DHCP lease (Linux)
sudo dhclient -r
sudo dhclient</code></pre>

  <h2>5️⃣ Introduction to IPv6</h2>
  <p>IPv6 is the successor of IPv4 and offers a much larger address space (128-bit addresses).</p>
  <ul>
    <li>Example: <code>2001:0db8:85a3:0000:0000:8a2e:0370:7334</code></li>
    <li>Abbreviated: <code>2001:db8:85a3::8a2e:370:7334</code></li>
    <li>IPv6 doesn't use NAT – every device can have a global address.</li>
  </ul>
  <pre><code># View IPv6 address
ip -6 addr

# Ping using IPv6
ping6 ipv6.google.com</code></pre>

  <h2>🧠 Quick Summary</h2>
  <ul>
    <li><strong>TCP/IP:</strong> 4-layer model handling complete communication.</li>
    <li><strong>ICMP:</strong> Vital for diagnostics (ping, traceroute).</li>
    <li><strong>ARP:</strong> Converts IP to MAC for local communication.</li>
    <li><strong>DHCP:</strong> Automatically assigns network info.</li>
    <li><strong>IPv6:</strong> New protocol solving address limitations.</li>
  </ul>

  <h2>📍 What’s Next? (Part 5 Preview)</h2>
  <ul>
    <li>🔐 Firewalls and packet filtering (iptables, nftables)</li>
    <li>🧱 Linux bridges, network namespaces, and virtual interfaces</li>
    <li>📡 Advanced DNS & caching systems</li>
  </ul>

</body>
</html>
