# FILMSTAR 
from flask import Flask, render_template

app = Flask(__FILMSTAR__)

# Static movie list
movies = [
    {
        "title": "Aapish – The Office 2025",
        "year": "2025",
        "poster": "https://i.postimg.cc/pdWq5GWL/aapish.jpg"
    },
    {
        "title": "Pokkhirajer Dim 2025",
        "year": "2025",
        "poster": "https://i.postimg.cc/ZKph0fp4/pokkhiraj.jpg"
    },
    {
        "title": "Grihapravesh 2025",
        "year": "2025",
        "poster": "https://i.postimg.cc/26gR8fnv/grihapravesh.jpg"
    }
]

@app.route('/')
def home():
    return render_template('index.html', movies=movies)

if __name__ == '__main__':
    app.run(debug=True)
<!DOCTYPE html>
<html>
<head>
    <title>FilmHub – Bengali Movies</title>
    <link rel="stylesheet" href="/static/style.css">
</head>
<body>
    <h1>📽️ Featured Bengali Movies</h1>
    <div class="movie-grid">
        {% for movie in movies %}
        <div class="movie-card">
            <img src="{{  https://images.app.goo.gl/HHcZFjiGAVkT3aUw7 }}" alt="{{ BORBAAD }}">
            <h3>{{ BORBAAD}}</h3>
            <p>{{ 2025 }}</p>
        </div>
        {% endfor %}
    </div>
</body>
</html>
body {
    background-color: #0d0d0d;
    color: #ffffff;
    font-family: Arial, sans-serif;
    text-align: center;
}

h1 {
    margin-top: 20px;
    color: #00ffcc;
}

.movie-grid {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    margin: 20px;
}

.movie-card {
    background-color: #1a1a1a;
    border-radius: 10px;
    margin: 15px;
    padding: 10px;
    width: 180px;
    transition: 0.3s;
}

.movie-card img {
    width: 100%;
    border-radius: 10px;
}

.movie-card:hover {
    box-shadow: 0 0 10px #00ffcc;
    transform: scale(1.05);
}
