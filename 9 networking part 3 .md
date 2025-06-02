<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
</head>
<body>

  <h1>📅Networking Basics Part 3 🚀</h1>

  <h2>☁️ Cloud Networking Concepts</h2>

  <h3>1️⃣ VPC (Virtual Private Cloud)</h3>
  <p>A logically isolated section of the cloud where you can launch resources in a virtual network.</p>
  <ul>
    <li><strong>Subnets:</strong> Divide VPC into public/private zones</li>
    <li><strong>Route Tables:</strong> Define how traffic flows between subnets and the internet</li>
    <li><strong>Internet Gateway:</strong> Allows public internet access</li>
    <li><strong>NAT Gateway:</strong> Allows private subnet instances to access the internet</li>
  </ul>

  <h3>2️⃣ Network Security Groups (NSGs)</h3>
  <p>Firewall rules in cloud platforms (like Azure/AWS) that control inbound and outbound traffic to network interfaces, VMs, or subnets.</p>
  <pre><code># Example NSG rule:
Allow Inbound
Protocol: TCP
Port: 22
Source: My IP
</code></pre>

  <h3>3️⃣ Peering and VPN</h3>
  <ul>
    <li><strong>VPC Peering:</strong> Connect two VPCs for private communication</li>
    <li><strong>VPN Gateway:</strong> Connect on-premise network to cloud securely</li>
    <li><strong>ExpressRoute (Azure):</strong> Dedicated high-speed connection</li>
  </ul>

  <h2>☸️ Kubernetes Networking</h2>

  <h3>4️⃣ Pod Networking</h3>
  <p>Each pod gets its own IP. CNI (Container Network Interface) plugins manage network configuration.</p>
  <ul>
    <li><strong>Common CNI plugins:</strong> Flannel, Calico, Cilium</li>
    <li><strong>Flat network:</strong> Pods can communicate across nodes without NAT</li>
  </ul>

  <h3>5️⃣ Services in Kubernetes</h3>
  <ul>
    <li><strong>ClusterIP:</strong> Default. Internal communication within the cluster</li>
    <li><strong>NodePort:</strong> Exposes service on static port on each node</li>
    <li><strong>LoadBalancer:</strong> Provisioned by cloud provider for external traffic</li>
  </ul>

  <h3>6️⃣ Ingress & Ingress Controllers</h3>
  <p>Provides routing rules and SSL termination for HTTP/S traffic into Kubernetes.</p>
  <pre><code>apiVersion: networking.k8s.io/v1
kind: Ingress
metadata:
  name: app-ingress
spec:
  rules:
  - host: myapp.example.com
    http:
      paths:
      - path: /
        pathType: Prefix
        backend:
          service:
            name: my-service
            port:
              number: 80
</code></pre>

  <h3>7️⃣ Network Policies</h3>
  <p>Controls communication between pods. Like firewalls for Kubernetes pods.</p>
  <pre><code>kind: NetworkPolicy
apiVersion: networking.k8s.io/v1
metadata:
  name: deny-all
spec:
  podSelector: {}
  policyTypes:
  - Ingress
  - Egress
</code></pre>

  <h2>🔄 GitOps and CI/CD Networking</h2>

  <h3>8️⃣ Webhooks and Git Connectivity</h3>
  <p>Ensure your CI/CD tools (e.g., GitHub Actions, Jenkins) can securely access:
    <ul>
      <li>Source code via HTTPS or SSH</li>
      <li>Webhooks from GitHub/GitLab for triggering builds</li>
    </ul>
  </p>

  <h3>9️⃣ Firewall Rules for CI/CD Agents</h3>
  <p>Open only required ports:
    <ul>
      <li>22 for SSH</li>
      <li>443 for API/webhook access</li>
    </ul>
  </p>

  <h3>🔐 10. Zero Trust Networking</h3>
  <ul>
    <li>Never trust, always verify</li>
    <li>Use identity-aware proxies and authentication layers</li>
    <li>Control access by user identity, not just IP</li>
  </ul>

  <h2>🧠 Summary</h2>
  <ul>
    <li>Cloud networking relies on isolation, routing, and security via VPCs and subnets</li>
    <li>Kubernetes networking enables dynamic service discovery, ingress control, and policy enforcement</li>
    <li>CI/CD pipelines require secure access to Git systems and proper firewall configurations</li>
  </ul>

  <h2>📍 What’s Next?</h2>
  <ul>
    <li>🔐 Dive into Service Mesh (Istio/Linkerd)</li>
    <li>🌐 DNS & TLS automation with Cert-Manager in Kubernetes</li>
    <li>📈 Monitor traffic with Prometheus + Grafana</li>
    <li>🧪 Simulate attacks with tools like Chaos Mesh</li>
  </ul>

</body>
</html>
