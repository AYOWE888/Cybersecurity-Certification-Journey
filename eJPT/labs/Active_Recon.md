# Active Reconnaissance: Full Room GitHack Log

## Key Points Studied & Tested

- **Browser-Based Reconnaissance:** Utilized built-in developer frameworks to review application layers, transport certificates, cookie elements, and direct response headers.

- **Layer 3 & Layer 4 Verification:** Deployed `ping` to isolate infrastructure presence and interpret remote operating systems using default Time-To-Live (`TTL`) indicators.

- **Route Path Interrogation:** Evaluated network layout boundaries using `traceroute` mechanisms to map active hops and bypass packet filters with TCP switches.

- **Application Banner Grabbing:** Leveraged interactive client vectors (`telnet` and `netcat`) to open direct TCP handles against remote ports, forcing running network daemons to reveal explicit application names and operational version codes.

- **Operational Classification:** Solidified the architectural boundary that any diagnostic technique transmitting raw frames or initiating network handshakes directly to a target system is classified as **Active Reconnaissance**.

---

## High-Impact Questions & Analysis

### 1. What is the size of the ICMP header in bytes?

**Analysis:** An Internet Control Message Protocol (ICMP) header uses exactly **8 bytes** of data, structuring static fields for the control **Type**, sub-category **Code**, **Checksum** validation, and specialized **Header Data**.

---

### 2. Does MS Windows Firewall block ping by default? (Y/N)

**Analysis:** **Y (Yes).** To prevent automated internal network mapping sweeps, default inbound security policies on modern Windows systems explicitly drop incoming ICMP Echo Requests.

---

### 3. In Traceroute B, how many routers are between the two systems?

**Analysis:** There are **25 intermediate routers**. The destination framework is reached at hop **26**, meaning hops **1 through 25** act as the Layer 3 routing nodes handling intermediate transit packets.

---

### 4. On the AttackBox, check the `nc` help menu to see how to start a listener. Which option ensures that `nc` remains listening even after a client disconnects?

**Analysis:** The keep-alive flag `-k` must be applied alongside the listen configuration (`-l`) to force Netcat to remain persistent and accept back-to-back incoming connections.

---

### 5. Connect to port 21 of the target VM. What is the version of the FTP server?

**Analysis:** Probing port **21** returns a cleartext protocol advertisement header:

```text
FTP server (Version 6.4/Linux-ftpd-0.17) ready.
```

The target application version is **0.17**.

---

### 6. Connect to port 80 of the target VM. What is the version of the HTTP server?

**Analysis:** Sending raw connection flags to port **80** establishes an unencrypted HTTP handshake, revealing that the application layer is running **Nginx 1.27.1**.

---

### 7. What is the primary operational benefit of using `dig` over legacy `nslookup` engines?

**Analysis:** `dig` directly uses native system OS resolver libraries and prints structured records matching authoritative zone files, avoiding the abstract formatting often associated with `nslookup`.

---

### 8. How does the transport layer configuration of RDAP enhance reconnaissance stability compared to WHOIS?

**Analysis:** WHOIS runs over raw TCP port **43**, which is heavily monitored or blocked by egress filters. RDAP transfers standard programmatic JSON structures over standard **HTTPS (port 443)**, blending seamlessly with everyday web traffic.

---

## Reference Material

| Item | Value |
|--------|--------|
| Target Room | TryHackMe Active Reconnaissance |
| Attacker Local IP | `10.65.121.59` |
| Target Environment IP | `10.65.160.255` |

---

## Proof of Completion

**Final Lab Status:** ✅ **100% Completed**

### Live Terminal Verification Stream

```text
[Insert terminal output, screenshots, or verification logs here]
```
