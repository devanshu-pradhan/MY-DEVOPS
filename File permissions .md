<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
 
</head>
<body>

  <h1>📅 File permissions and process management 🚀</h1>
  <p><strong>Topic:</strong> <em>File Permissions & Process Management</em></p>

  <div class="section">
    <h2>🔐 File Permissions</h2>
    <ul>
      <li>Understood permission types: <strong>read (r), write (w), execute (x)</strong></li>
      <li>Explored permission levels: <strong>Owner, Group, Others</strong></li>
      <li>Learned how to read symbolic and octal notations like <code>-rwxr-xr--</code> and <code>755</code></li>
      <li>Used <code>chmod</code> to modify permissions:
        <ul>
          <li><code>chmod 755 filename</code></li>
          <li><code>chmod +x script.sh</code></li>
        </ul>
      </li>
      <li>Used <code>chown</code> to change file ownership:
        <ul>
          <li><code>chown user:group file</code></li>
        </ul>
      </li>
    </ul>
  </div>

  <div class="section">
    <h2>⚙️ Process Management</h2>
    <ul>
      <li>Viewed running processes using <code>ps aux</code> and <code>top</code></li>
      <li>Monitored resource usage: CPU%, MEM%, PID</li>
      <li>Filtered process info with <code>grep</code>:
        <ul>
          <li><code>ps aux | grep nginx</code></li>
        </ul>
      </li>
      <li>Terminated processes using:
        <ul>
          <li><code>kill &lt;PID&gt;</code></li>
          <li><code>kill -9 &lt;PID&gt;</code> (force kill)</li>
        </ul>
      </li>
      <li>Explored <code>nice</code> and <code>renice</code> to manage process priority</li>
    </ul>
  </div>

  <div class="section highlight">
    <strong>🧠 Key Takeaway:</strong><br />
    "Mastering file permissions and process control is vital for system security, resource efficiency, and DevOps automation."
  </div>

  <div class="section next">
    <h2>📍 What's Next?</h2>
    <ul>
      <li>Learn Service Management using <code>systemctl</code></li>
      <li>Practice <strong>cron jobs</strong> and task scheduling</li>
      <li>Begin <strong>Bash scripting</strong> to automate tasks</li>
    </ul>
  </div>

</body>
</html>
