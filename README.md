# web-scrapping
Proves de web scrapping amb node.js

https://www.donnywals.com/build-a-simple-web-scraper-with-node-js/

https://www.freecodecamp.org/news/the-ultimate-guide-to-web-scraping-with-node-js-daa2027dcd3/

    npm install --save request request-promise cheerio puppeteer promise


Per descarregar imatges, https://stackoverflow.com/questions/12740659/downloading-images-with-node-js

- [x] Bug: linia 77, no agafa els elements img
- [ ] Separar la funcio download en fitxer apart (funcions de fitxers   )
- [ ] Pendent depurar error en promeses (surt en vermell)
- [ ] Funcio que esborri el directori /teams i tot el seu contingut si ja existeix
- [x] Afegida self-invoking function per evitar variables globals en el Global object i que puguin interferir amb les variables locals
- [ ] When creating .json and image directories --> clean the directory and remove it before executing 
- [ ] incloure excepcions en el codi en el tractament amb fitxers
- [ ] emprar modul 'path' per crear els paths als fitxers