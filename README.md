
# AI-RadiologyPortal - Technical Documentation

## **Project Overview**
AI-RadiologyPortal is a web application designed for a radiology and sonography clinic. The system allows users to:
- Register and log in to their accounts.
- View previous radiology results and DICOM-format X-ray images.
- Access general healthcare tips and preparation guidelines for radiology and sonography.

---

## **Technology Stack**
### **Frontend:**
- Framework: **Next.js (React 18+)**
- Styling: **Tailwind CSS**
- State Management: **Zustand or Redux (Optional)**
- Authentication: **NextAuth.js or Firebase Auth**
- API Calls: **Axios / Fetch API**

### **Backend:**
- Framework: **FastAPI (Python 3.10+)**
- Database: **PostgreSQL / MongoDB**
- Authentication: **JWT-based Auth (PyJWT)**
- DICOM Processing: **pydicom, Orthanc Server (optional)**
- Storage: **AWS S3 / Azure Blob Storage (for DICOM images)**

### **DevOps & Deployment:**
- Containerization: **Docker**
- CI/CD: **GitHub Actions**
- Hosting: **Vercel (Frontend), AWS/GCP/Azure (Backend & Database)**
- Monitoring: **Prometheus + Grafana**
- Logging: **ELK Stack / CloudWatch**

---

## **Project Setup & Installation**
### **1️⃣ Clone the Repository**
```sh
 git clone https://github.com/your-username/AI-RadiologyPortal.git
 cd AI-RadiologyPortal
```

### **2️⃣ Install Dependencies**
#### **Frontend:**
```sh
 cd frontend
 pnpm install  # or npm install / yarn install
```
#### **Backend:**
```sh
 cd backend
 pip install -r requirements.txt
```

### **3️⃣ Environment Variables**
Create a `.env` file in the frontend and backend directories:
```env
NEXT_PUBLIC_API_URL=http://localhost:8000
NEXTAUTH_SECRET=your_secret_key
```
```env
DATABASE_URL=postgresql://user:password@localhost:5432/radiology_db
JWT_SECRET=your_jwt_secret
```

### **4️⃣ Running the Application**
#### **Start the Backend**
```sh
 cd backend
 uvicorn main:app --reload --host 0.0.0.0 --port 8000
```
#### **Start the Frontend**
```sh
 cd frontend
 pnpm run dev  # or npm run dev / yarn dev
```

---

## **Git & Collaboration Setup**
### **GitHub Repository Setup**
1. Create a repository on GitHub: **AI-RadiologyPortal**
2. Push your project:
```sh
 git init
 git remote add origin https://github.com/your-username/AI-RadiologyPortal.git
 git add .
 git commit -m "Initial commit"
 git push -u origin main
```

### **Adding a Collaborator** (For Private Repos with GitHub Pro/Team)
1. Go to **GitHub Repo** → **Settings** → **Manage Access**
2. Click **"Invite a collaborator"**
3. Enter the collaborator’s **GitHub username or email**
4. Click **"Send Invite"**

### **Collaborator Cloning Repo**
```sh
 git clone https://github.com/your-username/AI-RadiologyPortal.git
```

---

## **Future Enhancements**
- Implement AI-based radiology insights using **YOLOv8 / MONAI / Hugging Face**
- Add **WebRTC-based teleconsultation**
- Integrate **FHIR-compliant API** for interoperability

---

### **Contributors**
- **[Your Name]** - Project Lead
- **[Collaborator Name]** - Backend Developer

For queries, contact: []

# Using the Web App in Iran – Key Considerations

- ✅ Hosting & Infrastructure:

Some cloud providers (like AWS, Google Cloud, and Azure) restrict services in Iran due to sanctions.
Alternative solutions:
Self-hosted server (VPS from an Iranian provider like ParsOnline, Afranet, or Hetzner in Germany).
Iran-friendly cloud providers (e.g., Hetzner, OVH, or local hosting companies).
- ✅ Domain & Accessibility:

- .ir domains are Iran-specific and may help with local SEO, but they may be blocked internationally.
VPN Considerations: Some foreign-hosted apps might require a VPN for Iranian users.
- ✅ Payment Integration:

International payment gateways (Stripe, PayPal, etc.) do not work in Iran.
Local payment solutions: Use Zarinpal, Pay.ir, or other Shaparak-compliant gateways if needed.
- ✅ DICOM Support & Internet Speed

If DICOM files are large, ensure your Iranian hosting can handle high-speed transfers.
Use compressed DICOM formats to reduce bandwidth usage.
- ✅ Compliance & Regulations

Ensure your data storage and privacy policies follow Iranian healthcare regulations (HIPAA-equivalent laws).


