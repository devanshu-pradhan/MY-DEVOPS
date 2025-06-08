<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">

</head>
<body>

  <h1>🌐 Networking Basics – Part 8</h1>
  <p><strong>Focus:</strong> Advanced Routing (OSPF, BGP), Linux Kernel Networking Internals, VPNs & Tunneling, Real-World Design</p>

  <!-- 1. OSPF -->
  <h2>1️⃣ OSPF – Open Shortest Path First</h2>
  <ul>
    <li>Interior Gateway Protocol (IGP) used within an organization.</li>
    <li>Link-state protocol – each router maintains a complete map of the network.</li>
    <li>Uses Dijkstra’s algorithm to calculate shortest paths.</li>
  </ul>
  <pre><code># Example: Configure OSPF using FRRouting
router ospf
 network 10.0.0.0/24 area 0
</code></pre>
  <p><strong>Key Terms:</strong> Area 0 (backbone), LSAs (Link State Advertisements), DR/BDR (election in broadcast networks).</p>

  <!-- 2. BGP -->
  <h2>2️⃣ BGP – Border Gateway Protocol</h2>
  <ul>
    <li>Exterior Gateway Protocol (EGP) used to route between autonomous systems (AS).</li>
    <li>Path-vector protocol – uses AS_PATH to prevent loops.</li>
    <li>Internet backbone protocol.</li>
  </ul>
  <pre><code># Basic BGP config (FRRouting or Cisco-like syntax)
router bgp 64512
 neighbor 192.0.2.1 remote-as 64513
 network 203.0.113.0/24</code></pre>
  <p><strong>Key Concepts:</strong> iBGP vs eBGP, route maps, communities, prefix filtering.</p>

  <!-- 3. Linux Kernel Networking Internals -->
  <h2>3️⃣ Linux Kernel Networking Internals</h2>
  <ul>
    <li>Linux has a full network stack built into the kernel.</li>
    <li><strong>Netfilter</strong> (iptables/nftables) used for packet filtering.</li>
    <li><strong>Routing tables</strong> can be viewed/modified using <code>ip route</code>.</li>
    <li>Uses <strong>network namespaces</strong> for container-level isolation.</li>
  </ul>
  <pre><code># Show all routing tables
ip route show

# Create a network namespace and assign a veth pair
ip netns add testns
ip link add veth0 type veth peer name veth1
ip link set veth1 netns testns</code></pre>

  <!-- 4. VPNs & Tunneling -->
  <h2>4️⃣ VPNs & Tunneling Concepts</h2>
  <ul>
    <li><strong>VPN:</strong> Creates secure, encrypted connections over public networks.</li>
    <li><strong>Tunneling:</strong> Encapsulates one protocol inside another (e.g., GRE, IP-in-IP).</li>
    <li>Common VPN tools: <strong>OpenVPN, WireGuard, IPsec</strong>.</li>
  </ul>
  <pre><code># Show active WireGuard interface
sudo wg show

# Set up IPsec VPN using strongSwan or Libreswan (not shown here due to length)</code></pre>
  <p><strong>Use Case:</strong> Site-to-site VPN, remote access VPNs, hybrid cloud tunnels.</p>

  <!-- 5. Real-World Network Design -->
  <h2>5️⃣ Real-World Network Design Examples</h2>
  <h3>🏢 Enterprise LAN (Layer 2/3)</h3>
  <ul>
    <li>Core → Distribution → Access Layer Model.</li>
    <li>Use VLANs to separate traffic (e.g., HR, Dev, Guests).</li>
    <li>Use ACLs & firewalls at boundaries.</li>
  </ul>

  <h3>☁️ Data Center / Cloud</h3>
  <ul>
    <li>Overlay networks (VXLAN) for tenant isolation.</li>
    <li>Load balancers (L4/L7) for traffic distribution.</li>
    <li>East-West (intra-DC) and North-South (internet-facing) traffic patterns.</li>
  </ul>

  <h3>🌍 ISP or Multi-Site Design</h3>
  <ul>
    <li>BGP used between sites or with cloud providers.</li>
    <li>Route redistribution between OSPF & BGP (if needed).</li>
    <li>High availability via failover links, VRRP, or BFD.</li>
  </ul>

  <!-- Summary -->
  <h2>🧠 Summary</h2>
  <ul>
    <li><strong>OSPF</strong> = link-state, fast convergence, internal routing.</li>
    <li><strong>BGP</strong> = Internet-scale routing, path-based decisions.</li>
    <li><strong>Linux Kernel</strong> handles advanced routing, namespaces, and packet filtering.</li>
    <li><strong>VPNs</strong> secure communication using encryption & tunneling.</li>
    <li><strong>Designs</strong> must balance performance, isolation, and scalability.</li>
  </ul>

  <h2>📍 What’s Next? (Part 9 Preview)</h2>
  <ul>
    <li>🔒 Network Security Best Practices (firewalls, IDS/IPS)</li>
    <li>🧪 Protocol Deep Dives (ARP, DHCP, ICMP, NAT)</li>
    <li>📶 Wireless Networking Concepts (2.4GHz vs 5GHz, channels, WPA)</li>
    <li>🧠 Interview-level Networking Scenarios</li>
  </ul>

</body>
</html>
