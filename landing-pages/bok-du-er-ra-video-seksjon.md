# Video-seksjonen «Se inni boken» (native Kajabi)

Siden består av tre seksjoner i Kajabi (Nova-tema), i denne rekkefølgen:

1. **Kodeblokk del 1** – alt i `bok-du-er-ra.html` før markøren `KAJABI-SPLITT` (stil, ikoner, hero → «Dette får du i boken»).
2. **Native seksjon «Se inni boken (video 9:16)»** – horisontal på desktop, stablet på mobil, hvit bakgrunn, gap 56 px.
   - Kodeblokk (tekst ved videoen):
     ```html
     <div class="dera" lang="nb" style="background:transparent">
       <p class="dera-eyebrow">Se inni boken</p>
       <h2>Bla i boken før du bestiller</h2>
       <p class="dera-lead">Få et lite innblikk i boken før du bestiller. Den er laget for å brukes, med øvelser og refleksjonsspørsmål underveis som du kan ta rett inn i hverdagen.</p>
       <p style="margin-top:24px"><a class="dera-btn" href="#bestill">Bestill signert bok – 349 kr <svg aria-hidden="true"><use href="#dera-i-arrow"/></svg></a></p>
     </div>
     ```
     `custom_classes: md:max-w-[460px]`
   - Videoblokk: mediefil «Book video» (media_id 4607592, Wistia gktyqaqlti), 9:16.
     `custom_classes: w-full max-w-[340px] mx-auto rounded-2xl overflow-hidden shadow-xl`, ingen autoplay, spilleknapp + fremdriftslinje + fullskjerm.
3. **Kodeblokk del 2** – alt i `bok-du-er-ra.html` etter markøren (Om Ine → bestilling → bunntekst).
