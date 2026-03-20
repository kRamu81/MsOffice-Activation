## Fix Microsoft Office Activation using OSPPREARM

### Step 1: Open Command Prompt as Administrator

1. Press **Windows Key**
2. Search **cmd**
3. Right-click **Command Prompt**
4. Click **Run as Administrator**

---

### Step 2: Open Office Installation Folder

1. Open **File Explorer**
2. Navigate to:

```
C:\Program Files\Microsoft Office\Office16
```
 <img width="1008" height="415" alt="image" src="https://github.com/user-attachments/assets/32a6efc9-7c80-432f-99bf-151232e691bd" />


3. Copy the **folder path** from the address bar.

---

### Step 3: Navigate to Office Folder in CMD

In Command Prompt type:

```
cd "C:\Program Files\Microsoft Office\Office16"
```
<img width="567" height="26" alt="image" src="https://github.com/user-attachments/assets/e6e0172e-990f-4eff-aba7-16621ad700ae" />

---

### Step 4: Check Office License Status

Run the following command:

```
cscript ospp.vbs /dstatus
```
<img width="964" height="422" alt="image" src="https://github.com/user-attachments/assets/94e6a878-267b-4bcf-bf05-c14832b3648d" />

This command will display the **license information**.

Look for the line:

```
SKU ID: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
```

Copy the **SKU ID**.

---

### Step 5: Rearm Office

Run the following command using the copied **SKU ID**:

```
OSPPREARM <SKU_ID>
```

Example:

```
OSPPREARM 6912a74b-a5fb-401a-bfdb-2e3ab46f4b02
```

---

### Step 6: Successful Message

If successful, you will see:

```
Microsoft Office rearm successful.
```
<img width="840" height="104" alt="image" src="https://github.com/user-attachments/assets/32466d1d-b947-4bfb-ad38-5dc75e1d2207" />

Restart Microsoft Office applications.

---

### Notes

* Works for **Office Volume License (KMS Client)** versions.
* Rearm resets the **Office activation grace period**.
* Rearm can only be used a limited number of times.
