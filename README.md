<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>SRTF CPU Scheduling Visualizer & Calculator README</title>
    <style>
        /* Basic styling for readability, common in markdown viewers */
        body { font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif; line-height: 1.6; max-width: 800px; margin: 0 auto; padding: 20px; }
        h1 { border-bottom: 2px solid #eee; padding-bottom: 10px; }
        h2 { border-bottom: 1px solid #eee; padding-bottom: 5px; margin-top: 30px; }
        pre, code { background-color: #f6f8fa; padding: 2px 4px; border-radius: 4px; font-family: "SF Mono", Consolas, "Liberation Mono", Menlo, Courier, monospace; overflow-x: auto; }
        pre { padding: 16px; margin: 15px 0; }
        ul, ol { padding-left: 20px; }
        .feature-list li { margin-bottom: 10px; }
    </style>
</head>
<body>

    <h1>🚀 SRTF CPU Scheduling Visualizer & Calculator</h1>

    <p>This project is a dynamic, browser-based tool designed to help students and developers visualize and calculate the results of the <strong>Shortest Remaining Time First (SRTF)</strong> preemptive CPU scheduling algorithm.</p>

    <hr>

    <h2>🌟 Key Features</h2>
    <ul class="feature-list">
        <li><strong>Interactive Calculator:</strong> Input custom process details (Name, Arrival Time, Burst Time) to run a live simulation.</li>
        <li><strong>Gantt Chart Visualization:</strong> Generates a clear, color-coded Gantt chart showing process execution over time, including preemption and context switches.</li>
        <li><strong>Comprehensive Metrics:</strong> Calculates and displays individual and average performance statistics:
            <ul>
                <li><strong>Turnaround Time (TAT)</strong></li>
                <li><strong>Waiting Time (WT)</strong></li>
                <li><strong>Response Time (RT)</strong></li>
                <li><strong>Completion Time (CT)</strong></li>
            </ul>
        </li>
        <li><strong>Theory Section:</strong> Includes a dedicated page explaining the SRTF algorithm, its steps, and its advantages/disadvantages.</li>
        <li><strong>Modern Design:</strong> Built with pure HTML/CSS/JavaScript, featuring a modern, responsive, and dark-mode friendly UI.</li>
    </ul>

    <hr>

    <h2>⚙️ How to Use</h2>

    <p>Since this is a simple front-end web application, deployment is straightforward.</p>

    <h3>1. Quick Start (Recommended)</h3>
    <ol>
        <li><strong>Clone the repository:</strong>
            <pre><code>git clone https://github.com/YashBhadange2006/SRTF-Algo.git</code></pre>
        </li>
        <li><strong>Navigate to the project folder:</strong>
            <pre><code>cd SRTF-Algo</code></pre>
        </li>
        <li><strong>Open the file:</strong> Simply open the <code>index.html</code> file in your web browser (e.g., Chrome, Firefox).</li>
    </ol>

    <h3>2. Using the Calculator</h3>
    <ol>
        <li>Switch to the <strong>Calculator</strong> tab in the navigation bar.</li>
        <li>Enter the required details (e.g., <code>P1</code>, Arrival Time <code>0</code>, Burst Time <code>8</code>).</li>
        <li>Click the <strong><code>➕ Add Process</code></strong> button.</li>
        <li>Repeat for all your processes.</li>
        <li>Click the <strong><code>⚡ Calculate SRTF</code></strong> button to generate the Gantt chart and results table.</li>
    </ol>

    <hr>

    <h2>💻 Algorithm Implementation Details</h2>

    <p>The core scheduling logic is implemented in the <code>calculateSRTF()</code> JavaScript function. It follows the principles of preemptive scheduling:</p>
    <ul>
        <li><strong>Iterative Time:</strong> The simulation runs in a <strong>time-stepping loop</strong> (<code>currentTime++</code>) until all processes are complete.</li>
        <li><strong>Preemption Check:</strong> At every time unit, the scheduler checks all <strong>arrived</strong> processes with remaining work.</li>
        <li><strong>Selection:</strong> It selects the process with the <strong>absolute minimum remaining time</strong> (<code>remainingTime</code>), instantly preempting the running process if a new process has a shorter remaining time.</li>
        <li><strong>Metric Calculation:</strong> Metrics like <strong>Turnaround Time</strong> and <strong>Waiting Time</strong> are calculated precisely when a process's <code>remainingTime</code> hits zero (i.e., when it completes).</li>
    </ul>

    <hr>

    <h2>🛠️ Technologies Used</h2>
    <ul>
        <li><strong>HTML5</strong> (Structure)</li>
        <li><strong>CSS3</strong> (Styling and Responsive Design)</li>
        <li><strong>JavaScript (ES6+)</strong> (SRTF Algorithm logic and DOM manipulation)</li>
    </ul>

    <hr>

    <h2>🤝 Contributing</h2>

    <p>Contributions are welcome! If you find a bug or have an idea for an enhancement (e.g., adding another scheduling algorithm like Round Robin or FCFS), please feel free to:</p>
    <ol>
        <li><strong>Fork</strong> the repository.</li>
        <li>Create a new branch (<code>git checkout -b feature/awesome-feature</code>).</li>
        <li>Commit your changes (<code>git commit -m 'feat: added awesome feature'</code>).</li>
        <li>Push to the branch (<code>git push origin feature/awesome-feature</code>).</li>
        <li>Open a <strong>Pull Request</strong>.</li>
    </ol>

    <hr>

    <h2>📝 License</h2>
    <p>This project is licensed under the <strong>MIT License</strong>. See the <code>LICENSE</code> file for details.</p>

    <hr>

    <h2>👤 Author</h2>
    <p><strong>Yash Bhadange</strong> - <a href="YOUR_GITHUB_PROFILE_LINK">GitHub Profile Link</a></p>

</body>
</html>
