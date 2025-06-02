# 🧠 Memory & Process Forensics Lab

This repository contains tools, labs, and techniques for analyzing live Linux systems and memory captures. It focuses on understanding how processes behave at a low level, how attackers may attempt to hide, and how defenders can spot forensic clues left behind.

This isn’t about reading a dashboard — it’s about **dissecting systems from the inside out**.

## 🎯 Why This Repo Exists

Most incident responders stop at surface logs. But attackers know how to:

- Leave no shell history
- Run binaries from memory
- Unlink files after execution
- Hide in plain sight using renamed or orphaned processes

This lab is designed to expose these behaviors and build hands-on intuition for **memory and process-level forensics**.

## 📂 Folder Structure

| Folder               | Description |
|----------------------|-------------|
| `proc-analysis/`     | Manual walkthroughs of `/proc`, mapping PIDs to behavior |
| `live-tools/`        | Demos using `ps`, `lsof`, `top`, `netstat`, `fuser`, etc. |
| `deleted-binaries/`  | Scenarios involving unlinked or hidden executables |
| `rootkit-hunting/`   | Common detection heuristics, e.g. `readdir()` hook checks |
| `volatility-labs/`   | Sample memory dumps, plugins, and analysis with Volatility |
| `memory-capture/`    | Tools and steps for safe memory capture (LiME, fmem, etc.) |
| `case-studies/`      | Real-world or simulated IR examples showing analysis flow |
| `cheatsheets/`       | One-liners and triage workflows for live response |
| `docs/`              | Conceptual writeups on memory layout, hidden process behavior, etc. |

## 🔍 Techniques Covered

- Using `/proc/<pid>/maps`, `cwd`, `exe`, and `fd/` to trace execution
- Finding deleted-but-running binaries
- Investigating suspicious parent-child process trees
- Identifying signs of rootkits (e.g. missing `ps` entries)
- Memory snapshot triage using **Volatility 2 & 3**
- Detection heuristics for in-memory execution, reflective loaders, etc.

## ⚒️ Tools You’ll See

- `lsof`, `fuser`, `ss`, `ps`, `top`, `htop`
- `strings`, `binwalk`, `gdb`
- `LiME`, `Volatility`, `vol.py`, `memdump`
- Kernel module analysis basics (optional)

## 👥 Who Should Use This

- SOC Analysts learning deeper triage methods
- IR professionals needing live forensics skills
- Blue teamers upskilling against evasive malware
- Students or career switchers looking to level up from log-only workflows

## 🧠 Philosophy

True forensic skill means going beyond what the attacker expects you to check.

This repo is designed to build:
- Deeper **observation habits**
- Pattern recognition of suspicious behavior
- Comfort with live triage *and* dead memory dumps

## 🛑 Legal Reminder

All memory captures and experiments must be done in **controlled, legal lab environments**. Never acquire or analyze memory from systems you don’t own or have explicit permission to test.

