# Sami FTP Server 2.0.1 - MKD Buffer Overflow (ASLR Bypass via SEH Overwrite)
A buffer overflow is triggered when a long MKD command is sent to the server and the user views the Log tab.

## 📅 Date
January 15, 2013

## ✍️ Exploit Author
- **Christian (Polunchis) Ramirez** — [https://intlabs.ca](https://intlabs.ca)

**Contacts:**  
- polunchis@intlabs.ca  

## 📦 Software Information
- **Affected Software:** Sami FTP Server 2.0.1
- **Vendor Website:** *(Vendor no longer active)*
- **Vulnerability Type:** Buffer Overflow (SEH Overwrite, ASLR Bypass)

## 🖥️ Tested On
- Windows XP SP3 (English)

## 🛡️ Vulnerability Description
A **buffer overflow vulnerability** exists in **Sami FTP Server 2.0.1**.  
By sending a maliciously crafted `MKD` (Make Directory) command with an overly long payload to the FTP server, it is possible to overwrite the **Structured Exception Handler (SEH)**.

This exploit demonstrates **bypassing ASLR** protections by controlling the SEH, leading to **arbitrary code execution**.

**Authentication is not required** to exploit this vulnerability.

## ⚙️ Exploitation Details
- **Port:** 21/TCP (FTP)
- **Command:** `MKD`
- **Attack Vector:** Remote
- **Authentication:** Not required
- **Bypass Techniques:** ASLR Bypass via SEH Overwrite
- **Impact:** Full remote code execution

## 🛠️ Usage
⚠️ **Warning:**  
This exploit is intended for educational and authorized penetration testing purposes only. Unauthorized access to systems without permission is illegal.

```bash
# Example usage (if you provide exploit.py)
python exploit.py --target <IP_ADDRESS> --port 21

