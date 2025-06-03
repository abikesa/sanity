<h2>🧠 Ukubona Intern Setup Guide (Mac)</h2>
<blockquote><em>“From zero to <code>git push</code> in 10 minutes.”</em></blockquote>

<details open>
  <summary>🚨 TL;DR — Git on Mac = Xcode Bottleneck</summary>
  <p>Git on Mac is crippled out-of-the-box. It’s <em>not standalone</em>. It lives <strong>inside</strong> Apple’s <strong>Command Line Tools (CLT)</strong>—installed via:</p>
  <pre><code>xcode-select --install</code></pre>
  <p>This is the <strong>first and worst</strong> bottleneck:</p>
  <ul>
    <li>No progress bar.</li>
    <li>No ETA.</li>
    <li>No escape if the popup breaks.</li>
  </ul>
  <p>👉 <strong>Don’t wait. Don’t wonder. Skip Apple.</strong></p>
</details>

<details>
  <summary>✅ Fastest Path: Homebrew Git (Bypass Apple)</summary>
  <pre><code>/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
brew install git</code></pre>
  <p>Now check:</p>
  <pre><code>git --version
which git  # should point to /opt/homebrew/bin/git</code></pre>
  <p>If you still see <code>/usr/bin/git</code>, you're stuck on the Apple leash.</p>
</details>

<details>
  <summary>💻 VS Code Setup (Intern Blitz – 10 min)</summary>
  <h4>1. Install VS Code</h4>
  <ul>
    <li><a href="https://code.visualstudio.com" target="_blank">code.visualstudio.com</a></li>
    <li>Drag to Applications</li>
  </ul>

  <h4>2. Launch & Configure</h4>
  <ul>
    <li>Open VS Code → allow system prompts.</li>
    <li>Go to Extensions and install:
      <ul>
        <li>✅ Python</li>
        <li>✅ Prettier</li>
        <li>✅ GitHub Copilot (optional)</li>
      </ul>
    </li>
  </ul>

  <h4>3. Create Folder + Test File</h4>
  <pre><code>mkdir ~/Desktop/intern-project
cd ~/Desktop/intern-project
code .</code></pre>
  <p>Inside VS Code:</p>
  <ul>
    <li>Create <code>test.py</code></li>
    <li>Add:</li>
  </ul>
  <pre><code>print("Hello, Ukubona!")</code></pre>
  <p>Run ▶️ (install interpreter if prompted)</p>
</details>

<details>
  <summary>🚀 Git Push Workflow (From Local → GitHub)</summary>
  <h4>❓ Ask First</h4>
  <p><strong>“Do you have a GitHub account?”</strong><br>If not: <a href="https://github.com" target="_blank">github.com</a> → signup + verify email.</p>

  <h4>🔧 Terminal Setup</h4>
  <pre><code>git config --global user.name "Jonathan Gasaatura"
git config --global user.email "jonathan@example.com"</code></pre>

  <h4>Create a repo on GitHub</h4>
  <ul>
    <li>Go to GitHub → <code>+</code> → New repository</li>
    <li>Public, no README, click Create</li>
  </ul>

  <h4>Then in Terminal:</h4>
  <pre><code>cd ~/Desktop/intern-project
git init
git add index.html
git commit -m "First commit"
git remote add origin https://github.com/USERNAME/intern-project.git
git branch -M main
git push -u origin main</code></pre>
  <p>🎉 Refresh GitHub → <code>index.html</code> is live.</p>
</details>

<details>
  <summary>🧪 Bonus: Sanity Check for Git + Python</summary>
  <pre><code>git --version
which git         # Good = /opt/homebrew/bin/git
python3 --version # Should not be 2.x
which python3</code></pre>
</details>

<details>
  <summary>🧱 Optional Add-Ons</summary>
  <ul>
    <li><strong>Install Python</strong> via Homebrew:</li>
  </ul>
  <pre><code>brew install python</code></pre>
  <ul>
    <li><strong>Create virtual environments:</strong></li>
  </ul>
  <pre><code>python3 -m venv myenv
source myenv/bin/activate</code></pre>
</details>

<blockquote><strong>🧭 Ukubona Philosophy</strong><br>
“Every world-changing tool starts in an empty folder. You own the soil. Now grow something.”</blockquote>
# flick 20250530024814-sb1K
# flick 20250602214626-oOiS
# flick 20250603004037-cc4J
