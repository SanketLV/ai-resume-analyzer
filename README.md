# Resumind - AI Resume Analyzer

## Smart feedback for your dream job!

Resumind is a modern web application that uses AI to analyze resumes against specific job descriptions, providing detailed feedback and improvement suggestions to help job seekers optimize their applications for Applicant Tracking Systems (ATS) and human reviewers.

## Table of Contents

- [Features](#features)
- [Technology Stack](#technology-stack)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Development](#development)
  - [Building for Production](#building-for-production)
- [Usage](#usage)
  - [Authentication](#authentication)
  - [Uploading a Resume](#uploading-a-resume)
  - [Viewing Analysis Results](#viewing-analysis-results)
- [Architecture](#architecture)
  - [Project Structure](#project-structure)
  - [Key Components](#key-components)
  - [Data Flow](#data-flow)
- [AI Integration](#ai-integration)
- [Deployment](#deployment)
- [Contributing](#contributing)
- [License](#license)

## Features

- **Resume Upload**: Upload PDF resumes for analysis
- **Job-Specific Analysis**: Tailor analysis to specific job descriptions and titles
- **ATS Compatibility Check**: Evaluate how well your resume will perform with Applicant Tracking Systems
- **Comprehensive Feedback**: Get detailed analysis in multiple categories:
  - **Tone & Style**: Language, professionalism, and clarity
  - **Content**: Quality and relevance of information
  - **Structure**: Organization and formatting
  - **Skills**: Relevance and presentation of skills
- **Visual Scoring**: Easy-to-understand visual representation of scores
- **Actionable Suggestions**: Specific tips for improvement with detailed explanations
- **Resume Management**: Track and compare multiple resume submissions
- **User Authentication**: Secure access to your resume data

## Technology Stack

- **Frontend**: React 19 with TypeScript
- **Routing**: React Router 7
- **Styling**: TailwindCSS
- **State Management**: Zustand
- **PDF Processing**: PDF.js
- **File Upload**: React Dropzone
- **Authentication**: Puter authentication system
- **Storage**: Puter key-value store and file system
- **AI Integration**: Puter AI for resume analysis

## Getting Started

### Prerequisites

- Node.js (v18 or higher recommended)
- npm, yarn, or pnpm

### Installation

Clone the repository and install dependencies:

```bash
# Clone the repository
git clone https://github.com/yourusername/resumind.git
cd resumind

# Install dependencies
npm install
# or
yarn install
# or
pnpm install
```

### Development

Start the development server with hot module replacement:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
```

Your application will be available at `http://localhost:5173`.

### Building for Production

Create a production build:

```bash
npm run build
# or
yarn build
# or
pnpm build
```

## Usage

### Authentication

1. When you first access the application, you'll be redirected to the authentication page
2. Sign in or create an account to access the resume analysis features
3. Your resume data will be securely stored in your account

### Uploading a Resume

1. Navigate to the upload page by clicking "Upload Resume" on the homepage
2. Fill in the required information:
   - Company Name (e.g., "Microsoft")
   - Job Title (e.g., "Software Engineer")
   - Job Description (copy and paste from the job posting)
3. Upload your resume in PDF format using the file uploader
4. Click "Analyze Resume" to start the analysis process
5. The system will process your resume and provide feedback based on the job details

### Viewing Analysis Results

After analysis, you'll be redirected to the results page, which includes:

1. **Resume Preview**: A visual representation of your uploaded resume
2. **Overall Score**: A summary score based on all evaluation categories
3. **ATS Score**: How well your resume will perform with Applicant Tracking Systems
4. **Detailed Feedback**: Expandable sections for each evaluation category:
   - **Tone & Style**: Language, professionalism, and clarity
   - **Content**: Quality and relevance of information
   - **Structure**: Organization and formatting
   - **Skills**: Relevance and presentation of skills
5. Each category includes:
   - A score out of 100
   - Positive aspects of your resume
   - Areas for improvement with detailed explanations

## Architecture

### Project Structure

The application follows a modern React Router structure:

- `/app`: Main application code
  - `/components`: Reusable UI components
  - `/lib`: Utility functions and helpers
  - `/routes`: Page components and routing
- `/constants`: Configuration constants and AI instructions
- `/public`: Static assets
- `/types`: TypeScript type definitions

### Key Components

- **Home Page**: Displays a list of uploaded resumes
- **Upload Page**: Handles resume upload and initiates analysis
- **Resume Page**: Displays detailed analysis results
- **ATS Component**: Shows ATS compatibility score and suggestions
- **Details Component**: Provides detailed feedback in multiple categories
- **Summary Component**: Gives an overview of all scores

### Data Flow

1. User uploads a resume with job details
2. Resume is stored in the file system
3. PDF is converted to an image for preview
4. AI analyzes the resume against the job description
5. Analysis results are stored in the key-value store
6. Results are displayed to the user in a structured format

## AI Integration

Resumind uses AI to analyze resumes with a carefully crafted prompt that:

1. Positions the AI as an expert in ATS and resume analysis
2. Instructs it to analyze the resume against the specific job title and description
3. Encourages thorough, detailed feedback with honest scoring
4. Specifies a structured response format for consistent feedback
5. Evaluates multiple aspects of the resume:
   - ATS compatibility
   - Tone and style
   - Content quality and relevance
   - Structure and formatting
   - Skills presentation and relevance

## Deployment

### Docker Deployment

To build and run using Docker:

```bash
docker build -t resumind .

# Run the container
docker run -p 3000:3000 resumind
```

The containerized application can be deployed to any platform that supports Docker, including:

- AWS ECS
- Google Cloud Run
- Azure Container Apps
- Digital Ocean App Platform
- Fly.io
- Railway

### DIY Deployment

If you're familiar with deploying Node applications, the built-in app server is production-ready.

Make sure to deploy the output of `npm run build`

```
├── package.json
├── package-lock.json (or pnpm-lock.yaml, or bun.lockb)
├── build/
│   ├── client/    # Static assets
│   └── server/    # Server-side code
```

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

---

Built with ❤️ using React Router and AI technology.