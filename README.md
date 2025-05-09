# GitHub Actions Practice Project

A simple React application designed to demonstrate GitHub Actions integration. This project serves as a hands-on learning tool for setting up and understanding GitHub Actions workflows.

## Project Overview

This application is a React-based web interface that provides information about Git, GitHub, and GitHub Actions through a toggle-able help area. It's intentionally simple to keep the focus on the GitHub Actions implementation rather than application complexity.

## Features

- Interactive UI with toggle-able help section
- Information cards about Git, GitHub, and GitHub Actions
- Modern React implementation using hooks

## Technology Stack

- React 18
- Vite for build tooling and development server
- ESLint for code linting
- Vitest for testing

## Getting Started

### Prerequisites

- Node.js (latest LTS version recommended)
- npm or yarn

### Installation

1. Clone the repository
2. Install dependencies:
```bash
npm install
```

### Development

To start the development server:
```bash
npm run dev
```

### Testing

To run tests:
```bash
npm test
```

### Linting

To run linting:
```bash
npm run lint
```

### Build

To build for production:
```bash
npm run build
```

## Project Structure

- `/src` - Source code
  - `/components` - React components
  - `/assets` - Static assets like images
  - `/test` - Test files
- `/.github/workflows` - GitHub Actions workflow definitions
  - `deployment.yml` - CI/CD workflow for linting, testing, and deployment
  - `issues.yml` - Workflow for handling GitHub issues

## GitHub Actions Integration

This project demonstrates GitHub Actions for CI/CD and repository automation. The following workflows are included:

### Deployment Workflow (`deployment.yml`)

A comprehensive CI/CD pipeline that triggers on push events and includes:

1. **Lint Job** - Runs ESLint checks on the codebase
2. **Test Job** - Executes the test suite using Vitest (runs after linting passes)
3. **Deploy Job** - Builds the application and simulates a deployment (runs after testing passes)

The workflow uses job dependencies to create a sequential pipeline, demonstrating a typical CI/CD process.

### Issues Workflow (`issues.yml`)

A simple workflow that triggers on issue-related events. Currently, it outputs the GitHub event payload for demonstration purposes.

### Adding Your Own Workflows

To add your own workflow:

1. Create a new YAML file in the `.github/workflows` directory
2. Define the workflow name, trigger events, and jobs
3. Commit and push the file to your repository

GitHub will automatically detect and run your workflow based on the defined triggers. 

### Documentation Events that trigger workflows

[GitHub Actions - Events](https://docs.github.com/en/actions/writing-workflows/choosing-when-your-workflow-runs/events-that-trigger-workflows)

### Upload Artifact Action Link
[Upload Artifact]{https://github.com/actions/upload-artifact}
