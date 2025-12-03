📡 Live Network Monitoring System using Python

This project provides a real-time network monitoring tool that tracks latency, packet loss, and network speed with live updated graphs. It triggers alerts when thresholds are exceeded, helping users easily diagnose performance issues.


🏷️ Badges

| Category   | Badge                                                                         |
| ---------- | ----------------------------------------------------------------------------- |
| Language   | ![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)                 |
| Monitoring | ![Network Monitor](https://img.shields.io/badge/Network-Monitoring-green.svg) |
| Status     | ![Active](https://img.shields.io/badge/Status-Active-success.svg)             |


🚀 Features

Measures Latency, Packet Loss, Upload & Download Speeds

Real-time live chart updates using Matplotlib

Auto-removes old data for efficient visualization

Alerts for high latency or bandwidth usage

Background monitoring thread for smooth UI

🧠 Architecture

┌──────────────┐
│  Scheduler   │ → Runs network checks every 2 sec
└───────┬──────┘
        │
┌───────▼────────┐      ┌──────────────────────┐
│ Network Check   │◀────▶│  Data Storage (Dict) │
│ (ping + I/O)    │      └──────────────────────┘
└───────┬────────┘
        │
┌───────▼────────┐
│ Live Graph Plot │ → Updates Matplotlib chart
└────────────────┘


🧩 Function Breakdown

| Function              | Purpose                                                                       |
| --------------------- | ----------------------------------------------------------------------------- |
| `monitor_latency()`   | Pings host and logs latency & packet loss. Shows alert if threshold crossed.  |
| `monitor_bandwidth()` | Tracks upload/download speed and logs alerts for high usage.                  |
| `monitor_network()`   | Timestamp + runs above two functions + data trimming.                         |
| `update_plot()`       | Refreshes live chart with new values.                                         |
| `run_scheduler()`     | Schedules checks every 2 seconds using a thread.                              |


📂 Project Structure

📁 Live-Network-Monitor
│── app.py  → Main script for monitoring & visualization

▶️ How to Run
1️⃣ Install Dependencies: pip install psutil ping3 matplotlib schedule

2️⃣ Run Script: python app.py

The graph window will open and auto-update — close it to stop monitoring.


🎯 Optional Enhancements

| Category       | Ideas                                         |
| -------------- | --------------------------------------------- |
| UI             | Build a GUI dashboard using Tkinter or PyQt   |
| Export         | Save logs in CSV or database                  |
| Alerts         | Desktop notifications / Email alerts          |
| Security       | Real-time firewall rule suggestions           |
| Monitoring     | Multiple host support + selectable thresholds |
| Smart Analysis | AI-based abnormal network behavior detection  |


👩‍💻 Author

S Krithika
