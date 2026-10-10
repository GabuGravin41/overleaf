# Fortress Focus: Local Blocker \& Progress Environment

You now have a complete, zero-dependency, local productivity environment called **Fortress** inside your project directory at:
[fortress/](file:///c:/Users/User%201/Documents/antigravity/beautiful-maxwell/fortress/)

This tool runs entirely on your local machine, requiring no paid API keys. It allows you to:
1.  **Enforce Work Sessions:** Blocks distracting websites (YouTube, Twitter, TikTok, Reddit, etc.) and disables browser incognito/dev-tools during work blocks.
2.  **Alert Transitions:** Pops up focus-stealing notifications on your screen forcing you to shift task sessions.
3.  **Keep a Living Biography:** Lets you log your daily completion status, successes, failures, and excuses into clean, structured Markdown and JSON diary files.
4.  **Track Biometrics \& Personality Profiles:** Logs mood, energy levels, focus quality, sleep/wake times, cognitive load symptoms, and distraction triggers.
5.  **Visualize Progress:** Auto-generates a local, offline-compatible HTML/SVG dashboard comparing your target schedule against actual execution metrics, including a **biometric trend graph**.
6.  **Analyze and Pivot:** Allows me, your AI partner, to scan your local logs and perform monthly reviews and optimizations.

---

## 1. System Components

The environment consists of the following local files:
*   [config.json](file:///c:/Users/User%201/Documents/antigravity/beautiful-maxwell/fortress/config.json): Timetable session hours, blocked domains list, and registry policies.
*   [blocker.py](file:///c:/Users/User%201/Documents/antigravity/beautiful-maxwell/fortress/blocker.py): Administrative script that edits the Windows hosts file and Registry keys to lock out Incognito mode and DevTools in Chrome and Edge. It contains the **3-Month Odyssean Contract** code.
*   [scheduler.py](file:///c:/Users/User%201/Documents/antigravity/beautiful-maxwell/fortress/scheduler.py): Background monitor checking the system clock. It silently triggers `blocker.py` and pops up focus-stealing Tkinter alerts at transitions.
*   [analytics.py](file:///c:/Users/User%201/Documents/antigravity/beautiful-maxwell/fortress/analytics.py): Parses daily logs and compiles them into a local [dashboard.html](file:///c:/Users/User%201/Documents/antigravity/beautiful-maxwell/fortress/dashboard.html), drawing SVG charts of completion rates and mood/focus trends.
*   [fortress.py](file:///c:/Users/User%201/Documents/antigravity/beautiful-maxwell/fortress/fortress.py): The main command-line dashboard for logging your daily progress, tasks, excuses, and checking your completion statistics.

---

## 2. Separate Blocker Constraints (Odyssean Contract vs. Scheduled Breaks)

To build discipline, the system splits focus constraints into two categories:

### **Category A: Scheduled Blocks (Social Media \& YouTube)**
*   **Target Domains:** `tiktok.com`, `instagram.com`, `facebook.com`, `twitter.com`, `x.com`, `reddit.com`, `youtube.com`
*   **Behavior:** Locked during your daily work sessions (Blocks A, B, and C). Unlocked during breaks, lunch, and off-hours.
*   **Temporary Reward:** If you need to access social media or YouTube during a study block, select **Option 6: Temporary Social Media Unblock** on the dashboard. Enter the number of hours (e.g., `1` or `0.5`). 
    *   This will unlock only the scheduled domains.
    *   The background scheduler checks your configuration every 30 seconds. Once the timer expires, the background daemon automatically re-applies the block, locking you out of social media again.

### **Category B: Permanent Blocks (Browser Incognito \& Adult Sites)**
*   **Target Domains:** `pornhub.com`, `xvideos.com`, `xnxx.com` (and browser-level incognito/dev-tools).
*   **Behavior:** Locked **24/7 for 3 Months** (August 21, 2026 to November 21, 2026).
*   **The Hard Lock:** The blocker checks the system clock. If the date is before November 21, 2026, the `unlock` command will **actively deny access** and restore the permanent blocks. Even when social media is unblocked during off-hours or via Option 6, Category B remains strictly locked.

---

## 3. Daily Logging \& The HTML Dashboard

Every time you log your review, or view analytics from the CLI:
1.  The dashboard parses all your daily logs inside [fortress/logs/](file:///c:/Users/User%201/Documents/antigravity/beautiful-maxwell/fortress/logs/).
2.  It compiles completion percentages for Blocks A, B, and C and updates a beautiful, local, offline-compatible page: [dashboard.html](file:///c:/Users/User%201/Documents/antigravity/beautiful-maxwell/fortress/dashboard.html)
3.  It automatically opens `dashboard.html` in your default browser, showing:
    *   **SVG Circular Progress Charts** indicating exact completion rates.
    *   **SVG Biometric Trend Chart:** Color-coded line graphs tracking your daily **Mood** (green), **Energy Level** (blue), and **Focus Quality** (orange) trends over the month.
    *   **Timeline Biography** showing your daily achievements, failures, excuses, and daily lessons side-by-side.

---

## 4. Setup \& Execution Guide

### **Step 1: Start the Background Blocker**
Open your terminal (Powershell or Command Prompt) as Administrator and run:
```bash
python "c:\Users\User 1\Documents\antigravity\beautiful-maxwell\fortress\scheduler.py"
```
Or open the dashboard and select **Option 3: Start Scheduler**. This starts the daemon that watches the clock, pops up Tkinter reminders, and applies the scheduled/permanent locks automatically.

### **Step 2: Daily End-of-Day Logging**
Before going to sleep, open the dashboard:
```bash
python "c:\Users\User 1\Documents\antigravity\beautiful-maxwell\fortress\fortress.py"
```
Select **Option 1: Log Daily Review**. After you enter your block statuses, you will be prompted for:
- **Biometrics:** Mood scale (1-10), Energy level (1-10), Focus quality (1-10), Wake-up time, and Bedtime.
- **Reflections:** Distraction triggers, cognitive load symptoms (brain fog, fatigue, clear mind), and a 1-sentence daily lesson.

This automatically updates your files inside `fortress/logs/` and auto-generates the updated [dashboard.html](file:///c:/Users/User%201/Documents/antigravity/beautiful-maxwell/fortress/dashboard.html).
Option 2 lets you view the dashboard in your default browser.
