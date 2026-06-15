# Results & Evaluation

Hullah was evaluated through three complementary types of testing: **unit testing**, **AI model evaluation**, and **usability testing**.

## Unit Testing

Automated unit tests (built with pytest) were used to validate critical modules, including:

- Body measurement calculations
- API endpoint behavior
- Image processing
- Body type classification logic

These tests, including edge-case simulations, confirmed the robustness of core system components.

## AI Model Evaluation

### Body Shape Classification

Two classification approaches were evaluated — one based on uploaded images, and one based on manually entered measurements:

| Model | Precision | Recall | F1-Score |
|---|---|---|---|
| Image-Based Classifier | 0.97 | 0.97 | 0.97 |
| Manual-Input Classifier | 0.96 | 0.96 | 0.96 |

Both classifiers demonstrated strong, consistent performance. The image-based model showed a slight edge, while the manual-input model serves as a reliable alternative when an image isn't available.

### Girth Measurement Accuracy

The girth prediction model was evaluated using Mean Absolute Error (MAE):

| Measurement | MAE (cm) |
|---|---|
| Bust Girth | 1.61 |
| Waist Girth | 0.20 |
| Hip Girth | 0.19 |

These low error values indicate high precision, particularly for waist and hip measurements.

## Usability Testing

Usability testing was conducted with five female participants from different age groups and technical backgrounds, each completing the test independently in their own environment, with no prior explanation (to simulate a first-time user experience).

### Tasks Evaluated

1. Sign up
2. Log in
3. Upload a body image
4. Enter measurements manually
5. Receive recommendations
6. Export summary as PDF

### Objective Results

- **Number of clicks:** Most tasks fell within ideal usability ranges. Simple tasks (log in, receive recommendations, export summary) averaged 4.5–5.5 clicks. The "Enter Measurements Manually" task (classified as complex) averaged 10 clicks — at the upper acceptable bound. "Sign up" slightly exceeded the ideal range for a medium-complexity task at 9 clicks.
- **Task duration:** Most tasks were completed within standard usability benchmarks — e.g., log in (~17 sec), receive recommendations (~15 sec), export summary (~25 sec), upload body image (~30 sec), sign up (~45 sec), and manual measurement entry (~65 sec, within the acceptable range for a complex task).

### Subjective Results

- **Ease of Use:** 80% of participants strongly agreed (and 20% agreed) that the app was easy to understand and use without assistance.
- **Satisfaction:** 80% of participants were satisfied or very satisfied with the app's performance.
- **Navigation:** All participants agreed or strongly agreed that they could navigate between pages with ease.

## Overall Conclusion

The combination of unit testing, AI model evaluation, and usability testing confirmed that Hullah:

- Performs accurate body measurement extraction and classification,
- Delivers relevant, body-shape-based abaya recommendations, and
- Provides an intuitive and accessible user experience across different user profiles.

## Future Work

Planned directions for extending Hullah include:

- **Data-Driven Body-Shape Classifier** — replacing rule-based logic with a more advanced machine learning model trained on an expanded dataset.
- **Multi-View Measurement Support** — allowing additional photo angles to further improve measurement accuracy.
- **Augmented Reality "Virtual Try-On"** — overlaying abaya designs onto a live camera view for real-time visualization.
- **E-Commerce & Tailor Integration** — connecting with retailers and tailoring services for a complete shopping experience.
- **Adaptive Recommendation Loop** — incorporating user feedback over time to personalize style suggestions further.
