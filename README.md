# 📚 Book Recommendation System

A simple web app built with Flask that recommends books based on user input.  
The recommendation model uses similarity scores calculated from book metadata.  

---

## 🚀 Features

- Users can enter a book name to get **top similar book recommendations**  
- Lightweight Flask backend serving HTML templates  
- Precomputed similarity and popularity data stored in `.pkl` files  
- Easy to deploy (e.g. on Render)  
- Clean UI with responsive navigation  

---

## 🧩 Repository Structure

```
.
├── app.py
├── book_recommender.ipynb
├── books.pkl
├── popular.pkl
├── pt.pkl
├── similarity_score.pkl
├── requirements.txt
└── templates/
    ├── index.html
    ├── recommend.html
    └── error.html
```

- **app.py** — main Flask application  
- **.pkl** files — precomputed data needed by the recommender  
- **templates/** — HTML templates for rendering pages  
- **book_recommender.ipynb** — notebook used for data processing & model building  

---

## 🛠 Setup Instructions

1. **Clone the repo**
   ```bash
   git clone https://github.com/Mayank-Pandey-Ji/Book-Recommendation-System.git
   cd Book-Recommendation-System
   ```

2. **(Optional) Use a Python virtual environment**
   ```bash
   python3 -m venv venv
   source venv/bin/activate   # on Linux / macOS
   venv\Scripts\activate      # on Windows
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Run the app locally**
   ```bash
   python app.py
   ```
   By default, visit `http://127.0.0.1:5000` in your browser.

---

## ☁️ Deployment on Render (or similar)

- Ensure `requirements.txt` lists all used packages  
- Create a `Procfile` with:
  ```
  web: gunicorn app:app
  ```
- Push your repo to GitHub, then connect to Render as a Web Service  
- Use Python 3 runtime, set start command to `gunicorn app:app`  
- If your `.pkl` files are large, consider hosting them externally (S3, GCS, etc.) or using Git LFS  

---

## 📦 Requirements Example

Your `requirements.txt` might include (depending on what your app uses):
```
Flask
gunicorn
pandas
numpy
scikit-learn
requests
```

---

## 🧠 How Recommendation Works

- Precompute similarity matrix between books (using e.g. cosine similarity)  
- Save it in `similarity_score.pkl`  
- When user inputs a book name:  
  1. Match it against existing titles  
  2. Pick top-N similar books from the similarity matrix  
  3. Return book details (title, author, cover) to front-end  

---

## 🙏 Contribution & Feedback

Feel free to:
- Improve UI / CSS / animations  
- Add more metadata (ratings, genres)  
- Use better models (e.g. embeddings, hybrid filtering)  
- Fix bugs or optimize loading times  

If you find issues, open an **Issue** or submit a **Pull Request**.

---

## 📄 License

Specify your license here (e.g. MIT, GPL).  
For example:

```
MIT License  
© 2025 Mayank Pandey
```

---

## 🔗 Links & Acknowledgements

- Based on “Book Recommendation System” tutorials and datasets  
- Thanks to open-source libraries: Flask, pandas, scikit-learn  

---

**Enjoy recommending books! 📖**
