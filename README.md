# Todo-sovellus

Full-stack todo-sovellus, jossa käyttäjä voi luoda tunnuksen, kirjautua sisään ja hallita omia tehtäviään.

## Teknologiat
**Frontend:** React, Vite, Axios, React Router  
**Backend:** Node.js, Express, PostgreSQL
**Autentikointi:** JWT (JSON Web Token), bcrypt
**Testaus:** Mocha, Chai

## Ominaisuudet

- Käyttäjän rekisteröinti ja kirjautuminen
- Tehtävien listaus, lisäys ja poisto
- Suojatut reitit token-pohjaisella autentikoinnilla
- MVC-arkkitehtuuri backendissä (model / controller / router)

## Rakenne

    todo/
    ├── src/              Frontend (React)
    ├── public/           Staattiset tiedostot
    └── server/           Backend (Express)
        ├── models/       Tietokantakyselyt
        ├── controllers/  Sovelluslogiikka
        ├── routes/       Reitit
        └── helper/       Apurit (tietokantayhteys, auth, virheluokka)

## Käyttöönotto

Asenna riippuvuudet sekä juuressa (frontend) että server-kansiossa (backend):

    npm install
    cd server
    npm install

Luo `server`-kansioon `.env`-tiedosto tietokanta- ja JWT-asetuksille.

Käynnistä backend (server-kansiossa):

    npm run dev

Käynnistä frontend (juuressa):

    npm run dev

## Testaus

Käynnistä palvelin test-tilassa (server-kansiossa):

    npm run start:test

Aja testit toisessa terminaalissa (server-kansiossa):

    npm test
