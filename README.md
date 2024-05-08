# goit-markup-hw-06

This is my first project

<!--

================= БЛОКОВА МОДЕЛЬ =============

box-sizing: content-box | border-box | inherit

================ ГЕОМЕТРІЯ ЕЛЕМЕНТА ====================

               СКИДАННЯ

h1,
h2,
h3,
h4,
h5,
h6,
p {
	margin-top: 0;
	margin-bottom: 0;
}

ul, ol {
	margin-top: 0;
	margin-bottom: 0;
	padding-left: 0;
}

====================== Властивість border ============================

border: ширина стиль колір;

Ширина рамки визначається в пікселях.
Стиль — одне значення з набору можливих значень, найпоширенішими значеннями є
solid, dashed і dotted.
Колір задається в будь-якому форматі, зазвичай HEX

border-width: значення;
border-style: значення;
border-color: значення;

border-top: ширина стиль колір;
border-right: ширина стиль колір;
border-bottom: ширина стиль колір;
border-left: ширина стиль колір;

border-radius: %; чи px;

border-top-left-radius: значення;
border-top-right-radius: значення;
border-bottom-right-radius: значення;
border-bottom-left-radius: значення;

================== приховати зайвий контент =================

overflow: hidden;
overflow: visible | hidden | scroll | auto




flex-wrap: wrap;
gap
row-gap
column-gap
margin-left: auto
margin-right: auto;
align-items: center;
justify-content: center;
background-image: url(шлях до зображення 1), url(шлях до зображення 2);
background-size: 100px, cover;
background-position: top right, center;+
background-repeat: repeat-x, no-repeat;

background-image: linear-gradient(
to bottom,
rgba(25, 25, 25, 0.3),
rgba(255, 0, 0, 0.3)
),
url(шлях до зображення);

background: background-color: background-image: background-repeat: background-position: background-attachment: background-size:

box-shadow: <x-offset> <y-offset> <blur> <spread> <color>

На один елемент можна додати кілька тіней,
вказавши їх значення через кому.

box-shadow: <x-offset> <y-offset> <blur> <spread> <color>,
<x-offset> <y-offset> <blur> <spread> <color>,
<x-offset> <y-offset> <blur> <spread> <color>,

       Внутрішня тінь

box-shadow: inset <x-offset> <y-offset> <blur> <spread> <color>
Встановлюємо колір заливки у спокійному стані.
.icon {
fill: #2a2a2a;
}
Змінюємо колір заливки при ховері.
.icon:hover {
fill: #03a9f4;
}
<svg>
<use href="./шлях-до-svg-спрайту/имʼя-спрайта.svg#ідентифікатор-символа"></use>
</svg>

.box:hover::before {
background-color: green;
}
.box:hover::after {
background-color: tomato;
}

position: static | relative | absolute | fixed | sticky

transition-property: background-color, color, ...;
transition-duration: <час>
transition-timing-function: ease; linear; ease-in; ease-out; ease-in-out;
transition-delay: <затримка>

transform: none | scale (масштаб 1.25 | 0.75) | opacity (прозорість) | transform (трансформація)
transform: rotate(45deg); rotate(0.5turn);

transform: translateX(tx), translateY(ty) і translate(tx, ty)

z-index: 2; z-index: 1; z-index: -1;

========================= FORM ===========================

<form name="feedback_form" autocomplete="off" novalidate>
	-- Елементи форми --
</form>

<form class="form" name="issue_report_form" autocomplete="off"></form>

================= BUTTON ===================

<form>
	-- Елементи форми --

  <button type="submit">Submit feedback</button>
  <button type="submit">Submit feedback</button>
</form>

button {
	font-family: inherit;
	color: currentColor;
}

================ INPUT ================

<form>
  <input class="form-input" type="text" name="username"/>
  <input class="form-input" type="text" name="topic"/>

  <button type="submit">Submit feedback</button>
</form>

<form>
  <label>
    Username
    <input type="text" name="username" />
  </label>
  <button type="submit">Submit feedback</button>
</form>

Якщо елемент форми не вкладено в label,
необхідно явно зв'язати їх через:
атрибут id елемента та
атрибут for мітки

<form>
  <label for="username">Username</label>
  <input type="text" name="username" id="username" />
  <button type="submit">Submit feedback</button>
</form>

input {
	font-family: inherit;
}

================== placeholder ======================

Атрибут placeholder дозволяє відображати текст-підказку

<form>
  <label>
    Username
    <input type="text" name="username" placeholder="Jacob Mercer" />
  </label>
  <button type="submit">Submit feedback</button>
</form>

Для оформлення тексту підказки використовується псевдоелемент ::placeholder.

input::placeholder {
	color: teal;
  font-weight: 700;
}

input:hover::placeholder,
input:focus::placeholder {
  color:orange;
}

            :placeholder-shown
дозволяє налаштовувати властивості поля вводу під час відображення тексту-підказки

input {
  border: 1px solid orange;
}

input:placeholder-shown {
  border-color: blue;
}

=============== autofocus ====================

<form>
  <label>
    First name
    <input type="text" name="firstName" autofocus />
  </label>
  <label>
    Last name
    <input type="text" name="lastName" />
  </label>
  <button type="submit">Submit</button>
</form>

================ :focus-within ==================

Застосовується до елемента, щойно він сам або елементи всередині нього отримують фокус.
Це дозволяє застосувати стилі на:
мітку
форму
окреме поле форми
при взаємодії користувача з полями форми.

.form:focus-within {
  border-color: #2196f3;
}

.form-label:focus-within {
  color: #2196f3;
}

================= textarea =================

<textarea class="bbb" name="vvv" rows="5" ~cols="2"~ placeholder="kkk"></textarea>

За замовчуванням елемент textarea можна розтягувати по горизонталі і вертикалі.
Для того щоб контролювати можливість зміни розміру користувачем, CSS має властивість resize.

.bbb {
resize: both | horizontal | vertical | none
}

============== select =================

<label class="class">
 <select class="class" name="size">
  <option value="xs">Extra Small</option>
  <option value="s">Small</option>
  <option value="m" selected>Medium</option>
  <option value="l">Large</option>
 </select>
</label>

=============== optgroup =============

<label class="class">
 <select name="month">
  <optgroup label="Summer">
    <option value="s6">June</option>
    <option value="s7">July</option>
    <option value="s8">August</option>
  </optgroup>

  <optgroup label="Autumn">
    <option value="s9">September</option>
    <option value="s10">October</option>
    <option value="s11">November</option>
  </optgroup>
 </select>
</label>

============= email & password & phone ===============

<label>
  Email
  <input type="email" name="email" />
</label>
<label>
  Password
  <input type="password" name="pwd" minlength="5" maxlength="12" />
</label>
<>
  Phone number
  <input type="tel" name="phone" />

  ============ number ================

  <input type="number" name="age" value="0" step="0.5" min="18" max="120" />

  ============ date == time == datetime-local ==================

               Для вибору лише дати
  <input type="date" />

               Для вибору лише часу
  <input type="time" />

               Для вибору дати і часу
  <input type="datetime-local" />

====================== type radio ======================

 <form>
  <p>Choose a color:</p>
  <label>
    <input type="radio" name="color" value="red" checked />
    Red
  </label>
  <label>
    <input type="radio" name="color" value="white" />
    White
  </label>
  <label>
    <input type="radio" name="color" value="green" />
    Green
  </label>
</form>

===================== type checkbox ====================

<form>
  <p>What are your hobbies?</p>
  <label>
    <input type="checkbox" name="hobby" value="music" checked />
    Music
  </label>
  <label>
    <input type="checkbox" name="hobby" value="sports" checked />
    Sports
  </label>
  <label>
    <input type="checkbox" name="hobby" value="reading" />
    Reading
  </label>
</form>

.form-input:checked {
outline: 2px solid #2196f3;
outline-offset: 2px;
box-shadow: 0 0 0 2px orangered;
}

input[type="checkbox"]:checked {
box-shadow: 0 0 0 2px orangered;
}
input[type="checkbox"]:checked + label {
color: blue;
}

<input type="checkbox" name="hobby" value="music" id="music" />
<label for="music">Music</label>

================= ОБОВ'ЯЗКОВИЙ required ========================

<input type="email" name="email" required />

================ DISABLED ===================

<button type="button">Active button</button>
<button type="button" disabled>Disabled button</button>

button:disabled {
background-color: lightgray;
cursor: not-allowed;
}

===================== Групування полів ===================

<form class="form">
  <fieldset class="form-group">
    <legend class="group-title">Enter your contact details</legend>
    <label class="form-label">
      Name
      <input type="text" name="username" />
    </label>
    <label class="form-label">
      Email
      <input type="email" name="email" />
    </label>
  </fieldset>

  <fieldset class="form-group">
    <legend class="group-title">Your favourite programming language</legend>
    <div class="form-field">
      <input type="checkbox" name="language" value="python" id="python">
      <label class="form-label" for="python">Python</label>
    </div>
    <div class="form-field">
      <input type="checkbox" name="language" value="js" id="js">
      <label class="form-label" for="js">JavaScript</label>
    </div>
    <div class="form-field">
      <input type="checkbox" name="language" value="ruby" id="ruby">
      <label class="form-label" for="ruby">Python</label>
    </div>
  </fieldset>

  <fieldset class="form-group">
    <legend class="group-title">I want to receive</legend>
    <div class="form-field">
      <input type="checkbox" name="newsletter" value="weekly" id="weekly">
      <label class="form-label" for="weekly">The weekly newsletter</label>
    </div>
    <div class="form-field">
      <input type="checkbox" name="newsletter" value="offers" id="offers">
      <label class="form-label" for="offers">Offers from the company</label>
    </div>
    <div class="form-field">
      <input type="checkbox" name="newsletter" value="associated_offers" id="associated_offers">
      <label class="form-label" for="associated_offers">Offers from associated companies</label>
    </div>
  </fieldset>

<button type="submit">Subscribe</button>

</form>

fieldset {
padding: 0;
margin: 0;
border: none;
}

================ Створення модального вікна ===================

<div class="modal-overlay">
      <div class="modal">
        <p>
          Lorem ipsum dolor
        </p>
      </div>
    </div>

.modal-overlay {
background-color: rgba(0, 0, 0, 0.5);

position: fixed;
top: 0;
left: 0;
width: 100%;
height: 100%;
z-index: 999;
display: flex;
justify-content: center;
align-items: center;

opacity: 0;
pointer-events: none;
transition: opacity 250ms ease-in-out;
}

.modal-overlay.is-open {
opacity: 1;
pointer-events: auto;
}

.modal {
background-color: #fff;
border-radius: 4px;
padding: 16px;
box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
max-width: 480px;
max-height: 80%;
overflow-y: auto;
}

================ MEDIA ===================

body {
  background-color: white;
}

/* Застосовується коли ширина в'юпорта менше або дорівнює 600px */

@media (max-width: 600px) {
  body {
    background-color: green;
  }
}

/* Застосовується коли ширина в'юпорта більше або дорівнює 800px */

@media (min-width: 800px) {
  body {
    background-color: orange;
  }
}

@media print {
  body {
    color: green;
  }
}

@media screen and (min-width: 400px) {
  /* ... */
}

@media only|not media-type ****only|and|not ****(media-feature) {
  /*
    Набір CSS-правил, які потрібно застосувати до документа,
    якщо умова перевірки медіатипу та виразу істинна
  */
}

@media screen and (min-width: 400px) and (max-width: 800px) {
  body {
    background-color: red;
  }
}

@media (max-width: 600px) (or)|(,)(min-width: 960px){
  body {
    background-color: gray;
  }
}

-->
