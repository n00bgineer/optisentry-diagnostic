# OptiSentry Diagnostic Server

![OptiSentry Application](https://res.cloudinary.com/dgu9rv3om/image/upload/v1691673076/optisentry/report_light_desktop.png)

**OptiSentry** is an open-source application performance and security monitoring system. Currently, for any given web application, it generates a report consisting of two parts:

1. Performance analysis, which contains the web application's performance report generated against one of OptiSentry's diagnostic servers running on a cloud instance deployed at a specific location (e.g., Singapore, London, Oregon, N. Virginia). The performance analysis is conducted using Google's `lighthouse` tool running on a headless browser of the rendering engine (i.e. webkit, chromium or firefox) or viewports of your choice.
2. Security analysis (WIP)

This repository contains the diagnostic server for the OptiSentry system. The **diagnostic server** generates the performance & security report for an application on a cloud instance deployed.

## Manual setup

---

## Getting Started

To set up the diagnostic server locally, follow the instructions below:

### Prerequisites

Make sure you have the following software installed on your machine:

- Node.js (LTS)
  ```
  node -v
  ```
- npm (Node Package Manager)

  ```
  npm -v
  ```

- traceroute
  ```
  sudo apt-get install traceroute
  ```
- Chromium/Chrome browser

  ```
  sudo apt install -y chromium-browser
  ```

### Installation

```
# Clone the repository to your local machine
git clone https://github.com/n00bgineer/optisentry-diagnostics.git ./diagnostic

# Change into the project directory
cd diagnostic

# Install the dependencies
npm install
```

### Configuration

The server requires a configuration file to run properly. Create a file named .env in the root directory of the project and define the following environment variables:

```
PORT=3000 # The port on which the server should listen
```

### Starting the Server

To start the server, run the following command:

```
npm start
```

The server will start running on the specified port (default: 3000). You can access it via http://localhost:3000.

## Automated Setup (Setup)

---

🚧 TBD

## API Endpoints

---

The diagnostic server provides the following API endpoints:

```
GET /api/status: Check if the server is running and responsive.
POST /api/report: Submit a report generation request to the server.
```

## API Documentation

---

For detailed information about each endpoint and how to use them, refer to the API documentation. The documentation is available at http://localhost:3000/api-docs when the server is running.

## Contributing

---

Contributions are welcome! If you find any issues or want to add new features, please open an issue or submit a pull request to the GitHub repository.

Before contributing, please read the contribution guidelines. If you have any questions or need assistance, please contact our support team at `n00bgineer@protonmail.com`.
