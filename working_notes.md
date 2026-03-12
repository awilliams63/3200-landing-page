Purpose

This document contains internal development notes for the Amanda Williams professional landing page project. It is intended to help developers or AI assistants understand the context of the project, current implementation, deployment setup, and areas for improvement.

This file is not intended for public viewing and should be used strictly as a working reference.

Project Overview

This project is a professional personal landing page for Amanda Williams, created for the course BAIS:3300 — Digital Product Management at the University of Iowa.

The goal of the project is to create a simple, professional website that:

Presents Amanda’s background to recruiters and hiring managers

Highlights academic achievements and professional experience

Demonstrates technical and analytical capabilities

Provides a polished online professional presence beyond a resume

The landing page includes the following sections:

Hero section

Bio section

Skills section

Featured projects section

Contact section

The project is intentionally kept simple and uses only HTML and CSS.

Repository

GitHub repository:

https://github.com/awilliams63/3200-landing-page

This repository contains all files required to deploy the landing page.

Deployment

The site is deployed using Azure Static Web Apps.

Azure deployment URL:

https://yellow-sand-02a106c1e.4.azurestaticapps.net

Custom domain:

https://awilliams63.me

Deployment is handled automatically through GitHub Actions CI/CD using the Azure Static Web Apps workflow.

Workflow file:

.github/workflows/azure-static-web-apps.yml

Key configuration:

app_location: "/"
api_location: ""
output_location: ""

Because the site is a static HTML/CSS project, there is no build step required.

Technology Stack
Technology	Purpose
HTML5	Website structure
CSS3	Styling and layout
Azure Static Web Apps	Hosting and deployment
GitHub Actions	Continuous deployment
GitHub	Version control

No frameworks or JavaScript libraries are currently used.

Current Site Structure
3200-landing-page
│
├── index.html
├── styles.css
├── PRD.md
├── STANDARDS.md
├── README.md
├── WORKING_NOTES.md
│
└── images
    └── headshot.jpg
File explanations

index.html
Main landing page containing all sections of the website.

styles.css
CSS styling for layout, typography, and visual structure.

PRD.md
Product Requirement Document describing the goals and requirements of the landing page.

STANDARDS.md
Defines coding standards and design guidelines for the project.

README.md
Public-facing repository documentation.

WORKING_NOTES.md
Internal documentation and development notes.

images/headshot.jpg
Professional headshot used in the hero section.

Website Content
Hero Section

Displays:

Name: Amanda Williams

Tagline: Turning Data Into Strategic Decisions

Professional headshot

Purpose: provide an immediate professional identity and value proposition.

Bio Section

Summary of Amanda’s academic background:

University of Iowa student pursuing:

B.B.A., Business Analytics & Information Systems

B.B.A., Finance

B.S., Exercise Science

Minor:

Therapeutic Recreation

Academic highlights:

GPA: 3.94

Honors student

Graduation:

May 2026

Focus areas:

analytics

strategy

consulting

sales and revenue strategy

Skills Section

Technical skills highlighted:

Advanced Excel

Python

SQL

Data Analysis

Data Visualization

Business and professional skills:

Presentation

Communication

Strategic thinking

These skills reflect Amanda’s ability to combine technical analytics with business decision making.

Featured Projects

Three professional experiences are presented as project-style highlights.

Huhtamaki — Commercial Career Program Intern

Key work:

Created executive dashboards from Circana datasets

Used Advanced Excel and Python

Applied database management concepts

Presented strategic insights to senior leadership

Iowa Athletix — Program Planning Intern

Key work:

Conducted data analysis for program development

Helped improve participant engagement

Assisted with operational planning

CarePro Health — Healthcare Administration Intern

Key work:

Analyzed departmental workflows

Contributed recommendations to improve efficiency

Participated in operational improvement initiatives

Known Issues
Domain configuration confusion

Initially the custom domain resolved to GitHub Pages instead of Azure.

This was resolved by updating DNS records to point to Azure Static Web Apps.

Extra HTML file

The repository originally contained:

Hello World index.html

This file caused confusion and was removed so that only:

index.html

remains as the default entry file.

Deployment Notes

Important rules for Azure Static Web Apps:

The project must include a root-level index.html.

The GitHub workflow must reference the correct location:

app_location: "/"

No build folder is required because this is a static site.

If index.html is missing or misnamed, Azure returns a 404 page.

Development Guidelines

Future edits should:

Keep the project simple and maintainable

Avoid adding unnecessary frameworks

Maintain semantic HTML structure

Keep styling centralized in styles.css

The site should remain lightweight and load quickly.

Future Improvements

Possible enhancements for future versions:

Add GitHub links to featured projects

Expand projects into detailed case study pages

Improve responsive design for smaller screens

Add additional styling improvements

Include optional downloadable resume

AI Assistant Notes

If an AI assistant is modifying this project:

Preserve the current file structure.

Do not introduce frameworks unless requested.

Keep code beginner-friendly for educational purposes.

Ensure any changes still deploy correctly through Azure Static Web Apps.

Last Updated

Project maintained by:

Amanda Williams
University of Iowa
BAIS:3300 — Digital Product Management
