Pre-requisite Software:
- python3 (https://www.python.org/)
- lm-sensors (https://github.com/lm-sensors/lm-sensors)
- kst2 (https://kst-plot.kde.org/)
(lm-sensors needs some setup)

Instalation Instructions:
- clone git
- copy "TempMonitor" to either where you want to run it or on your $PATH (recommend hard link to save space)
- initilize Temperature.log with whats in "---"s, repace 2970 with whatever is your max GPU fan speed (running sensors will show this)
---
0, 0, 0
100, 100, 2970

---
- now you can run TempMonitor wherever the log file is! (it will run else where but permanent log wont work well)
- to see the data being collected run "kst2 /tmp/Temperature.data" or "kst2 Temperature.log"
- ^C does not work for some reason, so the best way to Terminate "TempMonitor" is to find the PID of "TempMonitor" and "kill -9 PID"
     (htop has a search function which helps)


Information:
- Column 1 is CPU temperature
- Column 2 is GPU temperature
- Column 3 is GPU fan speed

