# Features

Hullah combines AI-driven body analysis with a curated abaya catalog to deliver a personalized recommendation experience. Below is a summary of the application's core capabilities.

## 1. Flexible Measurement Input

Users can choose between two input methods:

- **Manual Entry** — directly enter body measurements (height, bust, waist, hips, shoulders, arm length, etc.).
- **Image-Based Analysis** — upload a single, clear, front-facing full-body photo. The photo must meet basic guidelines (proper lighting, full-body visibility, frontal angle) for accurate analysis.

## 2. AI-Powered Body Measurement Extraction

When a photo is uploaded:

- The system performs initial image processing.
- A pose estimation model detects key body landmarks (keypoints).
- Pixel-based distances between keypoints are converted into centimeter measurements using the user's height as a reference scale.

## 3. Body Shape Classification

Based on the extracted or entered measurements, Hullah classifies users into one of **five body shape categories**, developed in collaboration with abaya designers:

- Hourglass
- Pear
- Apple
- Rectangle
- Inverted Triangle

## 4. Personalized Abaya Recommendations

Once the body shape is determined, Hullah retrieves suitable abaya styles from a **curated catalog of real-world designs** collected from professional abaya designers. Each abaya design is pre-linked to the body shapes it best suits, ensuring relevant, designer-informed recommendations.

Abaya catalog attributes include style/cut, color, fabric, and the body shapes it is suitable for.

## 5. Measurement & Recommendation Summary

The application displays a clear summary including:

- The user's extracted/entered measurements
- The classified body shape
- The personalized abaya recommendations

Users can review, manage (e.g., remove items from their selection), and finalize this summary.

## 6. Exportable PDF Report

Users can generate a **downloadable, printable PDF report** summarizing their measurements and selected recommendations — making it easy to share with a tailor or abaya designer for custom tailoring.

## 7. User Accounts

The application supports user accounts (sign up / log in), allowing users to:

- Save their measurement history
- Revisit previous recommendations
- Manage their profile information

## 8. Support / Help Channel

A built-in support feature allows users to submit inquiries or report issues directly within the app.

## 9. Privacy-Conscious Design

To protect user privacy:

- Only **extracted measurements** are stored.
- **Original uploaded photos are not retained** by the system.

## 10. Bilingual, Accessible Interface

The application interface was designed to be intuitive and accessible to a broad demographic, supporting both Arabic and English, including right-to-left layout considerations.

---

> **Note:** The current version focuses on recommendation and measurement, not direct purchasing. See [`results.md`](results.md) for future plans, including e-commerce integration and virtual try-on.
