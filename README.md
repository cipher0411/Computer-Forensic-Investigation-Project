# Computer-Forensic-Investigation-Project

> **Disclaimer:** This project is a fictional case created for demonstration purposes. It is not related to any real-life events or investigations. The case and evidence used here are purely for illustrative purposes and should not be interpreted as real. This project is not intended for educational use and does not represent actual forensic analysis or criminal investigations.

## Objective

The objective of this forensic investigation was to thoroughly examine digital evidence related to a criminal activity involving arson and fraud. The investigation focused on acquiring and analyzing data from multiple sources, including mobile phones, solid-state drives (SSDs), and USB sticks. This case aimed to uncover evidence that could help establish the involvement of individuals in planning and executing a fire at a storage facility, resulting in a fatality and an insurance fraud scheme.

### Skills Learned

- **Forensic Data Acquisition:** Gained hands-on experience in acquiring data from various digital devices using industry-standard forensic tools.
- **Digital Evidence Analysis:** Developed proficiency in using forensic tools like FTK Imager and Autopsy to analyze file structures, recover deleted files, and identify crucial digital evidence.
- **Password Cracking:** Enhanced skills in password recovery techniques using tools like John the Ripper to decrypt encrypted files.
- **Cryptographic Analysis:** Applied knowledge of encryption and hashing algorithms to validate the integrity of evidence and uncover hidden data.
- **Chain of Custody Management:** Gained experience in maintaining the integrity of evidence by following strict procedures for data acquisition and handling.

### Tools Used

- **FTK Imager:** A tool used for creating bit-for-bit forensic images of storage devices.
- **Autopsy:** Open-source software for analyzing forensic images, recovering deleted files, and examining file metadata.
- **John the Ripper:** A password cracking tool used to decrypt encrypted Word documents.
- **Write Blocker:** A hardware tool used to prevent accidental modification of evidence during the acquisition process.
- **Kali Linux:** A Linux distribution used for forensic investigations, particularly for running John the Ripper.

## Steps

### 1. Data Acquisition

**Objective:** To acquire data from the SSD and USB stick while ensuring data integrity using FTK Imager and write blockers.

- **Acquiring Data from the SSD:**
  - Attached the SSD to the write blocker to prevent data modification during the acquisition.
  - Connected the SSD to the computer and used FTK Imager to create a bit-for-bit image of the drive.
  - The forensic image was saved in the E01 format and hash values (MD5, SHA-1) were generated to verify data integrity.

  ![Ref 1: SSD Acquisition Process](path/to/your/screenshot1.png)

- **Acquiring Data from the USB Stick:**
  - Similar procedure was followed for the USB stick using FTK Imager.
  - A forensic image of the USB drive was created and stored in a separate folder with appropriate hash values to verify its integrity.

  ![Ref 2: USB Stick Acquisition](path/to/your/screenshot2.png)

### 2. Data Analysis

**Objective:** To analyze the forensic images from the SSD and USB stick using Autopsy and recover relevant evidence.

- **Loading Forensic Images into Autopsy:**
  - Opened Autopsy on the analysis workstation and created a new case for the investigation.
  - Added the forensic image files (E01) of the SSD and USB stick as data sources in Autopsy.

  ![Ref 3: Autopsy Data Ingestion](path/to/your/screenshot3.png)

- **Examination of SSD Files:**
  - After ingestion, Autopsy was used to browse the file system on the SSD. I found several relevant files in the "Bad Items" folder.
  - Notably, Word documents named `Skype.exe`, `Order.docx`, `Task.docx`, and `Rob.docx` were discovered, all of which were encrypted with passwords.

  ![Ref 4: SSD Analysis](path/to/your/screenshot4.png)

- **Examination of USB Stick Files:**
  - Similar analysis was conducted on the USB stick, where encrypted documents were found in the "Bad Items" folder.
  - These documents contained valuable evidence linking the suspects to the crime, including plans to carry out the arson.

  ![Ref 5: USB Analysis](path/to/your/screenshot5.png)

### 3. Decrypting Encrypted Files

**Objective:** To decrypt the encrypted Word documents found on the SSD and USB drive.

- **Using John the Ripper for Password Cracking:**
  - The encrypted Word documents (`Skype.exe`, `Order.docx`, `Task.docx`, `Rob.docx`) were extracted and stored in a folder on Kali Linux.
  - John the Ripper was set up on a Kali Linux virtual machine to perform brute-force password cracking on the documents.

  ![Ref 6: John the Ripper Setup](path/to/your/screenshot6.png)

- **Cracking the Passwords:**
  - Using a wordlist (`rockyou.txt`), John the Ripper attempted to brute-force the passwords for the encrypted documents.
  - The process revealed the passwords, allowing access to the content of the documents, which contained critical communications and instructions for executing the crime.

  ![Ref 7: Decrypted Documents](path/to/your/screenshot7.png)

### 4. Investigating Evidence

**Objective:** To analyze the decrypted documents and identify key evidence linking the suspects to the crime.

- **Content Analysis of `Rob.docx`:**
  - The document revealed instructions to turn off safety measures and spill fuel in the storage facility, which was part of the plan to set it on fire.

  ![Ref 8: Rob.docx Content](path/to/your/screenshot8.png)

- **Corroborating Evidence from the SSD:**
  - The analysis of the SSD's email folder revealed communication between the suspects, confirming the planning of the arson and fraud.

  ![Ref 9: Email Communication](path/to/your/screenshot9.png)

### 5. Reporting and Chain of Custody

**Objective:** To compile findings into a forensic report while ensuring the integrity of the evidence.

- **Creating the Final Report:**
  - A detailed forensic report was generated, summarizing the findings from the SSD, USB stick, and decrypted documents.
  - All evidence was securely stored, and the chain of custody was meticulously documented to ensure the integrity of the evidence.

  ![Ref 10: Forensic Report](path/to/your/screenshot10.png)

## Conclusion

This forensic investigation successfully uncovered crucial evidence linking the suspects to the arson and fraud scheme. The skills and tools learned during this project can be applied to similar investigations and are valuable for anyone pursuing a career in digital forensics.
