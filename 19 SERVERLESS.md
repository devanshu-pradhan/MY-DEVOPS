<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  
</head>
<body>

  <h1>⚡ Serverless Computing</h1>
  <p><strong>Focus:</strong> What is Serverless, Key Features, FaaS, Benefits, DevOps Impact, and Real-world Use Cases</p>

  <!-- 1. What is Serverless -->
  <h2>1️⃣ What is Serverless?</h2>
  <p>Serverless computing is a cloud computing model where the cloud provider manages the infrastructure, and developers only focus on writing code. You don’t manage servers — you just deploy functions.</p>

  <!-- 2. Key Concepts -->
  <h2>2️⃣ Key Concepts</h2>
  <ul>
    <li><strong>FaaS (Function-as-a-Service):</strong> Deploy small units of logic (functions) that run on demand.</li>
    <li><strong>Event-driven:</strong> Functions are triggered by events (HTTP request, file upload, DB change).</li>
    <li><strong>No server management:</strong> Cloud provider handles auto-scaling, updates, availability.</li>
    <li><strong>Pay-as-you-go:</strong> You are charged only when the function runs.</li>
  </ul>

  <!-- 3. Popular Serverless Platforms -->
  <h2>3️⃣ Popular Serverless Platforms</h2>
  <ul>
    <li>🔹 <strong>AWS Lambda</strong></li>
    <li>🔹 <strong>Azure Functions</strong></li>
    <li>🔹 <strong>Google Cloud Functions</strong></li>
    <li>🔹 <strong>Netlify Functions / Vercel</strong></li>
  </ul>

  <!-- 4. Example: AWS Lambda Function -->
  <h2>4️⃣ Example: AWS Lambda (Node.js)</h2>
  <pre><code>exports.handler = async (event) => {
  return {
    statusCode: 200,
    body: JSON.stringify({ message: "Hello from Lambda!" }),
  };
};</code></pre>

  <!-- 5. Serverless vs Traditional -->
  <h2>5️⃣ Serverless vs Traditional Architecture</h2>
  <table border="1" cellpadding="5">
    <tr>
      <th>Feature</th>
      <th>Serverless</th>
      <th>Traditional Server</th>
    </tr>
    <tr>
      <td>Infrastructure</td>
      <td>Managed by provider</td>
      <td>Managed by you</td>
    </tr>
    <tr>
      <td>Cost Model</td>
      <td>Pay per invocation</td>
      <td>Pay for uptime</td>
    </tr>
    <tr>
      <td>Scaling</td>
      <td>Auto-scaled</td>
      <td>Manual or auto with setup</td>
    </tr>
    <tr>
      <td>Use Case</td>
      <td>Microservices, APIs, Automation</td>
      <td>Monolithic apps, Stateful services</td>
    </tr>
  </table>

  <!-- 6. Benefits -->
  <h2>6️⃣ Benefits of Serverless</h2>
  <ul>
    <li>🚫 No server maintenance</li>
    <li>⚡ Fast deployments and iterations</li>
    <li>📉 Reduced costs for low-traffic services</li>
    <li>📈 Automatically scales up/down</li>
    <li>🧩 Ideal for event-driven architectures</li>
  </ul>

  <!-- 7. Serverless in DevOps -->
  <h2>7️⃣ Relevance to DevOps</h2>
  <ul>
    <li>🎯 Enables quicker deployments with CI/CD pipelines</li>
    <li>🔄 Supports microservices & modular architecture</li>
    <li>📦 Reduces infrastructure overhead for ops teams</li>
    <li>🛠️ Integrates with cloud-native tools (APIs, DBs, queues)</li>
  </ul>

  <!-- 8. Use Cases -->
  <h2>8️⃣ Real-world Use Cases</h2>
  <ul>
    <li>🔔 Notification services</li>
    <li>🧪 Test automation triggers</li>
    <li>🌐 REST APIs</li>
    <li>🧹 Background jobs (e.g., image resizing, log cleanup)</li>
    <li>💳 Payment webhook handlers</li>
  </ul>

  <!-- 9. Limitations -->
  <h2>9️⃣ Limitations</h2>
  <ul>
    <li>⏳ Execution timeout limits</li>
    <li>📁 Cold starts can affect latency</li>
    <li>🧠 Complexity in debugging and monitoring</li>
    <li>🔐 Vendor lock-in risks</li>
  </ul>

  <!-- 10. What's Next? -->
  <h2>📍 What's Next?</h2>
  <ul>
    <li>🧪 Create your first AWS Lambda or Azure Function</li>
    <li>🔄 Learn how to automate serverless deployment with CI/CD tools</li>
    <li>🔐 Explore serverless security best practices</li>
    <li>⚙️ Use serverless for API backend + frontend (e.g., S3 + Lambda + API Gateway)</li>
  </ul>

</body>
</html>
