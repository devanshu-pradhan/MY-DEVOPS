<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  
</head>
<body>

  <h1>🌐 Networking Basics – Part 5</h1>
  <p><strong>Focus:</strong> Firewalls, NAT, Network Namespaces, Linux Bridges, and Virtual Interfaces</p>

  <h2>🔐 1. Firewalls (iptables & nftables)</h2>
  <p>Firewalls control inbound/outbound traffic on a system or network based on rules.</p>
  <ul>
    <li><strong>iptables:</strong> Legacy firewall tool for packet filtering.</li>
    <li><strong>nftables:</strong> Modern replacement offering better performance and features.</li>
  </ul>
  <pre><code># Basic iptables command
sudo iptables -L

# Drop all incoming traffic
sudo iptables -P INPUT DROP

# Check nftables status
sudo nft list ruleset</code></pre>

  <h2>🌉 2. Linux Bridges</h2>
  <p>A network bridge connects two or more network segments, allowing communication as if they are one.</p>
  <ul>
    <li>Common in VM/container networking.</li>
    <li>Acts like a virtual switch (layer 2 device).</li>
  </ul>
  <pre><code># List existing bridges
brctl show

# Create a new bridge (example)
sudo brctl addbr br0
sudo ip link set dev br0 up</code></pre>

  <h2>🧱 3. Network Namespaces</h2>
  <p>Network namespaces isolate network resources like IP addresses, routing tables, and interfaces.</p>
  <ul>
    <li>Used heavily in Docker and Kubernetes.</li>
    <li>Each namespace has its own stack and routing.</li>
  </ul>
  <pre><code># Create and enter a namespace
sudo ip netns add devnet
sudo ip netns exec devnet bash

# Delete it
sudo ip netns del devnet</code></pre>

  <h2>🔁 4. NAT (Network Address Translation)</h2>
  <p>NAT maps private IPs to public IPs for internet access.</p>
  <ul>
    <li><strong>SNAT:</strong> Source NAT (for outgoing traffic)</li>
    <li><strong>DNAT:</strong> Destination NAT (for port forwarding)</li>
  </ul>
  <pre><code># Enable NAT via iptables (basic SNAT)
sudo iptables -t nat -A POSTROUTING -o eth0 -j MASQUERADE

# Enable IP forwarding
echo 1 | sudo tee /proc/sys/net/ipv4/ip_forward</code></pre>

  <h2>🖧 5. Virtual Interfaces (veth pairs)</h2>
  <p>Virtual Ethernet (veth) pairs are connected like pipes. Packets sent to one end appear on the other.</p>
  <ul>
    <li>Useful for connecting namespaces or containers to bridges.</li>
  </ul>
  <pre><code># Create veth pair
sudo ip link add veth0 type veth peer name veth1

# Move one end to a namespace
sudo ip netns add ns1
sudo ip link set veth1 netns ns1</code></pre>

  <h2>🧠 Summary</h2>
  <ul>
    <li><strong>iptables/nftables:</strong> Control traffic rules for system/network security.</li>
    <li><strong>Bridges:</strong> Act like virtual switches for interconnecting VMs/containers.</li>
    <li><strong>Namespaces:</strong> Provide full network isolation per container/VM.</li>
    <li><strong>NAT:</strong> Allows multiple devices to share one public IP.</li>
    <li><strong>veth:</strong> Essential for custom virtual networking.</li>
  </ul>

  <h2>📍 What’s Next? (Part 6 Preview)</h2>
  <ul>
    <li>🔍 Deep DNS resolution and caching</li>
    <li>📊 Bandwidth monitoring tools (iftop, iperf, bmon)</li>
    <li>🔧 Troubleshooting tools (tcpdump, netstat, ss)</li>
    <li>🧭 Static & dynamic routing (quagga, bird)</li>
  </ul>

</body>
</html>
