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

### 🖼️ Image 1 – VeraCrypt Main Window
[![VeraCrypt Main Window](images/01-veracrypt-main-window.png)](images/01-veracrypt-main-window.png)

### 🖼️ Image 2 – Volume Type
[![Volume Type](images/02-volume-type.png)](images/02-volume-type.png)

### 🖼️ Image 3 – Container Location
[![Container Location](images/03-container-location.png)](images/03-container-location.png)

### 🖼️ Image 4 – Encryption Options
[![Encryption Options](images/04-encryption-options.png)](images/04-encryption-options.png)

### 🖼️ Image 5 – Volume Size
[![Volume Size](images/05-volume-size.png)](images/05-volume-size.png)

### 🖼️ Image 6 – Volume Password
[![Volume Password](images/06-volume-password.png)](images/06-volume-password.png)

### 🖼️ Image 7 – Volume Formatting
[![Volume Formatting](images/07-volume-formatting.png)](images/07-volume-formatting.png)

### 🖼️ Image 8 – Overwrite Confirmation and Formatting Process
[![Overwrite Confirmation](images/08-overwrite-confirmation.png)](images/08-overwrite-confirmation.png)

### 🖼️ Image 9 – Volume Successfully Created
[![Volume Successfully Created](images/09-volume-created-success.png)](images/09-volume-created-success.png)

### 🖼️ Image 10 – Final “Volume Created” Screen
[![Final Volume Created](images/10-final-created-screen.png)](images/10-final-created-screen.png)

### 🖼️ Image 11 – Volume Selection for Mounting
[![Volume Selection for Mounting](images/11-volume-selection-mount.png)](images/11-volume-selection-mount.png)

### 🖼️ Image 12 – Mount Password Entry
[![Mount Password Entry](images/12-password-authentication.png)](images/12-password-authentication.png)

### 🖼️ Image 13 – Administrator Privilege Request
[![Administrator Privilege Request](images/13-admin-privileges.png)](images/13-admin-privileges.png)

### 🖼️ Image 14 – Volume Mounted Successfully
[![Volume Mounted Successfully](images/14-mounted-successfully.png)](images/14-mounted-successfully.png)

### 🖼️ Image 15 – Attempt to Open the Container Directly
[![Attempt to Open Container Directly](images/15-direct-open-attempt.png)](images/15-direct-open-attempt.png)

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
