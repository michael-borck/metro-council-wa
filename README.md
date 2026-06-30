# Metro Council WA

A modern static site generator for the Washington State Metro Council that leverages Jinja templating to create professional HTML documentation and web pages. This project automates the generation of organizational documentation, policy materials, and public-facing web content.

## About

The Metro Council WA project provides an efficient solution for managing and publishing government documentation. By utilizing Jinja2 templating, the system enables consistent styling and structure across all generated pages while maintaining content in accessible markdown and YAML formats.

## Features

- **Jinja2 Template Engine**: Powerful templating system for consistent page generation
- **Static Site Generation**: Generate complete HTML documentation without server dependencies
- **Markdown Support**: Write content in markdown for easy editing and version control
- **Automated Deployment**: GitHub Actions workflow for continuous integration and deployment
- **Modular Content Organization**: Well-structured directories for policies, documentation, and employee information
- **Responsive Design**: CSS-based styling with modern web standards

## Installation

### Prerequisites

- Python 3.7 or higher
- pip (Python package manager)
- Git

### Setup

1. Clone the repository:
```bash
git clone https://github.com/michael-borck/metro-council-wa.git
cd metro-council-wa
```

2. Create and activate a virtual environment:
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

## Usage

### Generate Static Site

To generate the static HTML site from templates and content:

```bash
python generate.py
```

This command will process all Jinja templates and content files, outputting the final HTML to the `dist/` directory.

### Development Server

For local development and testing:

```bash
python -m http.server 8000 --directory dist
```

Then navigate to `http://localhost:8000` in your browser.

### Content Structure

Content is organized in the `content/` directory:

- **content/docs/**: Documentation and organizational information
  - **policy/**: Policy documents (Code of Conduct, Procurement, etc.)
  - **support/**: Support resources and guides
- **content/employees/**: Employee profiles and information
- **content/jobs/**: Job listings and recruitment information

### Creating New Content

1. Add markdown files to the appropriate content directory
2. Include front matter with metadata (title, date, etc.)
3. Run the generator to build the site

Example markdown structure:
```markdown
---
title: Policy Title
date: 2024-01-01
---

# Policy Title

Content goes here...
```

## Project Structure

```
metro-council-wa/
├── .github/
│   └── workflows/
│       └── pages.yml           # GitHub Actions deployment workflow
├── content/
│   ├── docs/
│   │   ├── policy/             # Policy documents
│   │   └── support/            # Support resources
│   ├── employees/              # Employee information
│   └── jobs/                   # Job listings
├── dist/                       # Generated static site
│   └── assets/                 # CSS, JS, images
├── templates/                  # Jinja2 templates
├── brief.yaml                  # Configuration file
├── LICENSE                     # MIT License
└── requirements.txt            # Python dependencies
```

## Configuration

The `brief.yaml` file contains site-wide configuration settings including:

- Site title and metadata
- Navigation structure
- Template settings
- Deployment options

Modify this file to customize site behavior and appearance.

## Deployment

The project includes a GitHub Actions workflow (`.github/workflows/pages.yml`) that automatically builds and deploys the site to GitHub Pages on each push to the main branch.

To enable automatic deployment:

1. Ensure GitHub Pages is enabled in repository settings
2. Set the source branch to the deployment branch
3. Push changes to trigger the workflow

## Technologies

- **Jinja2**: Template engine for Python
- **Python**: Build and generation scripts
- **CSS**: Styling and responsive design
- **JavaScript**: Interactive components
- **Markdown**: Content format
- **YAML**: Configuration and metadata
- **GitHub Actions**: CI/CD automation

## Contributing

Contributions are welcome! Please follow these guidelines:

1. Fork the repository
2. Create a feature branch for your changes
3. Ensure all content follows the existing structure
4. Test site generation locally before submitting
5. Submit a pull request with clear descriptions

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contact

For questions or issues regarding the Metro Council WA documentation site, please open an issue on the GitHub repository or contact the project maintainer.

---

**Project Owner**: [michael-borck](https://github.com/michael-borck)