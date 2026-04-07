# 🔐 Report: Creation and Mounting of an Encrypted Volume with VeraCrypt

### 📁 Cybersecurity Portfolio

**Author:** [Your Name]
**Date:** April 7, 2026

---

## 📌 Introduction

This report documents, in a detailed step-by-step manner, the complete process of **creating, mounting, and functionally validating an encrypted file container** using VeraCrypt in a Linux environment.

The objective is to demonstrate practical knowledge of **data-at-rest encryption**, with emphasis on security best practices, including:

* selection of strong algorithms (**AES-256 + SHA-512**)
* generation of a complex password using Proton Pass
* proper entropy collection
* creation of a standard (non-hidden) container
* secure volume mounting
* read/write validation
* secure file behavior outside the software

The process was carried out in a Linux virtual machine for demonstration and portfolio-building purposes.

---

## 🖥️ Environment Used

* Linux operating system (XFCE interface)
* Tools used:

  * VeraCrypt
  * Proton Pass
  * Thunar (file manager)

---

## ⚙️ Step-by-Step Description of the Images

### 🖼️ Image 1 – VeraCrypt Main Window (print-vera.png)

* VeraCrypt opened on the **Volumes** tab
* Slots 1 through 11 empty
* Slot 6 selected (highlighted in blue)
* No mounted volumes

🔎 **Analysis:**
This is the software’s initial interface, where the user selects the mount slot for the encrypted volume.

🔐 **Security best practice observed:**
The **“Never save history”** option is enabled, preventing storage of usage traces.

---

### 🖼️ Image 2 – Volume Type (print-vera.1.arquivo.png)

* Start of the *VeraCrypt Volume Creation Wizard*
* Selected option: **Standard VeraCrypt Volume**
* Hidden volume option not used

🔎 **Analysis:**
The standard volume was chosen for its simplicity and portability.

🛡️ **Security note:**
The presence of the hidden volume option demonstrates awareness of advanced **plausible deniability techniques**, even though it was not used in this scenario.

---

### 🖼️ Image 3 – Container Location (print-vera.2.arquivo.png)

* Defined path:

```text
/home/purpleghost/Exemplo.criptografado/arquivo.criptografado
```

* “Never save history” enabled
* Warning about overwriting an existing file

🔎 **Analysis:**
A file-based container was chosen, allowing:

* portability
* easy backup
* secure transfer

⚠️ **Important event:**
VeraCrypt detected an existing file. Overwrite was manually confirmed.

---

### 🖼️ Image 4 – Encryption Options (print-vera.3.arquivo.png)

* Encryption algorithm: **AES (256-bit, XTS mode)**
* Hash algorithm: **SHA-512**

🔎 **Technical analysis:**

* **AES-256**: gold standard of modern symmetric encryption
* **XTS mode**: ideal for disk encryption
* **SHA-512**: robust hash function resistant to collisions

🛡️ **Conclusion:**
Highly secure configuration suitable for professional use.

---

### 🖼️ Image 5 – Volume Size (print-vera.4.arquivo.png)

* Defined size: **1 GiB**
* Available space: 193 GiB

🔎 **Analysis:**
A balanced choice for:

* practical testing
* real-world simulation

📌 **Observation:**
The size can be adjusted according to operational requirements.

---

### 🖼️ Image 6 – Volume Password (print-vera.5.arquivo.png)

* Password generated via Proton Pass
* Strength rating: **Strong Password**
* Disabled options:

  * PIM
  * Keyfiles

🔎 **Security analysis:**

* high entropy
* use of special characters
* automated generation

🛡️ **Critical best practice:**
Completely avoids predictable or reused passwords.

---

### 🖼️ Image 7 – Volume Formatting (print-vera.6.arquivo.png)

* Entropy collection through mouse movement
* Randomness bar in progress
* **Format** button available

🔎 **Technical analysis:**
At this stage:

* cryptographic keys are generated
* entropy ensures unpredictability
* the volume is internally structured

🔐 **Importance:**
The greater the entropy, the stronger the volume security.

---

### 🖼️ Image 8 – Overwrite Confirmation and Formatting Process (print-vera.7.arquivo.png)

* VeraCrypt main window open in the background
* Wizard at the **Volume Format** stage
* Entropy bar fully filled
* Warning dialog stating the file already exists
* **Yes** selected for overwrite

🔎 **Analysis:**
At this step, VeraCrypt requested confirmation to replace the previously existing container.

⚠️ **Important event:**
Overwrite was manually authorized, demonstrating operational awareness regarding:

* loss of previous contents
* complete regeneration of cryptographic keys
* reinitialization of the internal volume structure

🛡️ **Best practice observed:**
Explicit confirmation prevents accidental overwrites.

---

### 🖼️ Image 9 – Volume Successfully Created (print-vera.8.arquivo.png)

* VeraCrypt pop-up message displayed:

> “The VeraCrypt volume has been successfully created.”

* Formatting process completed
* Main window still open in the background

🔎 **Technical analysis:**
This confirms that all critical stages were completed successfully:

* key generation
* AES-256 application
* SHA-512 hashing
* internal filesystem creation
* portable container finalization

✔️ **Immediate result:**
The volume is now ready for mounting, authentication, and secure use.

---

### 🖼️ Image 10 – Final “Volume Created” Screen (print-vera.9.arquivo.png)

* Final wizard screen displaying **Volume Created**
* Options available:

  * **Next >**
  * **Exit**

🔎 **Analysis:**
This final screen confirms successful completion of the creation wizard.

The volume is now ready for:

* mounting in the selected slot
* secure file storage
* safe dismounting
* future reuse with the same password

---

### 🖼️ Image 11 – Volume Selection for Mounting (print-vera.10.arquivo.png)

* VeraCrypt main window on the **Volumes** tab
* Slot 1 selected
* Empty volume table
* **Select a VeraCrypt Volume** window open
* Selected file: **arquivo.criptografado**
* Approximate size: **1.1 GB**
* Displayed type: **Unknown**

🔎 **Analysis:**
This step begins the encrypted volume mounting process.

The file appears as **Unknown** because it is a binary encrypted container rather than a standard system-readable file format.

🛡️ **Best practice observed:**
Using the native file selector reduces path errors and mistyping risks.

---

### 🖼️ Image 12 – Mount Password Entry (print-vera.11.arquivo.png)

* Proton Pass window open in the background
* Password classified as **Strong**
* VeraCrypt authentication prompt visible
* Password field filled with hidden characters
* Disabled options:

  * Use PIM
  * Cache passwords and keyfiles in memory
  * Use keyfiles

🔎 **Analysis:**
This step demonstrates a secure authentication flow in which the strong password is retrieved directly from the password manager.

🔐 **Security relevance:**
Using Proton Pass drastically reduces the risk of reused, weak, or insecurely stored passwords.

---

### 🖼️ Image 13 – Administrator Privilege Request (print-vera.12.arquivo.png)

* Slot 1 remains selected
* Pop-up: **Administrator privileges required**
* Administrator password field visible

🔎 **Analysis:**
In Linux systems, mounting under **/media/** requires elevated privileges.

⚠️ **Important event:**
Privilege escalation is required only for the mounting operation and does not affect the container’s cryptographic security.

---

### 🖼️ Image 14 – Volume Mounted Successfully (print-vera.13.arquivo.png)

* Volume mounted in **Slot 1**
* Size: **1023 MiB**
* Mount directory:

```text
/media/veracrypt1
```

* Type: **Normal**
* Test file visible in Thunar

🔎 **Technical analysis:**
The volume was successfully mounted and is accessible as a normal directory while open.

The data remains **decrypted only in memory during active use**, returning to protected state after dismount.

🛡️ **Critical best practice:**
Immediate dismount after use is recommended to restore at-rest protection.

---

### 🖼️ Image 15 – Attempt to Open the Container Directly (print-vera.14.arquivo.png)

* File **arquivo.criptografado** selected in Thunar
* Type shown as **Unknown**
* **Set Default Application** pop-up displayed
* No recommended application available

🔎 **Analysis:**
This demonstrates the expected behavior when attempting to open the container outside VeraCrypt.

The operating system recognizes it as an encrypted binary blob with no associated application.

⚠️ **Security warning:**
The container should never be directly edited or manipulated through the file manager, as this may compromise its structural integrity.

---

## 🔒 Results Achieved

* Encrypted volume successfully created
* Secure container ready for use
* Effective data-at-rest protection
* Portable file compatible with multiple systems
* Successful mounting and functional validation

---

## 🛡️ Security Conclusions and Lessons Learned

This process demonstrates mastery of the following cybersecurity competencies:

* correct VeraCrypt usage
* strong encryption deployment (AES-256 + SHA-512)
* secure password generation with Proton Pass
* understanding of entropy importance
* application of operational best practices
* use of portable encrypted containers
* secure mounting workflow in Linux
* safe behavior validation outside the encryption software

---

## 📚 Final Considerations

The created volume can be mounted on different operating systems (Linux, Windows, and macOS), making it an efficient solution for:

* secure storage of sensitive data
* encrypted backups
* protection against unauthorized access in case of loss or theft

This type of practice is widely used in corporate environments and represents an essential competency for information security professionals.

---

## 🧰 Tools Used

* VeraCrypt
* Proton Pass
* Linux system (test environment)
