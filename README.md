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
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Teorija:

<!--
1. Potrebno je HTML dokumentu dodijeliti naslov "My Portfolio". Što je potrebno napisati unutar <head> oznake HTML dokumenta kako bi se to postiglo?
Odgovor: <title>My Portfolio</title>

2. Koji element koristimo za označavanje sadržaja koji predstavlja glavnu navigaciju?
Odgovor: <nav>

3. Koristeći HTML, označite sadržaj kao audio zapis sa kontrolama za upravljanje reprodukcijom sadržaja.
Odgovor:
<audio controls>
  <source src="audio.mp3" type="audio/mpeg">
  Vaš preglednik ne podržava audio zapis.
</audio>

4. Što je HTML?
Odgovor: Jezik za označavanje sadržaja web stranica (HyperText Markup Language).

5. Praktični zadatak HTML
Odgovor: Izrada obrasca s poljima za naziv i ocjenu te dvije pohranjene stavke.

6. Koji od navedenih elemenata je najprikladnije koristiti za označavanje sadržaja koji nije direktno povezan sa sadržajem koji ga okružuje?
Odgovor: <aside>

7. Koji od navedenih elemenata je najprikladnije koristiti za označavanje uvodnog sadržaja?
Odgovor: <header>

8. HTML dokument ne smije sadržavati više od jednog <article> elementa.
Odgovor: Netočno. Može ih biti više.

9. Kako HTML omogućuje izradu pristupačnih web stranica?
Odgovor: Korištenjem semantičkih elemenata i atributa poput aria-label, alt, itd.

10. Koji HTML atribut koristimo za primjenu linijskih stilskih pravila?
Odgovor: style

11. Koji selektor će selektirati sve <a> elemente koji se nalaze pod pokazivačem miša?
Odgovor: a:hover

12. Što je potrebno napisati da bi se iskoristila CSS3 varijabla "color-primary" kao vrijednost za promjenu boje teksta?
Odgovor: color: var(--color-primary);

13. HTML sadrži prazan <div> element. Koristeći CSS, selektirajte element i uredite ga tako da odgovara obliku na slici.
Odgovor:
div {
  background-color: rgb(40, 158, 40);
  width: 100px;
  height: 100px;
  translate: 50px 50px;
  transform: rotate(-90deg);
  border: 0px solid;
  border-radius: 75% 0% 75% 0%;
}

14. Praktični zadatak CSS
Odgovor: Oblikovanje korisničkog sučelja prema skici, s vanjskim .css dokumentom i media queryjima.

15. Potrebno je pozvati SCSS funkciju "lighten". Koja od navedenih linija koda je ispravna?
Odgovor: lighten($color, 20%)

16. Potrebno je iskoristiti SCSS mixin "square". Koja od navedenih linija koda je ispravna?
Odgovor: @include square;

17. Što je to minifikacija (minimizacija)? Zašto koristiti minifikaciju?
Odgovor: Uklanjanje nepotrebnih znakova iz koda radi bolje optimizacije i bržeg učitavanja.

18. Što se od navedenog ne koristi za petlju?
Odgovor: switch

19. Što od navedenog nije ispravan identifikator varijable?
Odgovor: 1broj (ne smije započeti brojkom)

20. Potrebno je definirati funkciju "max" koja će vratiti veći od dva broja.
Odgovor:
function max(a, b) {
  return a >= b ? a : b;
}

21. Koja je razlika između deklariranja varijable pomoću ključne riječi "let" i "const"?
Odgovor: let dopušta promjenu vrijednosti; const ne dopušta ponovno dodjeljivanje.

22. Praktični zadatak JS
Odgovor: Validacija obrasca, dodavanje stavke, brisanje, označavanje favorita (JS funkcionalnosti).

23. JavaScript je objektno-orijentirani programski jezik. Y/N
Odgovor: Da

24. JavaScript je funkcijski programski jezik. Y/N
Odgovor: Da

25. Što je ECMAScript?
Odgovor: Standard koji definira JavaScript jezik.

26. Što HTML DOM ne definira?
Odgovor: Ne definira izgled/stil (to radi CSS).

27. Koja od navedenih metoda koje postoje nad "document" objektom nije ispravna?
Odgovor: getElementsTagName() – ispravno je getElementsByTagName()

28. Napiši kod koji unutar elementa s ID-jem "copyright-year" ispisuje trenutnu godinu.
Odgovor:
document.getElementById("copyright-year").textContent = new Date().getFullYear();

29. Što je GIT?
Odgovor: Sustav za verzioniranje koda.

30. Kako se inicijalizira Git repozitorij?
Odgovor: git init

31. Što je to repozitorij?
Odgovor: Mjesto gdje se pohranjuje kod i prati njegova povijest.

32. Kako se instalira paket s nazivom algebra-library tako da se zapiše u package.json datoteku?
Odgovor: npm install algebra-library --save

34. Child komponenta može i smije mijenjati props objekt koji je primila od parent komponente. Y/N
Odgovor: Ne

35. Što od navedenog nije jedna od faza životnog ciklusa React komponente?
Odgovor: (npr. initRender – ne postoji kao službena faza)

36. Potrebno je u komponentu <User> postaviti prop "firstName". Odaberite ispravnu liniju koda.
Odgovor: <User firstName="Ivana" />
-->


