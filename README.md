# AWS IAM Security Best Practices 🚀

## **📌 Project Overview**
This project demonstrates **IAM Security Best Practices** by implementing **Least Privilege Access**, **Multi-Factor Authentication (MFA)**, and **AWS CloudTrail Logging**. These are **critical for cloud security** and will showcase your AWS security skills to potential employers.

## **🛠 AWS Services Used**
- **IAM (Identity and Access Management)** → Secure user & role access
- **AWS CloudTrail** → Monitor and log API activities
- **Amazon S3** → Store CloudTrail logs
- **AWS CLI** (optional) → Manage IAM users & policies

---

## **🚀 Step-by-Step Implementation**

### **1️⃣ Create an IAM User with Least Privilege**
1. **Go to AWS IAM Console** → [IAM Users](https://console.aws.amazon.com/iam/)
2. **Click "Create user"** → Name it `security-user`.
3. **Disable Console Access** (Only allow CLI/API access).
4. **Attach Policy:** `AmazonEC2ReadOnlyAccess`.
5. **Save and Test** by logging in with this user.

📌 **Why?** IAM users should have **only the permissions they need** (Least Privilege Principle).

---

### **2️⃣ Enable Multi-Factor Authentication (MFA)**
1. **Go to IAM Console** → Click on `security-user`.
2. **Click "Security Credentials"** → Enable MFA.
3. **Use Google Authenticator/Authy** → Scan the QR Code.
4. **Enter the MFA Code** and Save.

📌 **Why?** MFA adds an extra layer of security by requiring a one-time password from an authenticator app.

🔹 **Screenshot:** `screenshots/MFA-setup.png`

---

### **3️⃣ Configure IAM Password Policy**
1. **Go to IAM Console** → Account Settings.
2. **Set password policies:**
   - ✅ **Require uppercase letters**
   - ✅ **Require numbers & special characters**
   - ✅ **Force password expiration (90 days)**
   - ✅ **Prevent password reuse (last 3 passwords)**

📌 **Why?** Strong password policies help protect against credential theft.

🔹 **Example Policy File:** [`policies/password-policy-example.txt`](policies/password-policy-example.txt)

---

### **4️⃣ Enable CloudTrail for Security Monitoring**
1. **Go to AWS CloudTrail Console** → Create a new Trail.
2. **Store logs in an S3 Bucket** (`aws-security-logs`).
3. **Enable Log File Validation** (for integrity checking).
4. **Enable CloudWatch Logs** to receive alerts for security events.
5. **Verify logs in CloudTrail.**

📌 **Why?** CloudTrail helps track who accessed AWS resources and detects security issues.

🔹 **Screenshot:** `screenshots/CloudTrail-logs.png`

---

## **📊 Expected Outcomes**
✅ IAM user with **least privilege access** configured correctly.  
✅ MFA enabled for IAM users.  
✅ Secure **password policies** enforced.  
✅ CloudTrail logging enabled for security monitoring.  

---

## **📂 Project Files & Documentation**
- 📄 `README.md` → This documentation
- 📄 `setup-guide.md` → Step-by-step CLI setup (for automation)
- 📂 `policies/` → Contains example IAM policies
- 📂 `screenshots/` → Contains setup images

---

## **🎯 Next Steps**
🚀 **Extend this project by:**
- Enabling **AWS Config** to track IAM policy changes.
- Automating IAM policy enforcement using **AWS Lambda**.
- Sending **security alerts via SNS** when an IAM change is detected.

---

## **📢 Share & Showcase Your Work**
1. **Upload this project to GitHub**.
2. **Write a LinkedIn post** about what you learned.
3. **Create a short video demo** showing IAM Security setup.

**🔗 Follow me on GitHub: [github.com/teranr](https://github.com/teranr/)** 🚀
