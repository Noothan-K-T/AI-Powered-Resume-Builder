# AI Resume Builder

A full-stack web application that uses AI to generate professional, ATS-friendly resumes. Users can sign up, log in, generate resumes using AI, select templates, edit, save, and download resumes as PDF.

## Features

- User authentication (sign up, login)
- AI-powered resume generation (via Together API)
- Multiple resume templates
- Save and manage resume templates
- Download resumes as PDF
- Responsive and modern UI

## Project Structure

```
.vscode/
backend/
  components/
  config/
  controllers/
  models/
  pdfs/
  public/
  routes/
  services/
  views/
  .env
  package.json
  server.js
```

## Getting Started

### Prerequisites

- Node.js (v18+ recommended)
- MongoDB instance (local or remote)

### Setup

1. **Clone the repository**

   ```sh
   git clone https://github.com/yourusername/ai-resume-builder.git
   cd ai-resume-builder/backend
   ```

2. **Install dependencies**

   ```sh
   npm install
   ```

3. **Configure environment variables**

   Edit `backend/.env` with your MongoDB URI and Together API key:

   ```
   MONGO_URI=your_mongodb_uri
   JWT_SECRET=your_jwt_secret
   PORT=5000
   TOGETHER_API_KEY=your_together_api_key
   ```

4. **Start the server**

   ```sh
   npm run dev
   ```

   The backend runs at [http://localhost:5000](http://localhost:5000).

### Usage

- Visit [http://localhost:5000](http://localhost:5000) in your browser.
- Sign up or log in.
- Enter your resume details and select a template.
- Generate, edit, save, and download your resume.

## Technologies Used

- Node.js, Express.js
- MongoDB, Mongoose
- EJS templating
- Together API (for AI resume generation)
- Puppeteer (for PDF generation)
- Axios, bcryptjs, jsonwebtoken

## Folder Overview

- `components/` – React components (if using React)
- `config/` – Database configuration
- `controllers/` – Express route controllers
- `models/` – Mongoose models ([User](backend/models/User.js), [Template](backend/models/Template.js))
- `public/` – Static assets (CSS, images)
- `routes/` – Express routes ([authRoutes](backend/routes/authRoutes.js))
- `services/` – Service modules ([authService](backend/services/authService.js))
- `views/` – EJS templates ([home.ejs](backend/views/home.ejs), [index.ejs](backend/views/index.ejs), etc.)

## API Endpoints

- `POST /api/auth/register` – Register user
- `POST /api/auth/login` – Login user
- `POST /generate-resume` – Generate resume HTML via AI
- `POST /save-as-template` – Save resume template
- `POST /download-pdf` – Download resume as PDF
- `GET /get-templates?username=...` – Get saved templates
- `DELETE /delete-template/:id` – Delete a template

## License

MIT

## Credits

- [Together API](https://www.together.ai/)
- [jsPDF](https://github.com/parallax/jsPDF)
- [Font Awesome](https://fontawesome.com/)

---

**For any issues or contributions, please open an issue or pull request!**
