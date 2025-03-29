html__________________________________________________________________________________________________________________________
<!DOCTYPE html>
<html lang="hr">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Aplikacija za recenziranje knjiga</title>
  </head>
  <body>
    <div class="container">
      <h1>Recenzije knjiga</h1>

      <!-- Obrazac za unos -->
      <form id="review-form">
        <label for="book-title">Naziv knjige:</label>
        <input type="text" id="book-title" required />

        <label for="book-rating">Ocjena (1-10):</label>
        <input type="number" id="book-rating" min="1" max="10" required />

        <button type="submit">Pohrani recenziju</button>
      </form>

      <h2>Pohranjene recenzije</h2>

      <!-- Unaprijed pohranjene stavke -->
      <div class="review-item">
        <h3>Naslov knjige 1</h3>
        <p>Ocjena: 8</p>
        <p>Pohranjeno: 2025-03-28 10:00</p>
      </div>
      <div class="review-item">
        <h3>Naslov knjige 2</h3>
        <p>Ocjena: 9</p>
        <p>Pohranjeno: 2025-03-28 11:00</p>
      </div>
    </div>
  </body>
</html>

html+css_________________________________________________________________________________________________________________________
<!DOCTYPE html>
<html lang="hr">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Aplikacija za recenziranje knjiga</title>
    <link rel="stylesheet" href="style.css" />
  </head>
  <body>
    <div class="container">
      <h1>Recenzije knjiga</h1>

      <!-- Obrazac za unos -->
      <form id="review-form">
        <label for="book-title">Naziv knjige:</label>
        <input type="text" id="book-title" required />

        <label for="book-rating">Ocjena (1-10):</label>
        <input type="number" id="book-rating" min="1" max="10" required />

        <button type="submit">Pohrani recenziju</button>
      </form>

      <h2>Pohranjene recenzije</h2>

      <!-- Unaprijed pohranjene stavke -->
      <div class="review-item">
        <h3>Naslov knjige 1</h3>
        <p>Ocjena: 8</p>
        <p>Pohranjeno: 2025-03-28 10:00</p>
      </div>

      <div class="review-item">
        <h3>Naslov knjige 2</h3>
        <p>Ocjena: 9</p>
        <p>Pohranjeno: 2025-03-28 11:00</p>
      </div>
    </div>
  </body>
</html>
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
:root {
  --color-primary: #000;
  --color-secondary: #f1f1f1;
  --color-accent: #000;
  --spacing: 1rem;
}

body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
  background-color: white;
  color: var(--color-primary);
}

.container {
  max-width: 800px;
  margin: 0 auto;
  padding: var(--spacing);
}

h1,
h2 {
  text-align: center;
}

/* ----- Forma ----- */
form {
  background-color: var(--color-secondary);
  padding: 1rem;
  display: flex;
  flex-direction: column;
  gap: 0.5rem;
}

label {
  font-weight: bold;
}

input {
  padding: 0.5rem;
  border: 1px solid #999;
  font-size: 1rem;
}

button {
  padding: 0.6rem;
  background-color: var(--color-accent);
  color: white;
  border: none;
  font-weight: bold;
  cursor: pointer;
}

/* ----- Recenzije ----- */
.review-item {
  padding: 1rem 0;
  border-bottom: 1px solid #ccc;
}

.review-item h3 {
  margin: 0;
}

.review-item p {
  margin: 0.3rem 0;
}

.actions {
  display: flex;
  gap: 1rem;
  justify-content: flex-end;
  font-size: 0.9rem;
  margin-top: 0.5rem;
}

.actions span {
  cursor: pointer;
  text-decoration: underline;
}

/* ----- Mobilni dizajn (do 768px) ----- */
@media (max-width: 768px) {
  form {
    flex-direction: column;
  }

  form label {
    display: block;
  }

  input,
  button {
    width: 100%;
  }
}

/* ----- Desktop dizajn (od 769px naviše) ----- */
@media (min-width: 769px) {
  form {
    flex-direction: row;
    align-items: flex-end;
    gap: 1rem;
    padding: 1rem;
  }

  form label {
    display: none; /* skrivamo labele jer koristimo placeholdere */
  }

  #book-title {
    flex: 2;
    padding: 0.5rem;
    border: 1px solid #999;
    font-size: 1rem;
  }

  #book-rating {
    flex: 0 0 80px;
    padding: 0.5rem;
    border: 1px solid #999;
    font-size: 1rem;
  }

  button {
    flex: 0 0 auto;
    padding: 0.6rem 1rem;
    margin: 0;
  }
}

html+css+js_____________________________________________________________________________________________________________________
<!DOCTYPE html>
<html lang="hr">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Aplikacija za recenziranje knjiga</title>
    <link rel="stylesheet" href="style.css" />
  </head>
  <body>
    <div class="container">
      <h1>Recenzije knjiga</h1>

      <!-- Obrazac za unos -->
      <form id="review-form">
        <label for="book-title">Naziv knjige:</label>
        <input
          type="text"
          id="book-title"
          placeholder="Naziv knjige"
          required
        />

        <label for="book-rating">Ocjena (1-10):</label>
        <input
          type="number"
          id="book-rating"
          placeholder="Ocjena (1-10)"
          min="1"
          max="10"
          required
        />

        <button type="submit">Pohrani recenziju</button>
      </form>

      <h2>Pohranjene recenzije</h2>
    </div>

    <script src="script.js"></script>
  </body>
</html>
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
:root {
  --color-primary: #000;
  --color-secondary: #f1f1f1;
  --color-accent: #000;
  --spacing: 1rem;
}

body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
  background-color: white;
  color: var(--color-primary);
}

.container {
  max-width: 800px;
  margin: 0 auto;
  padding: var(--spacing);
}

h1,
h2 {
  text-align: center;
}

/* ----- Forma ----- */
form {
  background-color: var(--color-secondary);
  padding: 1rem;
  display: flex;
  flex-direction: column;
  gap: 0.5rem;
}

label {
  font-weight: bold;
}

input {
  padding: 0.5rem;
  border: 1px solid #999;
  font-size: 1rem;
}

button {
  padding: 0.6rem;
  background-color: var(--color-accent);
  color: white;
  border: none;
  font-weight: bold;
  cursor: pointer;
}

/* ----- Recenzije ----- */
.review-item {
  padding: 1rem 0;
  border-bottom: 1px solid #ccc;
}

.review-item h3 {
  margin: 0;
}

.review-item p {
  margin: 0.3rem 0;
}

.actions {
  display: flex;
  gap: 1rem;
  justify-content: flex-end;
  font-size: 0.9rem;
  margin-top: 0.5rem;
}

.actions span {
  cursor: pointer;
  text-decoration: underline;
}

.review-item.favorite {
  background-color: #fff9c4; /* žuta pozadina za favorite */
}

/* ----- Mobilni dizajn (do 768px) ----- */
@media (max-width: 768px) {
  form {
    flex-direction: column;
  }

  form label {
    display: block;
  }

  input,
  button {
    width: 100%;
  }
}

/* ----- Desktop dizajn (od 769px naviše) ----- */
@media (min-width: 769px) {
  form {
    flex-direction: row;
    align-items: flex-end;
    gap: 1rem;
    padding: 1rem;
  }

  form label {
    display: none;
  }

  #book-title {
    flex: 2;
    padding: 0.5rem;
    border: 1px solid #999;
    font-size: 1rem;
  }

  #book-rating {
    flex: 0 0 80px;
    padding: 0.5rem;
    border: 1px solid #999;
    font-size: 1rem;
  }

  button {
    flex: 0 0 auto;
    padding: 0.6rem 1rem;
    margin: 0;
  }
}
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
document.addEventListener("DOMContentLoaded", () => {
  const form = document.getElementById("review-form");
  const titleInput = document.getElementById("book-title");
  const ratingInput = document.getElementById("book-rating");
  const container = document.querySelector(".container");

  // Kreiraj spremnik za recenzije
  const reviewsContainer = document.createElement("div");
  container.appendChild(reviewsContainer);

  form.addEventListener("submit", (e) => {
    e.preventDefault();

    const title = titleInput.value.trim();
    const rating = parseInt(ratingInput.value.trim());

    if (!title || isNaN(rating) || rating < 1 || rating > 10) {
      alert("Molimo unesite ispravan naziv i ocjenu između 1 i 10.");
      return;
    }

    const reviewItem = document.createElement("div");
    reviewItem.classList.add("review-item");

    const date = new Date();
    const dateTimeStr =
      date.toLocaleDateString("hr-HR") +
      " " +
      date.toLocaleTimeString("hr-HR", { hour: "2-digit", minute: "2-digit" });

    reviewItem.innerHTML = `
            <h3>${title} - <em>${rating}</em></h3>
            <p>${dateTimeStr}</p>
            <div class="actions">
                <span class="favorite-btn">Dodaj u favorite</span>
                <span class="delete-btn">Obriši</span>
            </div>
        `;

    // Gumbi za favorite i brisanje
    const favBtn = reviewItem.querySelector(".favorite-btn");
    const delBtn = reviewItem.querySelector(".delete-btn");

    favBtn.addEventListener("click", () => {
      reviewItem.classList.toggle("favorite");
      const timestamp = reviewItem.querySelector("p");

      if (reviewItem.classList.contains("favorite")) {
        favBtn.textContent = "Ukloni iz favorita";
        if (!timestamp.innerHTML.includes("Favorit")) {
          timestamp.innerHTML += " - <em>Favorit</em>";
        }
      } else {
        favBtn.textContent = "Dodaj u favorite";
        timestamp.innerHTML = timestamp.innerHTML.replace(
          " - <em>Favorit</em>",
          ""
        );
      }
    });

    delBtn.addEventListener("click", () => {
      reviewItem.remove();
    });

    reviewsContainer.prepend(reviewItem);
    form.reset();
  });
});


