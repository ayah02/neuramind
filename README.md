# NeuraMind 🧠

NeuraMind is an interactive, web-based ADHD screening tool designed to explore ADHD patterns in the female brain through multimodal machine learning. 

This project translates a complex Python-based dual-stream ML ensemble (Keras Neural Network + LightGBM) into a seamless, client-side JavaScript application. It is based on research and dataset analysis from the **WiDS Datathon 2025** at Al Yamamah University.

## ✨ Key Features

* **Interactive Screening:** A 20-question assessment mapped to DSM-5 criteria (Attention, Restlessness, Emotional Regulation, and Daily Life Impact).
* **Real ML Architecture:** Scores users using a JavaScript implementation of a dual-stream ensemble trained on 1,213 real fMRI brain connectivity cases.
* **Privacy-First Processing:** All scoring and calculations happen entirely in the browser. No personal data is sent to external servers unless the user explicitly opts into the anonymous research pool.
* **Dynamic Visualizations:** Generates a personalized symptom radar chart using Chart.js.
* **Clinical PDF Reports:** Users can download a professionally formatted PDF report of their results to share with healthcare providers (powered by jsPDF).
* **Researcher Dashboard:** A password-protected admin panel for researchers to view aggregated, anonymous community statistics and export data to CSV.
* **Dark/Light Mode:** Fully responsive UI with theme toggling.

## 🤖 The ML Model

The underlying model logic replicates a high-performing architecture designed during the WiDS 2025 Datathon:
* **Stream 1 (Neural Network):** Represents a Keras Dense model (256→128) applying weighted scoring to the four symptom domains.
* **Stream 2 (LightGBM):** Captures non-linear boosting and connectome interactions (e.g., attention × emotion).
* **Ensemble:** Combines the two streams with a 40% (NN) / 60% (LGBM) weight distribution, using an F1-optimized threshold of 0.53 to determine the final prediction.
* **Original Model Performance:** 80.8% CV accuracy, 94.1% recall, and 0.82 AUC.

## 🛠️ Tech Stack

* **Frontend:** HTML5, CSS3, Vanilla JavaScript
* **Libraries:** 
  * [Chart.js](https://www.chartjs.org/) (Radar visualizations)
  * [jsPDF](https://parall.ax/products/jspdf) (PDF report generation)

## 🚀 How to Run Locally

Since this is a client-side application, no backend setup is required.

1. Clone the repository:
   ```bash
   git clone [https://github.com/yourusername/neuramind.git](https://github.com/yourusername/neuramind.git)
