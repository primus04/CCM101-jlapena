# ☁️ Continue Your Linux Investigation

## 1. Linux Server Investigation

The following Linux commands were used in the KillerCoda Playground to identify the basic information of the Linux server.

| Information          | Linux Command         | Command Meaning                                                                                                              |
| -------------------- | --------------------- | ---------------------------------------------------------------------------------------------------------------------------- |
| **Operating System** | `cat /etc/os-release` | Displays information about the installed Linux operating system, including its name and version.                             |
| **CPU Information**  | `lscpu`               | Displays detailed information about the CPU, such as architecture, number of CPUs, cores, and threads.                       |
| **Memory**           | `free -h`             | Displays the total, used, and available RAM. The `-h` option makes the values easier to read.                                |
| **Disk Space**       | `df -h`               | Displays the available and used disk space of the file systems. The `-h` option shows the values in a human-readable format. |

---

# 2. Commands and Results

## Operating System

### Command

```bash
cat /etc/os-release
```

### Meaning

This command displays information about the Linux operating system installed on the server. It can show the operating system name, version, ID, and other distribution details.

### Result

Paste the terminal output here.

### Screenshot

Paste your screenshot here.

---

## CPU Information

### Command

```bash
lscpu
```

### Meaning

This command displays information about the server's CPU. It can show the CPU architecture, number of CPUs, cores, threads, and processor information.

### Result

Paste the terminal output here.

### Screenshot

Paste your screenshot here.

---

## Memory

### Command

```bash
free -h
```

### Meaning

This command displays the server's memory usage. It shows the total, used, free, shared, and available RAM.

The `-h` means **human-readable**, so the memory values are displayed using units such as MB or GB.

### Result

Paste the terminal output here.

### Screenshot

Paste your screenshot here.

---

## Disk Space

### Command

```bash
df -h
```

### Meaning

This command displays information about disk space. It shows the total size, used space, available space, and percentage of disk space being used.

The `-h` means **human-readable**, making the storage values easier to understand.

### Result

Paste the terminal output here.

### Screenshot

Paste your screenshot here.

---

# 3. Cloud Migration

If this Linux server were migrated to the cloud, it could be hosted using virtual machine services from AWS, Microsoft Azure, or Google Cloud Platform.

| Cloud Platform            | Cloud Service          | Purpose                                                        |
| ------------------------- | ---------------------- | -------------------------------------------------------------- |
| **AWS**                   | Amazon EC2             | Runs Linux virtual machines in the AWS cloud.                  |
| **Microsoft Azure**       | Azure Virtual Machines | Runs Linux virtual machines in Microsoft Azure.                |
| **Google Cloud Platform** | Google Compute Engine  | Runs Linux virtual machines using Google Cloud infrastructure. |

---

# 4. Cloud Services

## AWS – Amazon EC2

**Amazon EC2 (Elastic Compute Cloud)** can host the Linux server as a virtual machine. It allows the organization to choose computing resources such as CPU, memory, storage, and networking according to the server's requirements.

## Microsoft Azure – Azure Virtual Machines

**Azure Virtual Machines** can run the Linux server in Microsoft's cloud infrastructure. Azure supports different Linux distributions and allows organizations to select the required CPU, memory, storage, and other resources.

## Google Cloud – Google Compute Engine

**Google Compute Engine** can host the Linux server as a virtual machine. It allows organizations to configure the machine's CPU, memory, storage, and other resources based on the workload.

---

# 5. Comparison

| Requirement               | AWS          | Microsoft Azure        | Google Cloud          |
| ------------------------- | ------------ | ---------------------- | --------------------- |
| **Linux Virtual Machine** | Amazon EC2   | Azure Virtual Machines | Google Compute Engine |
| **CPU Resources**         | Configurable | Configurable           | Configurable          |
| **Memory**                | Configurable | Configurable           | Configurable          |
| **Storage**               | Amazon EBS   | Azure Managed Disks    | Persistent Disk       |
| **Scalability**           | Yes          | Yes                    | Yes                   |

---

# 6. Conclusion

The Linux server can be migrated to any of the three major cloud platforms. AWS can use **Amazon EC2**, Microsoft Azure can use **Azure Virtual Machines**, and Google Cloud can use **Google Compute Engine**. These services allow organizations to run Linux servers in the cloud while providing flexible computing, memory, storage, and scaling options.

# 7. Terminal Screenshots

## Operating System

*Paste your `cat /etc/os-release` screenshot here.*

## CPU Information

*Paste your `lscpu` screenshot here.*

## Memory

*Paste your `free -h` screenshot here.*

## Disk Space

*Paste your `df -h` screenshot here.*
