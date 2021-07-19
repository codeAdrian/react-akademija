Instalirati NodeJS i NPM
https://nodejs.org/en/

Provjeriti radi li NPM u terminalu

```
npm -v
```

Mora vratiti neku verziju, npr "7.18.1".

Ako ne radi, onda si instalirajte
Bash terminal za Windows sustav i ponovo instalirajte NodeJS
https://gitforwindows.org/

Ukoliko ni tada ne radi, morate dodati NPM u Windows PATH. Pratite upute iz jedne od ova
https://stackoverflow.com/a/27864253
https://stackoverflow.com/a/27344046

## 1. Instalacija projekta (samo jednom)

U terminalu otvoriti (navigirati) do datoteke `cd naziv-datoteke` i pokrenuti

```
npm install
```

## 2. Pokretanje projekta

U terminalu otvoriti (navigirati) do datoteke `cd naziv-datoteke` i pokrenuti

```
npm run start
```

# Zadatak

## 1. dan

1. Preuzeti datoteku sa repozitorija (download zip), instalirati i pokrenuti projekt

2. Napraviti sljedeće komponente u `src/components` folderu:

   SearchForm - za formu (input i button)
   CollectionTable - za tablicu sa podacima
   TableItem - jedan podatkovni redak tablice (tr u tbody elementu)
   Pagination - paginacija (previous i next button i trenutni page)

3. Dodati HTML markup za komponente

4. Pozvati komponente u src/App.js

5. U `src/App.jsx` je importan `data` iz `src/data.json` kojeg danas koristite kao placeholder podatke. Sutra radimo API integraciju.

6. Prosljediti placeholder podatke komponentama putem props-a.

SearchForm - prima standardni React "children" prop koji će sadržavati rezultat pretraživanja. U suprotnom će ispisati "No results".

CollectionTable - prima standardni React "children" prop koji će sadržavati podatkovne retke koji se iterativno pozivaju ovisno o `releases` array-u podataka iz `data.json` datoteke.

TableItem - prima propove za prikaz podataka iz `releases` array-a `data.json` datoteke.

Pagination - prima propove za prikaz podataka iz `pagination` objekta `data.json` datoteke. Potrebni su `pages` koji sadrži ukupan broj pageva i `page` koji sadrži podatak koji je trenutni page.

7. Dodati stilove po želji (`src/index.css`) ili da izgleda slično sljedećem dizajnu.

### Korisne informacije

Prijedlog strukture App.json-a

```jsx

```

## 2. dan

export const Pagination = ({ page, pages }) => {
return (

      export const Search = ({ children }) => {

          export const Table = ({ children }) => {

              export const TableItem = ({ id, title, year, artists, genres, styles }) => {
