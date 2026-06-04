# AI-Powered Job Portal

A full-stack job portal with AI-driven resume matching, cover letter generation, and real-time job search powered by Indeed and Anthropic Claude.

## Features

- **Job Search with Filters** — Search jobs by keyword/location with date filters: Last 24 hours, 3 days, 7 days, 10 days
- **Resume Match Score** — Calculates a % match score for each job based on matched and missing skills from your profile
- **AI Cover Letter Generator** — Generates a personalised cover letter using the Anthropic Claude API
- **One-Click Apply** — Instantly generates a cover letter and shows the Apply Now link
- **Profile Sidebar with Skills Cloud** — Displays your profile, stats, and a visual skills cloud

## Tech Stack

| Layer    | Technology                          |
|----------|-------------------------------------|
| Frontend | HTML, CSS, Vanilla JavaScript       |
| Backend  | Python (http.server)                |
| Jobs API | Indeed MCP / Indeed API             |
| AI       | Anthropic Claude API (claude-sonnet-4-6) |

## Project Structure

```
job-portal-features/
├── job_portal.html       # Main frontend UI
├── job_portal.css        # Styles
├── job_portal_server.py  # Python backend server
└── README.md
```

## Getting Started

### Prerequisites

- Python 3.8+
- Anthropic API key

### Installation

```bash
git clone https://github.com/ermaneeshtiwari/job-portal-features.git
cd job-portal-features
pip install anthropic
```

### Configuration

Set your Anthropic API key as an environment variable:

```bash
export ANTHROPIC_API_KEY=your_api_key_here
```

### Run the Server

```bash
python job_portal_server.py
```

Then open your browser at:

```
http://127.0.0.1:8000
```

## Usage

1. **Search Jobs** — Enter a job title and location, then apply date filters to narrow results
2. **View Match Score** — Click any job to see your resume match % with matched and missing skills highlighted
3. **Generate Cover Letter** — Click "Generate AI Cover Letter" to get a tailored cover letter
4. **One-Click Apply** — Use the Apply Now button to open the job application directly

## API Endpoints

| Endpoint           | Method | Description                        |
|--------------------|--------|------------------------------------|
| `/api/jobs`        | GET    | Search jobs with filters           |
| `/api/cover-letter`| POST   | Generate AI cover letter           |

## Contributing

Feel free to open issues or submit pull requests to improve the portal.
