# Pomodoro CLI Timer 🕰️

A simple **Pomodoro Timer** that runs directly from your terminal using Node.js.  
Set custom **work** and **break** durations (in minutes) and get desktop notifications when it's time to switch.

This tool uses:
- `node-notifier` for desktop notifications
- `moment.js` for time formatting

## ✨ Features

- Terminal-based Pomodoro timer
- Customizable work and break durations
- Automatic switch between work and break sessions
- Desktop notification alerts

## 🚀 Installation

1. Clone this repository

```bash
git clone https://github.com/your-username/pomodoro-timer-cli.git
cd pomodoro-timer-cli


npm install
node index.js <work_duration> <break_duration>
node index.js 25 5

Work: 00:25:00
Work: 00:24:59
...
Notifications are disabled
Reason: DisabledForUser Please make sure that the app id is set correctly.


notifier.notify({
  title: isWorking ? 'Break Time!' : 'Work Time!',
  message: isWorking ? "let's break" : 'Now get back to Work!',
  sound: true,
  wait: true,
  appID: 'PomodoroTimer' // Optional for Windows SnoreToast
});
