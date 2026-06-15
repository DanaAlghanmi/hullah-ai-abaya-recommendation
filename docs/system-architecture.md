# System Architecture

This document provides a high-level, conceptual overview of Hullah's architecture. No source code, configuration, or implementation details are included.

## Architectural Layers

Hullah is organized into **three main layers**: Frontend, Backend, and AI Model.

### 1. Frontend Layer

The frontend is the mobile interface through which users interact with the application. Through this layer, users can:

- Manually enter measurements or upload a photo for analysis
- View their body shape and measurement summary
- Browse and select personalized abaya recommendations
- Save selections and export a measurement/recommendation summary

### 2. Backend Layer

The backend acts as the bridge between the mobile interface and the AI model. Its responsibilities include:

- Managing data flow between the app and the AI services
- Exposing API endpoints for measurement processing and recommendations
- Handling image transfer for analysis
- Coordinating communication with the application's database

### 3. AI Model Layer

The AI layer is responsible for the application's core intelligence:

- **Pose Estimation** — detects body keypoints from an uploaded image.
- **Measurement Conversion** — converts pixel-based keypoint distances into centimeter measurements using the user's height as a scale reference.
- **Body Shape Classification** — classifies the user into one of five body shape categories using a trained classification model.
- **Girth Prediction** — estimates body girth measurements (e.g., bust, waist, hip) using a trained regression model.
- **Recommendation Engine** — matches the classified body shape against a curated catalog of abaya designs to generate personalized recommendations.

## High-Level Data Flow

1. User provides input (manual measurements or a photo) via the mobile app.
2. The app sends the input to the backend API.
3. If a photo was provided, the AI layer performs pose estimation and measurement extraction.
4. Measurements are classified into a body shape using a trained model.
5. The recommendation engine selects suitable abaya designs from the catalog based on the body shape.
6. Results (measurements, body shape, and recommendations) are returned to the app and displayed to the user.
7. The user can export a summary report of their results.

## Technology Categories Used

At a high level, the following categories of technologies were used during development (general-purpose tools and frameworks, not project-specific configuration):

| Category | Examples of Technology Used |
|---|---|
| Programming Language | Python (AI/backend logic) |
| Mobile Development | Flutter / Dart |
| Backend Framework | FastAPI |
| AI / Computer Vision | YOLOv8 (pose estimation) |
| Machine Learning | Scikit-learn (classification), gradient-boosted regression models (girth prediction) |
| Cloud Database & Auth | Firebase |
| Hosting / Deployment | Cloud-based API hosting |
| Development Tools | Android Studio, Visual Studio Code, Git/GitHub |

> These represent the **categories and general tools** used in the project for transparency purposes. Implementation details, configurations, and source code are intentionally excluded from this repository.
