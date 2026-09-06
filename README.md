# MERN Gallery App

A simple gallery application built with React (Vite), Node.js + Express, and MongoDB.
Images are uploaded to the backend and saved on the server's local disk (`server/uploads`).
Express serves that folder publicly, and MongoDB stores only the resulting image URL.

## Features
- Upload an image (stored on local disk, URL saved in MongoDB)
- Responsive gallery grid
- Full-screen image viewer                                 (modal)
- Previous / Next slider inside the viewer
- Delete an image (record removed from MongoDB, grid refreshes instantly)

## Setup

### Backend
```bash
cd server
npm install
cp .env.example .env  
npm run dev         
```

### Frontend

cd client
npm install
npm run dev


### Folder Structure

'''
gallery-app/
└── gallery-app/
    ├── client/
    │   ├── src/
    │   │   ├── components/
    │   │   │   ├── Gallery.jsx
    │   │   │   ├── UploadForm.jsx
    │   │   │   └── Viewer.jsx
    │   │   ├── api.js
    │   │   ├── App.jsx
    │   │   ├── index.css
    │   │   └── main.jsx
    │   ├── .env.example
    │   ├── index.html
    │   ├── package-lock.json
    │   ├── package.json
    │   └── vite.config.js
    ├── server/
    │   ├── middleware/
    │   │   └── upload.js
    │   ├── models/
    │   │   └── Image.js
    │   ├── routes/
    │   │   └── imageRoutes.js
    │   ├── uploads/
    │   │   └── .gitkeep
    │   ├── .env.example
    │   ├── package-lock.json
    │   ├── package.json
    │   └── server.js
    ├── .gitignore
    └── README.md  
    '''

## API
 Method  Endpoint         Description                                  

 POST    /api/images      Upload an image file, save it, store its URL 
 GET     /api/images      Get all images        
 DELETE  /api/images/:id  Delete one image                             
