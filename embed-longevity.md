# Codici di embed: longevity

Ogni blocco è autonomo: incolla iframe e `<script>` insieme, nel punto dell'articolo
dove deve comparire il grafico. Se ne usi più di uno nella stessa pagina non si disturbano.

L'altezza nello `style` è quella di partenza, misurata sul telefono più stretto (320 px):
appena il grafico comunica la propria altezza reale, viene corretta (610 px su desktop).

Tutti i grafici con i codici da copiare: <https://sapomnia.github.io/longevity/>

---

## 1. I posti letto nelle RSA italiane

Indirizzo: <https://sapomnia.github.io/longevity/posti-rsa-ogni-10mila-over-65.html>

```html
<iframe id="longevity-posti-rsa-ogni-10mila-over-65" src="https://sapomnia.github.io/longevity/posti-rsa-ogni-10mila-over-65.html" title="I posti letto nelle RSA italiane" loading="lazy" scrolling="no" style="width:100%;height:700px;border:0;display:block"></iframe>
<script>
(function () {
  var iframe = document.getElementById('longevity-posti-rsa-ogni-10mila-over-65');
  window.addEventListener('message', function (evento) {
    if (evento.origin !== 'https://sapomnia.github.io' || evento.source !== iframe.contentWindow) return;
    var dati = evento.data || {};
    var altezza = parseInt(dati.altezza || dati.height, 10);
    if (altezza > 100 && altezza < 8000) iframe.style.height = altezza + 'px';
  });
})();
</script>
```

---

## 2. RSA, i posti letto e le liste d'attesa

Indirizzo: <https://sapomnia.github.io/longevity/persone-lista-attesa-per-posto-letto.html>

```html
<iframe id="longevity-persone-lista-attesa-per-posto-letto" src="https://sapomnia.github.io/longevity/persone-lista-attesa-per-posto-letto.html" title="RSA, i posti letto e le liste d'attesa" loading="lazy" scrolling="no" style="width:100%;height:800px;border:0;display:block"></iframe>
<script>
(function () {
  var iframe = document.getElementById('longevity-persone-lista-attesa-per-posto-letto');
  window.addEventListener('message', function (evento) {
    if (evento.origin !== 'https://sapomnia.github.io' || evento.source !== iframe.contentWindow) return;
    var dati = evento.data || {};
    var altezza = parseInt(dati.altezza || dati.height, 10);
    if (altezza > 100 && altezza < 8000) iframe.style.height = altezza + 'px';
  });
})();
</script>
```
