<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  
</head>
<body>

  <h1>📅 Shell Scripting Basics 🚀</h1>
  

  <h2>📜 What I Learned</h2>
  <ul>
    <li>Shell scripts are a series of Linux commands written in a file, executed by the shell (e.g., <code>bash</code>)</li>
    <li>Basic script starts with a shebang line:
      <pre><code>#!/bin/bash</code></pre>
    </li>
    <li>Created and executed a script:
      <pre><code>nano script.sh
chmod +x script.sh
./script.sh</code></pre>
    </li>
    <li>Used variables and printed them:
      <pre><code>name="DevOps Learner"
echo "Hello $name"</code></pre>
    </li>
    <li>Used input and arguments:
      <pre><code>read -p "Enter your name: " user
echo "Welcome $user"</code></pre>
      <pre><code>echo "First argument: $1"</code></pre>
    </li>
    <li>Used conditional statements:
      <pre><code>if [ $user == "admin" ]; then
  echo "Access granted"
else
  echo "Access denied"
fi</code></pre>
    </li>
    <li>Used loops:
      <pre><code>for i in {1..5}
do
  echo "Number $i"
done</code></pre>
    </li>
    <li>Created simple menu using <code>case</code> statement</li>
  </ul>

  <h3>🧠 Key Takeaway:</h3>
  <p>"Shell scripting helps automate tasks, create toolchains, and manage configurations — a must-have for every DevOps engineer."</p>

  <h2>📍 What's Next?</h2>
  <ul>
    <li>Write real-world automation scripts (e.g., backups, user creation)</li>
    <li>Explore functions in shell scripts</li>
    <li>Handle errors and return codes</li>
    <li>Understand environment variables</li>
  </ul>

</body>
</html>
