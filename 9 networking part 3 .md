<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
</head>
<body>

  <h1>📅 Networking Basics – Part 3</h1>
  <p><strong>Topic:</strong> <em>Routing, Subnetting, NAT, DNS – Deeper Networking Concepts</em></p>

  <h2>🧭 1. Routing Fundamentals</h2>
  <p>Routing is the process of selecting paths in a network along which to send data packets.</p>
  <ul>
    <li><strong>Static Routing:</strong> Manually defined route entries.</li>
    <li><strong>Dynamic Routing:</strong> Uses protocols like OSPF, RIP, or BGP to learn and update routes automatically.</li>
    <li><strong>Default Route:</strong> A route used when no other matches exist (e.g., 0.0.0.0/0).</li>
  </ul>
  <pre><code># View routing table in Linux
ip route show

# Add static route
sudo ip route add 192.168.2.0/24 via 192.168.1.1</code></pre>

  <h2>🔢 2. IP Addressing and Subnetting</h2>
  <p>Subnetting divides a larger network into smaller, manageable sub-networks.</p>
  <ul>
    <li><strong>IP Address:</strong> E.g., 192.168.10.25/24</li>
    <li><strong>Subnet Mask:</strong> Defines the network and host portion (e.g., 255.255.255.0)</li>
    <li><strong>CIDR Notation:</strong> Classless Inter-Domain Routing, e.g., /24</li>
  </ul>
  <p><strong>Subnet Calculation:</strong></p>
  <pre><code>Network: 192.168.10.0/24
Range:   192.168.10.1 – 192.168.10.254
Broadcast: 192.168.10.255
Total Hosts: 254</code></pre>

  <h2>🌐 3. NAT (Network Address Translation)</h2>
  <p>Translates private IP addresses to public IPs. Useful in LAN-to-Internet scenarios.</p>
  <ul>
    <li><strong>SNAT (Source NAT):</strong> Used for outbound connections (internal → internet).</li>
    <li><strong>DNAT (Destination NAT):</strong> Used for port forwarding (internet → internal).</li>
  </ul>
  <pre><code># Example using iptables for SNAT
sudo iptables -t nat -A POSTROUTING -o eth0 -j MASQUERADE</code></pre>

  <h2>📡 4. DNS Deep Dive</h2>
  <p>The Domain Name System (DNS) translates human-readable domain names to IP addresses.</p>
  <ul>
    <li><strong>A Record:</strong> Maps domain to IPv4</li>
    <li><strong>AAAA Record:</strong> Maps domain to IPv6</li>
    <li><strong>CNAME:</strong> Alias to another domain</li>
    <li><strong>MX:</strong> Mail server records</li>
  </ul>
  <pre><code># Query DNS records
dig example.com
dig +short A google.com
host example.com
nslookup example.com</code></pre>

  <h2>🌍 5. Public vs Private IPs</h2>
  <p>Private IPs are used inside networks; public IPs are routable on the internet.</p>
  <ul>
    <li>Private ranges:
      <ul>
        <li>10.0.0.0 – 10.255.255.255</li>
        <li>172.16.0.0 – 172.31.255.255</li>
        <li>192.168.0.0 – 192.168.255.255</li>
      </ul>
    </li>
    <li>Public IPs are allocated by ISPs and are unique globally.</li>
  </ul>

  <h2>📂 6. Useful Network Config Files (Linux)</h2>
  <ul>
    <li><code>/etc/hosts</code> – Manual DNS resolution</li>
    <li><code>/etc/resolv.conf</code> – DNS server config</li>
    <li><code>/etc/network/interfaces</code> – Interface settings (Debian)</li>
    <li><code>/etc/netplan/*.yaml</code> – Netplan configs (Ubuntu)</li>
  </ul>

  <h2>🔎 7. Common Troubleshooting Tools</h2>
  <ul>
    <li><code>ping</code> – Test network reachability</li>
    <li><code>traceroute</code> – Display route to host</li>
    <li><code>ip a</code> – Show network interfaces and IPs</li>
    <li><code>netstat / ss</code> – View socket connections</li>
    <li><code>tcpdump</code> – Packet sniffer</li>
  </ul>

  <h2>💡 Light DevOps Relevance</h2>
  <p>DevOps professionals benefit from understanding:</p>
  <ul>
    <li>Routing and DNS for service exposure</li>
    <li>NAT and firewall rules for infrastructure security</li>
    <li>Subnetting for VPC/VNet planning in the cloud</li>
  </ul>

  <h2>📘 Summary</h2>
  <ul>
    <li>Routing helps traffic move efficiently across networks.</li>
    <li>Subnetting allows efficient IP allocation.</li>
    <li>NAT bridges internal networks to the internet.</li>
    <li>DNS is essential for user-friendly network access.</li>
  </ul>

  <h2>📍 What’s Next? (Part 4 Preview)</h2>
  <ul>
    <li>Advanced TCP/IP stack behavior</li>
    <li>Firewall concepts (iptables, nftables)</li>
    <li>DHCP, ARP, and ICMP protocols</li>
    <li>IPv6 – the future of addressing</li>
  </ul>

</body>
</html>
