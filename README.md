# Metadata-Extraction-using-ExifTool-log2timeline-and-Hidden-Data-Search-using-Steganography-Tools
## AIM:
To extract metadata, perform timeline analysis, and search for hidden data using forensic tools like ExifTool, log2timeline, and steganography detection tools.

## DESIGN STEPS:
### Step 1:
Use exiftool to extract metadata from files such as images, documents, and videos.

### Step 2:
Use log2timeline and plaso to create and analyze event timelines from system logs and file metadata.

### Step 3:
Apply steganography detection tools like steghide, zsteg, or binwalk to uncover hidden data in media files.

## PROGRAM:
Metadata and Timeline Forensics, Steganography Analysis Steps
## OUTPUT:
### ✅ A. Using ExifTool – for file metadata
- **📦 Install:**
```bash
sudo apt update
sudo apt install exiftool -y
```
- **📂 Extract metadata from a file:**
```bash
exiftool image.jpg
```
- **📁 Batch process a folder:**
```bash
exiftool -r /path/to/folder
```
- **📌 Useful flags:**
  
- ```-G: Show metadata group```

- ```-time:all: Show only timestamps```

- ```-GPSLatitude -GPSLongitude: Extract GPS data```
![1](https://github.com/user-attachments/assets/ea6237c8-0614-4d52-a2b1-83c132856531)
### install log2timeline
```
sudo apt install plaso -y
```

```
sudo apt install steghide -y
```
- **Embed data**
```
steghide embed -cf /home/kali/Downloads/wallpaper.jpg -ef /home/kali/Downloads/secret.txt
```
![2](https://github.com/user-attachments/assets/db1f07c3-2346-4535-91c8-610a5c0335e5)
- **Extract hidden data:**
```
steghide extract -sf hidden.jpg

```
![3](https://github.com/user-attachments/assets/551e3b0a-0b6d-4f31-8e2b-40b9b3b2da29)
### Using binwalk – for file analysis
```bash
sudo apt install binwalk -y
binwalk suspicious.jpg
```
```bash
binwalk /home/kali/Downloads/wallpaper.jpg
```
![4](https://github.com/user-attachments/assets/4fb2c773-2dfd-4fb1-b5fc-4d33459b2b87)


## RESULT:
Metadata was successfully extracted, timeline analysis was completed, and hidden data was identified using steganography tools.

