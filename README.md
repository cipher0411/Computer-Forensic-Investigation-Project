# Computer-Forensic-Investigation-Project

> **Disclaimer:** This project is a fictional case created for demonstration purposes. It is not related to any real-life events or investigations. The case and evidence used here are purely for illustrative purposes and should not be interpreted as real. This project is not intended for educational use and does not represent actual forensic analysis or criminal investigations.

## Objective

The objective of this forensic investigation was to thoroughly examine digital evidence related to a criminal activity involving arson and fraud. The investigation focused on acquiring and analyzing data from multiple sources, including mobile phones, solid-state drives (SSDs), and USB sticks. This case aimed to uncover evidence that could help establish the involvement of individuals in planning and executing a fire at a storage facility, resulting in a fatality and an insurance fraud scheme.

This investigation was conducted in strict compliance with the **Association of Chief Police Officers (ACPO)** guidelines, ensuring proper evidence handling and integrity throughout the process.

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

---

## Steps

### 1. Crime Scene Visit
**Objective:** To secure the crime scene, identify potential evidence, and document the environment for analysis while adhering to ACPO guidelines.

![image](https://github.com/user-attachments/assets/7b758a59-79fe-44d3-9606-d36743aa6cc3)


- **Documenting the Scene:**
  - Photographed and recorded the layout of the crime scene, focusing on areas of interest, including the storage facility, suspect's workstation, and any devices or storage media found.
  - Collected physical evidence, including mobile phones, an SSD, a USB stick, and handwritten notes, following strict evidence handling protocols.

- **Tagging Evidence:**
  - Each piece of evidence was assigned a unique identifier and placed in evidence bags with tamper-proof seals.
  - A detailed log was created, noting the date, time, location, and description of each item collected.

- **Transporting Evidence:**
  - The collected evidence was securely transported to the forensic lab while maintaining a proper chain of custody to prevent contamination or tampering.

---

### 2. Data Acquisition
**Objective:** To acquire data from the SSD and USB stick while ensuring data integrity using FTK Imager and write blockers.

![image](https://github.com/user-attachments/assets/40667468-0b35-41ef-9b3d-6a302b32e815)


- **Acquiring Data from the SSD:**
  - Attached the SSD to the write blocker to prevent data modification during the acquisition.
  - Connected the SSD to the computer and used FTK Imager to create a bit-for-bit image of the drive.
  - The forensic image was saved in the E01 format and hash values (MD5, SHA-1) were generated to verify data integrity.

- **Acquiring Data from the USB Stick:**
  - Similar procedure was followed for the USB stick using FTK Imager.
  - A forensic image of the USB drive was created and stored in a separate folder with appropriate hash values to verify its integrity.

---

### 3. Data Analysis
**Objective:** To analyze the forensic images from the SSD and USB stick using Autopsy and recover relevant evidence.

![image](https://github.com/user-attachments/assets/d56e232e-211e-47a6-857c-11d6f7e1fb31)



- **Loading Forensic Images into Autopsy:**
  - Opened Autopsy on the analysis workstation and created a new case for the investigation.
  - Added the forensic image files (E01) of the SSD and USB stick as data sources in Autopsy.

- **Examination of SSD Files:**
  - After ingestion, Autopsy was used to browse the file system on the SSD. I found several relevant files in the "Bad Items" folder.
  - Notably, Word documents named `Skype.exe`, `Order.docx`, `Task.docx`, and `Rob.docx` were discovered, all of which were encrypted with passwords.

- **Examination of USB Stick Files:**
  - Similar analysis was conducted on the USB stick, where encrypted documents were found in the "Bad Items" folder.
  - These documents contained valuable evidence linking the suspects to the crime, including plans to carry out the arson.

---

### 4. Decrypting Encrypted Files
**Objective:** To decrypt the encrypted Word documents found on the SSD and USB drive.

![image](https://github.com/user-attachments/assets/0c06c59b-9aa9-4e3d-b067-e5ff89445dc7)

- **Using John the Ripper for Password Cracking:**
  - The encrypted Word documents (`Skype.exe`, `Order.docx`, `Task.docx`, `Rob.docx`) were extracted and stored in a folder on Kali Linux.
  - John the Ripper was set up on a Kali Linux virtual machine to perform brute-force password cracking on the documents.

- **Cracking the Passwords:**
  - Using a wordlist (`rockyou.txt`), John the Ripper attempted to brute-force the passwords for the encrypted documents.
  - The process revealed the passwords, allowing access to the content of the documents, which contained critical communications and instructions for executing the crime.

---

### 5. Investigating Evidence
**Objective:** To analyze the decrypted documents and identify key evidence linking the suspects to the crime.

![image](https://github.com/user-attachments/assets/f8f90e29-800b-4cb2-87a1-d3402dff81e8)

- **Content Analysis of `Rob.docx`:**
  - The document revealed instructions to turn off safety measures and spill fuel in the storage facility, which was part of the plan to set it on fire.

- **Corroborating Evidence from the SSD:**
  - The analysis of the SSD's email folder revealed communication between the suspects, confirming the planning of the arson and fraud.

---

### 6. Reporting and Chain of Custody
**Objective:** To compile findings into a forensic report while ensuring the integrity of the evidence.

![image](https://github.com/user-attachments/assets/06526645-5988-45f8-b482-642d73b6e214)


- **Creating the Final Report:**
  - A detailed forensic report was generated, summarizing the findings from the SSD, USB stick, and decrypted documents.
  - All evidence was securely stored, and the chain of custody was meticulously documented to ensure the integrity of the evidence.

---

## Additional Images

![image](https://github.com/user-attachments/assets/081ba7c5-b46a-4e96-b90f-2d1478c82727)
![image](https://github.com/user-attachments/assets/d0085b63-a835-4453-867e-fe8c8877babf)
![image](https://github.com/user-attachments/assets/a4588003-a129-4529-891f-596dc95f17d9)
![image](https://github.com/user-attachments/assets/dd75bcc4-0725-4b96-9492-9123d3a25388)
![image](https://github.com/user-attachments/assets/49611cc3-366a-4f0f-9183-d980f324baa9)
![image](https://github.com/user-attachments/assets/c233d45c-911e-4dcc-80d9-1247763b0c4a)
![image](https://github.com/user-attachments/assets/4ea4395c-f228-4e75-a431-6b64a5b4802c)
![image](https://github.com/user-attachments/assets/692c46bc-d7cb-46f9-b93f-d9a1527dbd4b)
![image](https://github.com/user-attachments/assets/2ebc1a8b-dce8-4b89-8a61-df958fd8cccd)
![image](https://github.com/user-attachments/assets/dd0ade87-6acd-4dd1-8fd3-5764cdc048f4)
![image](https://github.com/user-attachments/assets/214a59d5-030b-40ef-9acd-fb05648c7536)
![image](https://github.com/user-attachments/assets/f0f508dd-5103-4321-97ef-2f964016b623)
![image](https://github.com/user-attachments/assets/0c489bc1-9952-4190-ae68-bc1f6d74fcfc)
![image](https://github.com/user-attachments/assets/c840170d-b572-485a-9d51-1c460e7b17a8)
![image](https://github.com/user-attachments/assets/95dcb96a-6e76-45ac-b817-a6221aa97322)
![image](https://github.com/user-attachments/assets/4579fd6d-72bb-4241-972d-b153102fa98f)
![image](https://github.com/user-attachments/assets/af966dbb-a4fe-4e37-b906-3f12482e689b)
![image](https://github.com/user-attachments/assets/afc8d561-87d5-497a-bd10-9325b60a9ab7)

---

## Conclusion

This forensic investigation successfully uncovered crucial evidence linking the suspects to the arson and fraud scheme. The skills and tools learned during this project can be applied to similar investigations and are valuable for anyone pursuing a career in digital forensics.
