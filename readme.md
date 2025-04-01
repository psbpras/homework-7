Docker and Python

# QR Code Generator with Docker

This project generates a QR code that links to my GitHub homepage using Python inside a Docker container.

## **Generated QR Code**
Scan this QR code with your phone camera to visit my GitHub profile:

https://github.com/psbpras/homework-7/blob/main/QRCode_20250401160132.png

## **Project Setup & Execution**
### **1. Build the Docker Image**
```sh
docker build -t my-qr-app .
```

### **2. Run the Container**
```sh
docker run -d --name qr-generator my-qr-app
```

### **3. View Logs**
Check logs to verify QR code creation:
```sh
docker logs qr-generator
```

### **4. Retrieve the QR Code Image**
```sh
docker cp qr-generator:/app/qr_codes/github_qr.png .
```

### **5. Open the QR Code**
- **Windows:** Double-click `github_qr.png`
- **Mac/Linux:** Use `open github_qr.png` or `xdg-open github_qr.png`

## **Docker Commands Reference**
### **View Running Containers**
```sh
docker ps
```
### **Stop Container**
```sh
docker stop qr-generator
```
### **Remove Container**
```sh
docker rm qr-generator
```
### **Remove Image**
```sh
docker rmi my-qr-app
```

## **QR Code Generation Log**
Below is a screenshot of the logs confirming successful QR code creation:

https://github.com/psbpras/homework-7/blob/main/QRCode_20250401160132.png

---
🚀 **Now scan the QR code and check out my GitHub!**

