<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
 
</head>
<body>

  <h1>📅Bash Scripting Part 2 (Advanced Concepts) 🚀</h1>
  

  <h2>🔍 What I Learned</h2>
  <ul>
    <li><strong>Functions with Return Values:</strong>
      <pre><code>add() {
  return $(($1 + $2))
}
add 3 4
echo "Sum: $?"</code></pre>
    </li>

    <li><strong>Local Variables in Functions:</strong>
      <pre><code>greet() {
  local name=$1
  echo "Hello, $name"
}
greet "DevOps"</code></pre>
    </li>

    <li><strong>Using Arrays:</strong>
      <pre><code>arr=("dev" "test" "prod")
echo ${arr[1]}  # Outputs: test</code></pre>
    </li>

    <li><strong>Looping Through Arrays:</strong>
      <pre><code>for env in "${arr[@]}"
do
  echo "Environment: $env"
done</code></pre>
    </li>

    <li><strong>Error Handling and Exit Codes:</strong>
      <pre><code>command_not_found
if [ $? -ne 0 ]; then
  echo "Error occurred"
fi</code></pre>
    </li>

    <li><strong>Using `trap` for Cleanup:</strong>
      <pre><code>trap "echo 'Script interrupted'; exit" INT
while true; do
  sleep 1
done</code></pre>
    </li>

    <li><strong>Redirecting Output and Logging:</strong>
      <pre><code>echo "Starting..." >> script.log
ls /nonexistent 2>> error.log</code></pre>
    </li>

    <li><strong>Reading Files Line by Line:</strong>
      <pre><code>while read line; do
  echo "Line: $line"
done &lt; file.txt</code></pre>
    </li>

    <li><strong>Using `getopts` for Flags:</strong>
      <pre><code>while getopts ":u:p:" opt; do
  case $opt in
    u) user=$OPTARG ;;
    p) pass=$OPTARG ;;
  esac
done</code></pre>
    </li>
  </ul>

  <h3>🧠 Key Takeaway:</h3>
  <p>"Advanced Bash scripting allows you to write robust automation tools, perform system monitoring, and create reusable DevOps workflows."</p>

  <h2>📍 What's Next?</h2>
  <ul>
    <li>Create a full backup script using conditionals, logging, and scheduling</li>
    <li>Use bash in CI/CD pipeline scripts (e.g., Azure DevOps, GitHub Actions)</li>
    <li>Explore JSON parsing using <code>jq</code> in bash scripts</li>
    <li>Master bash script debugging: <code>bash -x script.sh</code></li>
  </ul>

</body>
</html>
