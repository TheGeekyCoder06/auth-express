# auth-express

**Live Demo:**  
https://auth-five-taupe.vercel.app

## Description  
A complete authentication and user management backend built with Express.js.  
Includes protected routes, admin-only access, image upload/delete APIs, and JWT-based authentication.

## Tech Stack  
- Node.js  
- Express.js  
- MongoDB  
- JWT Authentication  
- Multer (file uploads)  
- Cloudinary / Local Uploads (based on helpers)  

---

## Project Structure  
controllers/
db/
helpers/
middleware/
models/
postman-tests/
routes/
uploads/
utils/
server.js
vercel.json
package.json

yaml
Copy code

---

## Features  
- User registration & login  
- JWT-based authentication  
- Protected routes (user & admin)  
- Change password  
- Image upload, retrieve & delete  
- Fetch all users (protected)  
- Fully deployable on Vercel  

---

## Environment Variables  
Create a `.env` file:

PORT=3000
MONGO_URI=your_mongodb_uri
JWT_SECRET=your_secret_key
CLOUD_NAME=your_cloudinary_cloud
API_KEY=your_cloudinary_api_key
API_SECRET=your_cloudinary_api_secret

yaml
Copy code

---

## Installation

```bash
git clone https://github.com/TheGeekyCoder06/auth-express
cd auth-express
npm install
npm start
Base URL
arduino
Copy code
https://auth-five-taupe.vercel.app
API Endpoints
Auth Routes
Method	Endpoint	Description
POST	/api/auth/register	Register a new user
POST	/api/auth/login	Login and receive JWT
POST	/api/auth/change-password	Change password (requires token)

Home Routes
Method	Endpoint	Description
GET	/api/home/welcome	Public welcome route
GET	/api/home/get-users	Get all users (protected)

Admin Routes
Method	Endpoint	Description
GET	/api/admin/welcome	Admin-only welcome route

Image Routes
Method	Endpoint	Description
POST	/api/images/upload	Upload image (protected)
GET	/api/images/get	Fetch all uploaded images
DELETE	/api/images/delete/:id	Delete specific image (protected)

Testing
A complete Postman collection is included under:

Copy code
postman-tests/
Import it into Postman to test login → protected routes → uploads → delete workflow.

Deployment
Already configured for Vercel using vercel.json.
Just set environment variables in the Vercel dashboard and deploy.

Author
Developed and maintained by Harshith M (TheGeekyCoder06).