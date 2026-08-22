## 1. 💽 Operating System

The server runs **Ubuntu 24.04.4 LTS**, using the release codename **Noble**.

| Information        | Result             |
| ------------------ | ------------------- |
| **Distributor ID** | Ubuntu              |
| **Description**    | Ubuntu 24.04.4 LTS  |
| **Release**        | 24.04               |
| **Codename**       | `noble`             |

Ubuntu provides the operating environment where the server's applications, processes, networking, and other resources operate.

---

# 2. 🧩 Kernel Version

The server is running **Linux kernel 6.8.0-138-generic**.

| Information        | Result              |
| ------------------ | -------------------- |
| **Kernel Version** | `6.8.0-138-generic`  |

The kernel serves as the core of the Linux operating system, managing system resources and allowing software to interact with the available hardware.

---

# 3. 🖲️ CPU Model

The CPU identified by the Linux environment is an **Intel Xeon E312xx (Sandy Bridge, IBRS update)**.

| Information    | Result                                        |
| -------------- | ----------------------------------------------- |
| **CPU Model**  | Intel Xeon E312xx (Sandy Bridge, IBRS update)   |
| **BIOS Model** | RHEL-9.6.0 PC (Q35 + ICH9, 2009) CPU @ 2.0GHz   |

The CPU provides the processing capability required to execute applications, system processes, and cloud workloads.

---

# 4. 🔩 CPU Cores

The environment has **1 CPU core** available.

| Resource      | Value |
| ------------- | ----: |
| **CPU Cores** | **1** |

A CPU core represents an available processing unit. In this environment, the cloud server has a single assigned core for processing its workloads.

---

# 5. 📊 Memory / RAM

The server has **1.9 GiB of total RAM**.

### Memory Status

| Memory           |  Amount |
| ---------------- | ------: |
| **Total**        | 1.9 GiB |
| **Used**         | 452 MiB |
| **Free**         | 770 MiB |
| **Shared**       | 1.1 MiB |
| **Buffer/Cache** | 856 MiB |
| **Available**    | 1.4 GiB |

### Swap Status

| Swap      |  Amount |
| --------- | ------: |
| **Total** | 1.0 GiB |
| **Used**  |     0 B |
| **Free**  | 1.0 GiB |

At the time of checking, the server had **1.4 GiB of available memory**, while its **1.0 GiB swap space was unused**.

---

# 6. 🗄️ Disk Capacity

The primary filesystem is `/dev/vda1`, which provides **19 GB** of storage.

| Filesystem  |  Size |   Used | Available | Usage | Mount Point |
| ----------- | ----: | -----: | --------: | ----: | ----------- |
| `/dev/vda1` | 19 GB | 5.4 GB |     13 GB |   30% | `/`         |

### Storage Snapshot

```text
Total Capacity    19 GB
Used              5.4 GB
Available         13 GB
Utilization       30%
```

Approximately **70% of the main filesystem remains available**, providing space for applications, files, and additional system data.

---

# 7. 📁 Mounted File Systems

The Linux environment contains several mounted filesystems. Each serves a specific purpose within the operating system.

| Filesystem   |   Size |   Used | Available | Usage | Mount Point |
| ------------ | -----: | -----: | --------: | ----: | ----------- |
| `tmpfs`      | 191 MB | 996 KB |    190 MB |    1% | `/run`      |
| `/dev/vda1`  |  19 GB | 5.4 GB |     13 GB |   30% | `/`         |
| `tmpfs`      | 952 MB |  84 KB |    952 MB |    1% | `/dev/shm`  |
| `tmpfs`      | 5.0 MB |    0 B |    5.0 MB |    0% | `/run/lock` |
| `/dev/vda16` | 881 MB | 117 MB |    703 MB |   15% | `/boot`     |
| `/dev/vda15` | 105 MB | 6.2 MB |     99 MB |    6% | `/boot/efi` |

### 🧭 Filesystem Roles

| Mount Point | Purpose                                                                |
| ----------- | ----------------------------------------------------------------------- |
| `/`         | Main root filesystem containing the operating system and applications   |
| `/boot`     | Stores files required during the Linux boot process                     |
| `/boot/efi` | Contains EFI-related boot files                                         |
| `/run`      | Stores temporary runtime information                                    |
| `/dev/shm`  | Provides temporary shared-memory storage                                |
| `/run/lock` | Provides temporary lock-related runtime storage                         |

---

# 8. 🏷️ Hostname

The hostname assigned to the server is:

```text
ubuntu
```

| Information  | Result   |
| ------------ | -------- |
| **Hostname** | `ubuntu` |

The hostname provides an identifiable name for the server within its environment.

---

# 9. 📡 IP Address

The server returned two IP addresses:

| Interface Address | IP Address   |
| ------------------ | ------------ |
| **Address 1**      | `172.30.1.2` |
| **Address 2**      | `172.17.0.1` |

These addresses were returned by the `hostname -I` command.

>  **Network Note:** Both addresses belong to private IP address ranges and are associated with the network environment provided by the cloud playground.

---

# 🧾 Additional Notes

While inspecting the environment, the `dh` command (from the `debhelper` package) was attempted but was **not found**, with the system suggesting installation via:

```bash
apt install debhelper
```

This indicates `debhelper` is not installed by default in this playground image.

---

# *📋 Summary*

*The following table summarizes the main infrastructure resources identified in the Linux environment.*

| *Category*    | *Resource*     | *Result*                         |
| ------------- | -------------- | --------------------------------- |
| *💽 OS*       | *Distribution* | *Ubuntu 24.04.4 LTS*              |
| *🧩 System*   | *Kernel*       | *6.8.0-138-generic*               |
| *🖲️ Compute*  | *CPU*          | *Intel Xeon E312xx*               |
| *🔩 Compute*  | *CPU Cores*    | *1*                               |
| *📊 Memory*   | *RAM*          | *1.9 GiB*                         |
| *🗄️ Storage*  | *Main Disk*    | *19 GB*                           |
| *📁 Storage*  | *Root Usage*   | *30%*                             |
| *🏷️ Network*  | *Hostname*     | *`ubuntu`*                        |
| *📡 Network*  | *IP Addresses* | *`172.30.1.2`**, **`172.17.0.1`*  |
