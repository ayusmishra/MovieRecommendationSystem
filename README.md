# MovieRecommendationSystem
A hybrid movie recommendation engine that combines Computer Vision (Real-time Emotion Detection) with Collaborative Filtering. It curates content based on your current facial expression and historical viewing preferences. 🎭 🎥

# 🎭 Mood-Based Hybrid Recommendation System

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Library](https://img.shields.io/badge/Library-DeepFace%20%7C%20OpenCV-green)
![Status](https://img.shields.io/badge/Status-Prototype-orange)

**Don't just watch what you *liked*. Watch what you *feel*.**

This project is a Proof-of-Concept (PoC) for a multimodal recommendation engine that moves beyond static history. It integrates **Computer Vision** to detect the user's real-time emotional state and combines it with **Collaborative Filtering** to provide context-aware movie suggestions.

---

## 🚀 Key Features

* **👁️ The "Eye" (Emotion Recognition):** Uses `DeepFace` and `OpenCV` to analyze facial expressions via webcam in real-time (Happy, Sad, Neutral, etc.).
* **🧠 The "Brain" (Hybrid Logic):**
    * **Mood Congruence:** Filters genres to match your current emotional state.
    * **Era Preference:** Analyzes your history to determine if you prefer "Classic" (1900s) or "Modern" (2000s) cinema.
    * **Collaborative Filtering:** Uses Cosine Similarity to find users with similar tastes and ranks the final selection.
* **🔒 Privacy First:** Images are processed in RAM and immediately discarded. No facial data is stored.

---

## 🛠️ Architecture

The system follows a 3-step filtration pipeline:

1.  **Input:** Webcam Feed → Face Detection → **Emotion Label** (e.g., "Happy").
2.  **Filter Layer:**
    * *Mood Filter:* Removes conflicting genres (e.g., removes "Tragedy" if user is "Happy").
    * *History Filter:* Prioritizes the user's preferred cinematic era.
3.  **Ranking Layer:** Calculates similarity scores between the active user and the database to rank the final movie list.

---

## 📦 Tech Stack

* **Language:** Python 3.x
* **Computer Vision:** OpenCV, DeepFace
* **Data Manipulation:** Pandas, NumPy
* **Machine Learning:** Scikit-Learn (Cosine Similarity)
* **Environment:** Jupyter Notebook

---

## ⚡ Installation & Usage

1.  **Clone the Repository**
    ```bash
    git clone [https://github.com/your-username/mood-recommendation-system.git](https://github.com/your-username/mood-recommendation-system.git)
    cd mood-recommendation-system
    ```

2.  **Install Dependencies**
    ```bash
    pip install opencv-python deepface pandas scikit-learn matplotlib
    ```

3.  **Run the Notebook**
    Launch Jupyter Lab or Notebook and open `Mood_Recommender.ipynb`.
    ```bash
    jupyter notebook
    ```

4.  **Allow Camera Permissions**
    The system requires webcam access to detect your mood. Ensure your browser or terminal has permission to access the camera.

---

## 📊 Sample Output

**Scenario:** User looks "Happy" and has a history of watching 90s movies.

| Step | Output |
| :--- | :--- |
| **1. Vision** | `Detected Emotion: HAPPY` |
| **2. Era Check** | `Preference: CLASSIC (1900s)` |
| **3. Recommendation** | **1. The Lion King (1994)** <br> *Reason: Matches Happy Mood + Classic Era + High Community Rating* |

---

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.
1.  Fork the Project
2.  Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3.  Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4.  Push to the Branch (`git push origin feature/AmazingFeature`)
5.  Open a Pull Request

## 📄 License

Distributed under the MIT License. See `LICENSE` for more information.

---

*Built with 💻 and ☕ by [Your Name]*
