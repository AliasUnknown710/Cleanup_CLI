## 🧼 Cleanup_CLI


A cross-platform CLI tool for automated system cleanup using config-driven path targeting.


No hardcoded paths.


No toy examples.


Just actionable cleanup.


---


| Script       | Description                                         |
|--------------|-----------------------------------------------------|
| cleanup.py   | Deletes temp files and folders based on OS config.  |
| config.json  | Defines cleanup targets for Windows, Linux, macOS.  |
| README.md    | You're reading it.                                  |


---


## 🧠 Why This Script Matters


  This repo showcases practical automation for:


  ✅ Cross-platform system cleanup


  🔧 Config-driven path targeting


  🧩 Real-world error handling and output


  🪶 Minimal, extensible CLI logic


  Built for maintainability and portability. No brittle configs. No fluff.


---


## ⚙️ How It Works


  🧠 Detects OS via platform.system()


  📂 Loads cleanup targets from config.json


  🧹 Deletes files and folders with status output


  🚫 Skips missing paths and handles exceptions gracefully


---


## 🛠️ Supported Platforms


  🪟 Windows


  🐧 Linux


  🍎 macOS


---


## 🚀 Usage


# Run cleanup with default config


   python cleanup.py
   

# Dry run (preview deletions)


  python cleanup.py --dry-run


# Verbose output

 
  python cleanup.py --verbose


---


## 📊 Logging Output


  Each deletion is logged with status:


    [✔] Deleted: /tmp/cache


    [✘] Skipped (not found): /var/log/old_logs


    [⚠] Error: Permission denied on /System/Temp


---


## ⏰ Cron Integration (Linux/macOS)


  Add to crontab for scheduled cleanup:


# Run every Sunday at 2am


  0 2 * * 0 /usr/bin/python3 /path/to/cleanup.py >> /var/log/cleanup.log 2>&1


---


## 🗓️ Task Scheduler (Windows)


  Use Task Scheduler to run cleanup.py weekly:


  Trigger: Weekly


  Action: python.exe


  Arguments: C:\path\to\cleanup.py


  Optional: Redirect output to cleanup.log

