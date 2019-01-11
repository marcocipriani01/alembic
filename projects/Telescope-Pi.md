---
title: Telescope-Pi
image: cover.jpg
feature_text: |-
  ## <span style="color:white">Telescope-Pi</span>
  <span style="color:white">Telescope remote control service for Raspberry Pi</span>
feature_image: cover.jpg
excerpt: 'Telescope-Pi is the name I gave to the Raspberry Pi 3 B+ I use to remotely
  control my telescope. This project contains an installer that will guide the user
  while downloading and configuring all the INDI drivers and software needed to control
  CCDs, DSLRs and telescope mounts. Moreover, a Bluetooth service is installed: if
  you are away from known Wi-Fi network, you can use its Android app to connect the
  board to another access point or even start the hotspot mode, ideal if you are,
  for instance, in a trip far from light pollution. The service will also start the
  Indi Web Manager (and the OpenFocuser server if installed) at startup, while the
  system service manager (systemd) will check if something suddenly crashed: if the
  server crashes, it is automatically restarted. No programming competencies are required
  to install the software because the installation scripts are completely automated
  and will even fix common Raspberry issues (e.g. Bluez and Rfcomm). When configured,
  just turn on the board (no mouse, keyboard or screen required), use the app to connect
  to a Wi-Fi AP and then remotely manage the telescope!'
aside: true
---

#### Project home on [GitHub](https://github.com/marcocipriani01/Telescope-Pi)

Telescope-Pi is the name I gave to the Raspberry Pi 3 B+ I use to remotely control my telescope. This project contains an installer that will guide the user while downloading and configuring all the INDI drivers and software needed to control CCDs, DSLRs and telescope mounts. Moreover, a Bluetooth service is installed: if you are away from known Wi-Fi network, you can use its Android app to connect the board to another access point or even start the hotspot mode, ideal if you are, for instance, in a trip far from light pollution. The service will also start the Indi Web Manager (and the OpenFocuser server if installed) at startup, while the system service manager (systemd) will check if something suddenly crashed: if the server crashes, it is automatically restarted. No programming competencies are required to install the software because the installation scripts are completely automated and will even fix common Raspberry issues (e.g. Bluez and Rfcomm). When configured, just turn on the board (no mouse, keyboard or screen required), use the app to connect to a Wi-Fi AP and then remotely manage the telescope!

### Usage and description

Behind the scenes, it's an Indi Web Manager starter/stopper, network and power manager Bluetooth service for Raspberry Pi (Raspbian only, tested on 3 B+). Installers in the `install-kit` folder will guide you through updating the system, installing, configuring and starting the server and its dependencies, just run them in the correct order. If you don't need OpenFocuser, script 4 can be skipped without problems. You'll be asked for a hostname for the server, a password for the hotspot mode and the network interface to control via Bluetooth. INDI and bluez will be downloaded/updated automatically and common troubles about Bluetooth in Raspbian will be fixed. Then some systemd services will be set up to correctly start the Bluetooth controller and indiserver.

### Android app
I'm still working on a good Android app for Telescope-Pi. In the meanwhile, you can use a Bluetooth serial terminal app (in this way, it should work even with iPhones or desktop Bluetooth terminals, but I've never tested it in these ways): just connect to the board and all the available commands will be listed. Chose an option by sending a number and start controlling your Raspberry!

![Telescope-Pi](2.jpg)
