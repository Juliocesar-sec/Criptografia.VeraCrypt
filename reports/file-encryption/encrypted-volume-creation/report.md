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
![VeraCrypt Main Window](https://github.com/Juliocesar-sec/Criptografia.VeraCrypt/blob/003685a990f97c040b3ac38e621fcd5fe376ef42/print-vera.png)

### 🖼️ Image 2 – Volume Type
![Volume Type]([https://github.com/Juliocesar-sec/Criptografia.VeraCrypt/blob/1a162cafe558b9ce4eeb4d4250620fb5d00c7c03/print-vera.1.arquivo.png)

### 🖼️ Image 3 – Container Location
![Container Location](https://github.com/Juliocesar-sec/Criptografia.VeraCrypt/blob/0d0c4163fb1d9e7e1c4d00e9b27f9cf84e414436/print-vera.3.arquivo.png)

### 🖼️ Image 4 – Encryption Options
![Encryption Options]([images/04-encryption-options.png](https://github.com/Juliocesar-sec/Criptografia.VeraCrypt/blob/0d0c4163fb1d9e7e1c4d00e9b27f9cf84e414436/print-vera.4.arquivo.png))

### 🖼️ Image 5 – Volume Size
![Volume Size]([images/05-volume-size.png](https://github.com/Juliocesar-sec/Criptografia.VeraCrypt/blob/0d0c4163fb1d9e7e1c4d00e9b27f9cf84e414436/print-vera.5.arquivo.png))

### 🖼️ Image 6 – Volume Password
![Volume Password](https://github.com/Juliocesar-sec/Criptografia.VeraCrypt/blob/0d0c4163fb1d9e7e1c4d00e9b27f9cf84e414436/print-vera.6.arquivo.png)

### 🖼️ Image 7 – Volume Formatting
![Volume Formatting](https://github.com/Juliocesar-sec/Criptografia.VeraCrypt/blob/0d0c4163fb1d9e7e1c4d00e9b27f9cf84e414436/print-vera.7.arquivo.png)

### 🖼️ Image 8 – Overwrite Confirmation and Formatting Process
![Overwrite Confirmation]([images/08-overwrite-confirmation.png](https://github.com/Juliocesar-sec/Criptografia.VeraCrypt/blob/0d0c4163fb1d9e7e1c4d00e9b27f9cf84e414436/print-vera.8.arquivo.png)

### 🖼️ Image 9 – Volume Successfully Created
![Volume Successfully Created]([images/09-volume-created-success.png](https://github.com/Juliocesar-sec/Criptografia.VeraCrypt/blob/0d0c4163fb1d9e7e1c4d00e9b27f9cf84e414436/print-vera.9.arquivo.png)

### 🖼️ Image 10 – Final “Volume Created” Screen
![Final Volume Created](https://github.com/Juliocesar-sec/Criptografia.VeraCrypt/blob/89aad5cc9b458d51d509e12ba8d629fbda108afa/print-vera.10.arquivo.png)

### 🖼️ Image 11 – Volume Selection for Mounting
![Volume Selection for Mounting]([images/11-volume-selection-mount.png](https://github.com/Juliocesar-sec/Criptografia.VeraCrypt/blob/0d0c4163fb1d9e7e1c4d00e9b27f9cf84e414436/print-vera.11.arquivo.png)

### 🖼️ Image 12 – Mount Password Entry
![Mount Password Entry]([images/12-password-authentication.png](https://github.com/Juliocesar-sec/Criptografia.VeraCrypt/blob/0d0c4163fb1d9e7e1c4d00e9b27f9cf84e414436/print-vera.12.arquivo.png.png)

### 🖼️ Image 13 – Administrator Privilege Request
![Administrator Privilege Request](ghttps://github.com/Juliocesar-sec/Criptografia.VeraCrypt/blob/0d0c4163fb1d9e7e1c4d00e9b27f9cf84e414436/print-vera.13.arquivo.png)

### 🖼️ Image 14 – Volume Mounted Successfully
![Volume Mounted Successfully]([images/14-mounted-successfully.png](https://github.com/Juliocesar-sec/Criptografia.VeraCrypt/blob/0d0c4163fb1d9e7e1c4d00e9b27f9cf84e414436/print-vera.14.arquivo.png))

### 🖼️ Image 15 – Attempt to Open the Container Directly
![Attempt to Open Container Directly](images/15-direct-open-attempt.png)

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
