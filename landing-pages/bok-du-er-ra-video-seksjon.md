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
   - Video: «video_embed»-blokk med Wistia-iframe for mediefilen «Book video» (media_id 4607592, Wistia gktyqaqlti),
     i en egen 9:16-boks. Kajabis vanlige videoblokk tvinger 16:9 og ga svarte felt rundt den stående videoen.
     ```html
     <div style="position:relative;width:100%;max-width:340px;aspect-ratio:9/16;margin:0 auto;border-radius:16px;overflow:hidden;background:#f6d6dc;box-shadow:0 20px 50px rgba(58,42,48,0.22);">
       <iframe src="https://fast.wistia.net/embed/iframe/gktyqaqlti?videoFoam=false&fitStrategy=contain&playerColor=9b2c64&playButton=true&controlsVisibleOnLoad=false" title="Bla i boken Du er rå!" allow="autoplay; fullscreen" allowfullscreen frameborder="0" scrolling="no" loading="lazy" style="position:absolute;top:0;left:0;width:100%;height:100%;border:0;"></iframe>
     </div>
     ```
     `custom_classes: w-full max-w-[340px] mx-auto`. Den gamle videoblokken (…_1) ligger igjen i temaet, men er tatt ut av block_order.
3. **Kodeblokk del 2** – alt i `bok-du-er-ra.html` etter markøren (Om Ine → bestilling → bunntekst).
