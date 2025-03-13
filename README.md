# 🐧 Linux File System Hierarchy Explained  

The Linux filesystem is structured in a hierarchical tree format, starting at the root directory `/`. Each directory under `/` has a specific purpose and stores different types of system and user data. Understanding this structure is fundamental for system administration, troubleshooting, and development on Linux systems.  

---

## 🗂️ Key Linux Directories and Their Purposes  

| 📁 **Directory** | 📝 **Description** |
|-----------------|-------------------|
| **`/`**  | The root directory. Everything starts from here! |
| **`/bin`**  | Essential command binaries (e.g., `ls`, `cp`, `mv`) required for the system to boot and operate in single-user mode. |
| **`/boot`** | Files needed to boot the system, like the Linux kernel (`vmlinuz`) and bootloader (GRUB) configuration. |
| **`/dev`**  | Device files representing hardware components (e.g., `/dev/sda`, `/dev/tty`). |
| **`/etc`**  | Host-specific system-wide configuration files. Most system configuration files live here (e.g., `/etc/passwd`, `/etc/fstab`). |
| **`/home`** | User home directories (e.g., `/home/alice`). Each user has their own directory for personal files. |
| **`/lib`**  | Shared library files and kernel modules required by binaries in `/bin` and `/sbin`. |
| **`/media`** | Mount point for removable media (CD-ROMs, USB drives). |
| **`/mnt`**  | Temporary mount points for filesystems, often used for manually mounted volumes. |
| **`/opt`**  | Add-on application software packages, typically third-party apps (e.g., `/opt/google/chrome`). |
| **`/proc`** | Virtual filesystem providing process and kernel information as files (e.g., `/proc/cpuinfo`). |
| **`/root`** | Home directory for the root user (administrator). |
| **`/run`**  | Runtime data for processes since the last boot (PID files, sockets). |
| **`/sbin`** | System binaries used for system administration, generally reserved for the root user (e.g., `ifconfig`, `reboot`). |
| **`/srv`**  | Site-specific data served by the system (e.g., web server data at `/srv/www`). |
| **`/sys`**  | Virtual filesystem that provides information about devices and drivers (sysfs). |
| **`/tmp`**  | Temporary files. Often cleared at boot or on a schedule. |
| **`/usr`**  | User system resources: contains user programs, libraries, documentation (e.g., `/usr/bin`, `/usr/lib`). |
| **`/var`**  | Variable data files expected to grow, such as logs (`/var/log`), mail, and spool directories. |

---

## 🔧 Practical Tips  

### 1️⃣ Check disk space usage  

    df -h

2️⃣ Explore system processes with /proc

    cat /proc/cpuinfo
    cat /proc/meminfo

3️⃣ List user home directories

    ls /home    

4️⃣ Check system logs

    tail -f /var/log/syslog    

5️⃣ Explore loaded kernel modules

    ls /lib/modules/$(uname -r)/    


🎯 Summary
The Linux file system hierarchy standard (FHS) helps maintain consistency across different distributions. Knowing the purpose of each directory can significantly simplify system administration, troubleshooting, and securing Linux environments.    
