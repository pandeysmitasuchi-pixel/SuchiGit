# SuchiGit
# Travel Memory App Deployment on AWS

## Overview
This project demonstrates deploying a **MERN stack Travel Memory application** on AWS using a **3-Tier Architecture**:
- **Frontend (React)** → EC2 + Nginx
- **Backend (Node.js)** → EC2 + Nginx
- **Database (MongoDB Atlas)** → Managed cloud DB
- **Load Balancing** → AWS ALB
- **Domain Management** → Cloudflare + GoDaddy

## Architecture
1. User → `suchismita.co.in` (Cloudflare DNS)
2. Frontend Load Balancer → Frontend EC2 instances
3. React app communicates with Backend via `backend.suchismita.co.in`
4. Backend Load Balancer → Backend EC2 instances
5. Node.js connects to MongoDB Atlas cluster

## Deployment Steps
1. **Backend Setup**
   - Clone repo, configure `.env`, run Node.js, set up Nginx reverse proxy.
2. **Frontend Setup**
   - Clone repo, update `url.js`, run React, set up Nginx reverse proxy.
3. **Scaling**
   - Create AMIs, launch replicas, whitelist IPs in MongoDB Atlas.
4. **Load Balancing**
   - Create Target Groups & ALBs for frontend & backend.
5. **Domain Setup**
   - Configure Cloudflare CNAME records for frontend & backend.

## Deliverables
- Fully functional app at: [http://suchismita.co.in](http://suchismita.co.in)
- Backend domain: [http://backend.suchismita.co.in](http://backend.suchismita.co.in)
- MongoDB Atlas cluster storing travel memories.

## Submission
- Code pushed to GitHub: [SuchiGit](https://github.com/pandeysmitasuchi-pixel/SuchiGit.git)
- Documentation includes screenshots & architecture diagram.

