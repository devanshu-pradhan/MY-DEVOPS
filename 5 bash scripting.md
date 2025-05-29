<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">

</head>
<body>

  <h1>📅Bash Scripting Basics🚀</h1>
  

  <h2>🔍 What I Learned</h2>
  <ul>
    <li><strong>Bash</strong> is a powerful scripting shell used in most Linux systems for automation.</li>
    <li>Started every bash script with a shebang:
      <pre><code>#!/bin/bash</code></pre>
    </li>
    <li>Created and executed basic bash script:
      <pre><code>nano myscript.sh
chmod +x myscript.sh
./myscript.sh</code></pre>
    </li>
    <li>Declared variables and printed them:
      <pre><code>name="DevOps"
echo "Hello, $name"</code></pre>
    </li>
    <li>Captured user input:
      <pre><code>read -p "Enter your name: " user
echo "Welcome $user"</code></pre>
    </li>
    <li>Handled command-line arguments:
      <pre><code>echo "Script name: $0"
echo "First arg: $1"</code></pre>
    </li>
    <li>Wrote conditionals:
      <pre><code>if [ "$user" == "admin" ]; then
  echo "Hello Admin"
else
  echo "Access Denied"
fi</code></pre>
    </li>
    <li>Used loops (for, while):
      <pre><code>for i in 1 2 3
do
  echo "Iteration $i"
done</code></pre>
    </li>
    <li>Created and used functions:
      <pre><code>greet() {
  echo "Hello, $1"
}
greet "DevOps"</code></pre>
    </li>
    <li>Checked exit status using <code>$?</code> and used <code>exit</code> command</li>
  </ul>

  <h3>🧠 Key Takeaway:</h3>
  <p>"Bash scripting helps automate Linux tasks, system configurations, CI/CD workflows — making it a core DevOps skill."</p>

  <h2>📍 What's Next?</h2>
  <ul>
    <li>Practice writing bash functions and modular scripts</li>
    <li>Learn error handling, logs, and status codes</li>
    <li>Create real DevOps scripts (system monitoring, backup, setup)</li>
  </ul>

</body>
</html>
