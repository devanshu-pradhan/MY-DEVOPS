<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  
</head>
<body>

  <h1>📦 Containers – The Backbone of Modern DevOps</h1>
  <p><strong>Focus:</strong> What are containers, how they work, Docker intro, benefits, DevOps usage</p>

  <!-- 1. What is a Container -->
  <h2>1️⃣ What is a Container?</h2>
  <p>A container is a lightweight, standalone, and executable software package that includes everything needed to run a piece of software: code, runtime, libraries, and settings. It shares the host OS kernel but runs in isolated user spaces.</p>

  <!-- 2. Key Features -->
  <h2>2️⃣ Key Features</h2>
  <ul>
    <li>🚀 Fast startup time</li>
    <li>📦 Lightweight (no full OS inside)</li>
    <li>🔐 Isolated and secure</li>
    <li>🛠️ Portable across environments (dev, test, prod)</li>
    <li>⛓️ Uses OS-level virtualization</li>
  </ul>

  <!-- 3. Containers vs Virtual Machines -->
  <h2>3️⃣ Containers vs Virtual Machines</h2>
  <table border="1" cellpadding="5">
    <tr>
      <th>Aspect</th>
      <th>Containers</th>
      <th>Virtual Machines</th>
    </tr>
    <tr>
      <td>Boot Time</td>
      <td>Seconds</td>
      <td>Minutes</td>
    </tr>
    <tr>
      <td>Resource Usage</td>
      <td>Low</td>
      <td>High</td>
    </tr>
    <tr>
      <td>Isolation Level</td>
      <td>Process-level</td>
      <td>Hardware-level</td>
    </tr>
    <tr>
      <td>Use Case</td>
      <td>Microservices, CI/CD</td>
      <td>Legacy Apps, Full OS</td>
    </tr>
  </table>

  <!-- 4. Docker Basics -->
  <h2>4️⃣ Docker – The Popular Container Engine</h2>
  <ul>
    <li>Docker is a containerization platform used to build, ship, and run containers.</li>
    <li>Images are blueprints of containers.</li>
    <li>Containers are instances of Docker images.</li>
  </ul>
  <pre><code># Check Docker version
docker --version

# Run a container
docker run hello-world

# List running containers
docker ps

# Build an image
docker build -t myapp .

# Run an interactive container
docker run -it ubuntu bash</code></pre>

  <!-- 5. Benefits in DevOps -->
  <h2>5️⃣ Why Containers Are Important in DevOps</h2>
  <ul>
    <li>🔁 Consistency across dev, staging, and prod</li>
    <li>⚡ Faster deployment and rollback</li>
    <li>🔬 Easy to scale microservices</li>
    <li>📦 Simplifies CI/CD pipelines</li>
    <li>🛠️ Works well with Kubernetes, Jenkins, GitHub Actions</li>
  </ul>

  <!-- 6. Container Registries -->
  <h2>6️⃣ Container Registries</h2>
  <ul>
    <li><strong>Docker Hub:</strong> Default public registry</li>
    <li><strong>Azure Container Registry (ACR)</strong></li>
    <li><strong>Amazon ECR, GitHub Container Registry</strong></li>
  </ul>
  <pre><code># Push image to Docker Hub
docker tag myapp username/myapp
docker push username/myapp</code></pre>

  <!-- 7. Summary -->
  <h2>🧠 Summary</h2>
  <ul>
    <li>Containers isolate apps with minimal overhead</li>
    <li>They are faster and lighter than VMs</li>
    <li>Docker is the most used container runtime</li>
    <li>DevOps relies heavily on containers for automation, testing, and delivery</li>
  </ul>

  <!-- 8. What's Next -->
  <h2>📍 What's Next?</h2>
  <ul>
    <li>🎓 Learn how to write Dockerfiles</li>
    <li>🌐 Understand container networking</li>
    <li>⚙️ Start using Kubernetes for container orchestration</li>
    <li>🔒 Explore container security and scanning tools (e.g., Trivy)</li>
  </ul>

</body>
</html>
