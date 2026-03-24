Egy **komplex, de még 16 éveseknek is élvezetes projektfeladat** működik a legjobban, ha egyetlen témán belül sok CSS-tulajdonságot lehet kipróbálni. Jó tapasztalat, ha **egy mini weboldalt készítenek**, amelyben több aloldal vagy szekció van.

Az alábbi feladat **szinte az összes felsorolt CSS/HTML elemet természetesen használja**.

---

# Projektfeladat: „Álom utazási iroda” weboldal

A diákok készítsenek egy **egylapos (single page) utazási iroda weboldalt**, amely bemutat 3–4 úti célt.

Az oldal részei:

1. fejléc navigációval

2. bemutatkozó rész (hero)

3. úti célok kártyákban

4. galéria

5. jelentkezési űrlap

6. lábléc

---

# 1. Navigáció és belső linkek

Feladat:

- legyen navigáció a tetején

- linkeljen az oldal különböző részeire

HTML elemek:

```
<header>
<nav>
<a href="#home">Főoldal</a>
<a href="#destinations">Úti célok</a>
<a href="#gallery">Galéria</a>
<a href="#contact">Kapcsolat</a>
<a href="https://hu.wikipedia.org" target="_blank">Külső link</a>
</nav>
</header>
```

Tanulható:

- belső link (`#id`)

- külső link

- `target="_blank"`

CSS:

```
nav a:hover
nav a:visited
```

---

# 2. Úti cél kártyák (CSS Grid)

A diákok készítsenek **kártyás elrendezést**.

```
<section id="destinations">
<div class="grid">

<div class="card">
<img src="paris.jpg">
<h3>Párizs</h3>
<p>Romantikus város.</p>
</div>

</div>
</section>
```

CSS:

```
.grid{
display:grid;
grid-template-columns: repeat(3,1fr);
gap:20px;
}
```

Tanulható:

- `css-grid`

- `object-fit`

```
.card img{
width:100%;
height:200px;
object-fit:cover;
}
```

---

# 3. Képek effektekkel (filter)

```
.card img{
filter: grayscale(100%);
transition:0.4s;
}

.card img:hover{
filter:grayscale(0%);
}
```

Tanulható:

- `filter`

- `transition`

---

# 4. Hover animáció a kártyán

```
.card:hover{
transform:scale(1.05);
}
```

vagy

```
.card:hover{
transform:rotate(2deg);
}
```

Tanulható:

- `transform`

- `transition`

---

# 5. Galéria (aspect-ratio)

```
.gallery img{
width:100%;
aspect-ratio:1/1;
object-fit:cover;
}
```

Tanulható:

- `aspect-ratio`

- `object-fit`

---

# 6. Jelentkezési űrlap

```
<form>

<label>Név</label>
<input type="text" required>

<label>Email</label>
<input type="email">

<label>Úti cél</label>
<select>
<option>Párizs</option>
<option>Róma</option>
</select>

<textarea placeholder="Üzenet"></textarea>

<button>Küldés</button>

</form>
```

Tanulható:

- `input`

- `select`

- `textarea`

- `button`

---

# 7. Attribútum szelektor

```
input[type="text"]{
border:2px solid blue;
}

input[required]{
background:#fff7cc;
}
```

---

# 8. CSS kombinátorok

```
.card > h3{
color:darkblue;
}

.card + .card{
margin-top:20px;
}

.card ~ p{
font-style:italic;
}
```

Tanulható:

- `>`

- `+`

- `~`

---

# 9. Position

Pl. egy badge:

```
.card{
position:relative;
}

.badge{
position:absolute;
top:10px;
right:10px;
background:red;
color:white;
}
```

---

# 10. Overflow

```
.description{
height:80px;
overflow:auto;
}
```

---

# 11. Outline

```
input:focus{
outline:3px solid orange;
}
```

---

# 12. Media query (reszponzív)

```
@media (max-width:800px){

.grid{
grid-template-columns:1fr 1fr;
}

body{
background:#eef;
}

}

@media (max-width:500px){

.grid{
grid-template-columns:1fr;
}

}
```

---

# 13. max-width / min-width

```
.container{
max-width:1000px;
min-width:300px;
margin:auto;
}
```

---

# 14. Egyszerű animáció

```
@keyframes float{

0%{transform:translateY(0);}
50%{transform:translateY(-10px);}
100%{transform:translateY(0);}

}

.logo{
animation:float 3s infinite;
}
```

---

# Kész projektben ezek mind megjelennek

| Téma                 | Hol használjuk |
| -------------------- | -------------- |
| linkek               | navigáció      |
| css-grid             | kártyák        |
| filter               | képek          |
| transition           | hover          |
| transform            | kártyák        |
| animation            | logo           |
| overflow             | leírás         |
| object-fit           | képek          |
| aspect-ratio         | galéria        |
| position             | badge          |
| form                 | jelentkezés    |
| outline              | input focus    |
| attribútum szelektor | input[type]    |
| kombinátorok         | card példák    |
| media-query          | reszponzív     |

---

# Tanári extra ötlet (nagyon működik)

Add ki **szinteket**, mint egy játék:

### Level 1

oldal szerkezet

### Level 2

grid + képek

### Level 3

hover effektek

### Level 4

form

### Level 5

responsive

Így a diákok **sikerélményt kapnak**.

---

✅ Ha szeretnéd, készítek egy **nagyon jól működő teljes mintafeladatot diákoknak (feladatlap + pontozás + minta layout)**, amit sok webfejlesztő tanár használ.Készítettem egy **teljes mintafeladatot diákoknak**, amely

- tanulási segédanyagként is működik

- sok **magyarázó megjegyzést** tartalmaz

- lefedi az általad felsorolt **HTML és CSS tulajdonságokat**.

A diákok ezt **alapként megkaphatják**, majd bizonyos részeket ki lehet törölni vagy nekik kell elkészíteni.

---

# Projektfeladat – Utazási iroda weboldal

Készíts egy egyszerű bemutatkozó weboldalt egy képzeletbeli utazási iroda számára!

A weboldal tartalmazzon:

- navigációt

- úti célokat bemutató kártyákat

- galériát

- jelentkezési űrlapot

- reszponzív megjelenést

---

# 1. HTML szerkezet (index.html)

```html
<!DOCTYPE html>
<html lang="hu">
<head>
<meta charset="UTF-8">
<title>Dream Travel</title>

<link rel="stylesheet" href="style.css">
</head>

<body>

<!-- Navigáció belső linkekkel -->
<header id="home">

<h1 class="logo">Dream Travel</h1>

<nav>
<a href="#destinations">Úti célok</a>
<a href="#gallery">Galéria</a>
<a href="#contact">Kapcsolat</a>

<!-- külső link -->
<a href="https://hu.wikipedia.org/wiki/Turizmus" target="_blank">
Turizmus (külső link)
</a>

</nav>

</header>


<!-- Úti célok -->
<section id="destinations">

<h2>Népszerű úti célok</h2>

<div class="grid">

<div class="card">

<div class="badge">Akció</div>

<img src="paris.jpg" alt="Paris">

<h3>Párizs</h3>

<p class="description">
Párizs a romantika fővárosa.
A város híres az Eiffel toronyról,
múzeumairól és kávézóiról.
</p>

</div>


<div class="card">

<img src="rome.jpg" alt="Rome">

<h3>Róma</h3>

<p class="description">
Róma az örök város, ahol
történelem és kultúra
minden utcában megtalálható.
</p>

</div>


<div class="card">

<img src="tokyo.jpg" alt="Tokyo">

<h3>Tokió</h3>

<p class="description">
Tokió modern és hagyományos
kultúra különleges keveréke.
</p>

</div>

</div>

</section>


<!-- Galéria -->
<section id="gallery">

<h2>Galéria</h2>

<div class="gallery">

<img src="city1.jpg">
<img src="city2.jpg">
<img src="city3.jpg">
<img src="city4.jpg">

</div>

</section>


<!-- Kapcsolat -->
<section id="contact">

<h2>Jelentkezés utazásra</h2>

<form>

<label>Név</label>
<input type="text" required>


<label>Email</label>
<input type="email">


<label>Úti cél</label>
<select>

<option>Párizs</option>
<option>Róma</option>
<option>Tokió</option>

</select>


<label>Üzenet</label>
<textarea></textarea>

<button>Küldés</button>

</form>

</section>


<footer>
<p>Dream Travel 2026</p>
</footer>


</body>
</html>
```

---

# 2. CSS (style.css)

```css
/* oldal alap stílus */

body{
font-family:Arial;
margin:0;
}


/* max-width használata */

header,section,footer{

max-width:1000px;
min-width:300px;

margin:auto;
padding:20px;

}


/* navigáció */

nav a{

margin-right:15px;
text-decoration:none;
color:darkblue;

}

/* hover effekt */

nav a:hover{
color:red;
}


/* outline amikor input fókuszba kerül */

input:focus{
outline:3px solid orange;
}



/* GRID layout */

.grid{

display:grid;
grid-template-columns:repeat(3,1fr);
gap:20px;

}


/* kártya */

.card{

border:1px solid #ccc;
padding:10px;

position:relative;

transition:0.3s;

}


/* transform hover */

.card:hover{

transform:scale(1.05);

}


/* badge absolute position */

.badge{

position:absolute;
top:10px;
right:10px;

background:red;
color:white;
padding:5px;

}



/* kép stílus */

.card img{

width:100%;
height:200px;

object-fit:cover;


/* filter effekt */

filter:grayscale(100%);

transition:0.5s;

}


/* filter hover */

.card img:hover{
filter:grayscale(0%);
}



/* overflow példa */

.description{

height:60px;

overflow:auto;

}



/* galéria */

.gallery{

display:grid;
grid-template-columns:repeat(4,1fr);
gap:10px;

}


.gallery img{

width:100%;

/* aspect ratio */

aspect-ratio:1/1;

object-fit:cover;

}



/* attribútum szelektor */

input[type="text"]{

border:2px solid blue;

}



/* animáció */

@keyframes float{

0%{transform:translateY(0);}

50%{transform:translateY(-10px);}

100%{transform:translateY(0);}

}


.logo{

animation:float 3s infinite;

}



/* CSS kombinátor példák */

/* csak közvetlen gyermek */

.card > h3{
color:darkgreen;
}


/* következő elem */

.card + .card{
border-color:blue;
}



/* MEDIA QUERY */

@media (max-width:800px){

.grid{
grid-template-columns:1fr 1fr;
}

.gallery{
grid-template-columns:1fr 1fr;
}

}


@media (max-width:500px){

.grid{
grid-template-columns:1fr;
}

}
```

---

# 3. A feladatban szereplő technológiák

A projekt tartalmazza:

HTML:

- nav

- section

- header

- footer

- form

- input

- select

- textarea

- button

- belső és külső link

CSS:

- combinator selectors (`>`, `+`)

- attribute selector

- outline

- max-width / min-width

- filter

- transform

- animation

- overflow

- transition

- object-fit

- position

- css-grid

- media-query

- aspect-ratio

---

# 4. Diákoknak adható plusz feladatok

1️⃣ Készíts még **két új úti cél kártyát**.

2️⃣ Adj hozzá **új form mezőt** (pl. dátum).

3️⃣ Készíts **hover animációt a galéria képein**.

4️⃣ Mobile nézetben változtasd meg a **háttér színt**.

5️⃣ Adj hozzá **új filter effektet**.

---

# 5. Tanári javaslat

Nagyon jól működő tanítási sorrend:

1. HTML struktúra

2. Grid layout

3. Képek és object-fit

4. Hover effektek

5. Form

6. Position

7. Animation

8. Responsive design

Így minden órán **látható fejlődés** lesz.

---

Ha szeretnéd, készítek még egy **még jobb verziót tanároknak**, amelyben:

- vannak **hibás kódrészletek (debug feladat)**

- vannak **hiányos részek (kitöltendő feladat)**

- és egy **pontozási rubrika dolgozathoz / beadandóhoz**.
