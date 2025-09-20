# 🚀 VSD RISC-V SoC Tapeout Program – Week 0

## 📌 System Setup

* ✅ Installed **Ubuntu 20.04 LTS** (VirtualBox VM)
* ✅ Allocated **6 GB RAM, 4 vCPUs, 50 GB HDD**
* ✅ Installed Guest Additions for full-screen support

```bash
sudo apt update
sudo apt install build-essential dkms linux-headers-$(uname -r)
cd /media/<your-username>/VBox_GAs_7.1.8/
./autorun.sh
```

---

## 🛠️ Tool Installations

### 1️⃣ Yosys – Open Source Synthesis Tool

```bash
sudo apt-get update
git clone https://github.com/YosysHQ/yosys.git
cd yosys
sudo apt install make
sudo apt-get install build-essential clang bison flex \
    libreadline-dev gawk tcl-dev libffi-dev git \
    graphviz xdot pkg-config python3 libboost-system-dev \
    libboost-python-dev libboost-filesystem-dev zlib1g-dev

make config-gcc
git submodule update --init --recursive
make -j$(nproc)
sudo make install
```

✅ Verified with:

```bash
yosys -V
```

---

### 2️⃣ Icarus Verilog (iverilog) – Simulator

```bash
sudo apt-get update
sudo apt-get install iverilog
```

✅ Verified with:

```bash
iverilog -V
```

---

### 3️⃣ GTKWave – Waveform Viewer

```bash
sudo apt-get update
sudo apt install gtkwave
```

✅ Verified with:

```bash
gtkwave --version
```

---

## 📂 Progress Summary

* [x] Installed **Ubuntu VM**
* [x] Installed **Yosys** (logic synthesis)
* [x] Installed **Icarus Verilog** (simulation)
* [x] Installed **GTKWave** (waveform visualization)
* [x] Verified toolchain working

---

## 📸 Screenshots / Logs

*(Here you can add screenshots of terminal outputs for yosys -V, iverilog -V, gtkwave --version)*

---

✨ **Next Step → Week 1: RTL Design & Simulation**

---
