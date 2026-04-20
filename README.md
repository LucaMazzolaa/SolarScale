SUPSI 2026  
Corso d’interaction design, CV429.01  
Docenti: A. Gysin, G. Profeta  

Progetto 1: La conquista dello spazio

# SISTEMA SOLARE IN SCALA
Autore: Luca Mazzola \
[SISTEMA SOLARE IN SCALA](https://lucamazzolaa.github.io/NASA70/)
<br><br>


## Introduzione e tema
Questo progetto esplora il Sistema solare a partire da una criticità evidente: molte delle rappresentazioni diffuse risultano poco accurate nel restituire le reali proporzioni tra dimensioni dei pianeti e distanze li separano nello spazio. La scala del Sistema è infatti così vasta da rendere impossibile una visualizzazione fedele all’interno di un’unica immagine, portando spesso a semplificazioni e alterazioni che ne compromettono la comprensione.<br>

Per affrontare questo limite, il progetto scompone il Sistema solare in tre elementi principali: dimensioni dei pianeti, posizioni e movimenti nel tempo, e distanze dal Sole. Questa scelta permette di costruire visualizzazioni più chiare, leggibili e coerenti.<br>

Ne deriva una visualizzazione interattiva capace di tradurre dati scientifici in un’esperienza visiva immediata, rendendo percepibili proporzioni normalmente astratte e restituendo in modo efficace la reale struttura e scala del Sistema solare.
<br><br>


## Riferimenti progettuali
A livello di funzione e di visualizzazione, il progetto si è basato su tre riferimenti principali, scelti in relazione ai tre temi in cui il Sistema solare è stato scomposto, con l’obiettivo di avvicinarsi il più possibile a una rappresentazione chiara e fedele delle proporzioni.<br>

Per il tema delle dimensioni, il riferimento principale è il [video](https://www.youtube.com/watch?v=i93Z7zljQ7I&t=29s) che mette in evidenza in modo immediato e comparativo le reali scale tra i pianeti.
<img width="1512" height="848" alt="Screenshot 2026-04-10 alle 09 20 55" src="https://github.com/user-attachments/assets/06a67fb2-d185-4371-92ba-9acb89c81ba1" />
<br>

Per posizioni e rotazioni, è stato utilizzato come base lo [strumento interattivo](https://ssd.jpl.nasa.gov/tools/orbit_viewer.html) che permette di osservare in modo semplificato i movimenti orbitali in tempo reale e comprendere le relazioni dinamiche tra i corpi celesti.
<img width="1512" height="720" alt="Screenshot 2026-04-10 alle 09 22 02" src="https://github.com/user-attachments/assets/7aafc356-7595-477e-832f-e0f72e2dbade" />
<br>

Per le distanze dal Sole, il riferimento chiave è la [pagina web](https://joshworth.com/dev/pixelspace/pixelspace_solarsystem.html) che rappresenta in modo  efficace la reale vastità degli spazi tra i pianeti, rendendo percepibile ciò che normalmente risulta astratto.
<img width="1512" height="734" alt="Screenshot 2026-04-10 alle 09 22 52" src="https://github.com/user-attachments/assets/cde59bcd-cf58-4614-9bd0-9613b45e7c19" />
<br><br>


## Design dell’interfaccia e modalità di interazione
Il design è concepito per offrire un'esperienza immersiva, minimale e "data-driven". Richiama l'estetica dei terminali scientifici e dei database aerospaziali, utilizzando uno sfondo nero profondo (spazio), testo bianco in font rigorosi (Neue Montreal) e un cursore personalizzato che si adatta agli elementi interattivi.<br>

L'interfaccia è strutturata secondo il principio della rivelazione progressiva: l'utente entra in una pagina con un'interfaccia minimale e, man mano che dimostra l'intento di esplorare, il sistema sblocca le visioni e i controlli avanzati.

### Mappa del sito (Pagine)
* **`index.html`** – Home / Intro
* **`dimensioni.html`** – Confronto scala
* **`posizioni.html`** – Mappa orbitale
* **`distanze.html`** – Viaggio lineare
* **`misurazioni.html`** – Sezione informativa
* **`crediti.html`** – Colophon


### Livello 1: menu globale fisso
Presente costantemente in tutte le pagine per garantire orientamento e coerenza visiva.
* **Alto-sinistra:** logo, dimensioni, posizioni, distanze.
* **Alto-destra:** metodi di misurazione, crediti.


### Livello 2: trigger di esplorazione
La soglia d'ingresso per le simulazioni (esclusi `index.html` e `crediti.html`).
* **Gesto core:** "Scorri per esplorare / leggere".
* **Meccanica:** l'azione di scroll (rotellina/trackpad) dissolve l'header introduttivo testuale e sblocca fisicamente la visione e la navigazione del motore visivo sottostante, immergendo l'utente nei dati.


### Livello 3: interazioni secondarie
Strumenti di controllo specifici che compaiono solo dopo aver superato il trigger di esplorazione iniziale (esclusi `index.html` e `crediti.html`).

**`dimensioni.html`**
* **Centro-basso:** sidebar con icone dei pianeti per il salto rapido.
* **Lati (centro):** frecce a comparsa con anteprima dati (Nome, Diametro).

**`posizioni.html`**
* **Centro-basso:** plancia del tempo spaziale (slider velocità, play/pausa/skip, data attuale).
* **Basso-destra:** controlli fisici di zoom (+ / -).

**`distanze.html`**
* **Centro-basso:** sidebar con icone dei pianeti per il salto rapido.
* **Lati (centro):** frecce a comparsa con anteprima dati (distanza da un pianeta all'altro).

**`misurazioni.html`**
* **Interazione:** layout di pura lettura. Lo scroll guida la navigazione verticale nativa tra i blocchi di testo e i player video, senza la comparsa di ulteriori pannelli di controllo.

### Dimostrazione
<video src="https://github.com/user-attachments/assets/bcbb3ed4-d773-4657-a18b-299ced5210eb" loop autoplay muted controls style="max-width: 100%;"></video>
<br>


## Tecnologia usata

Il progetto poggia su una solida architettura front-end nativa, sviluppata in **HTML5, CSS3 e JavaScript (ES6)**. HTML definisce la struttura semantica dell'interfaccia, mentre CSS ne gestisce l'estetica attraverso un design system responsivo basato su variabili, calcoli fluidi e tipografia personalizzata. JavaScript funge da motore logico dell'applicazione: orchestra il DOM, gestisce gli eventi dell'utente e sincronizza l'interfaccia con i dati e le librerie esterne.<br>

Di seguito vengono presentati tre estratti di codice chiave che sono stati fondamentali nello sviluppo del progetto, in quanto determinanti per la costruzione della logica interattiva:<br>

### 1. Motore grafico 3D (Three.js e Model-Viewer)
Per la rappresentazione visiva dei corpi celesti si è optato per un approccio ibrido. Il web component `<model-viewer>` delega al browser il rendering efficiente dei modelli più leggeri (pianeti terrestri), mentre Three.js gestisce il rendering avanzato dei giganti gassosi e della stella.

**HTML** (da `distanze.html`):
```html
<model-viewer id="Earth" src="./assets/earth.glb" auto-rotate rotation-per-second="3.44deg" disable-zoom interaction-prompt="none" camera-orbit="0deg 75deg 105%" style="width:13px;height:13px;" touch-action="none" shadow-intensity="0" exposure="1.5"></model-viewer>

<div id="Jupiter" class="three-planet" data-file="jupiter.glb" data-rot="8" style="width:140px;height:140px;"></div>
```

**CSS** (da `distanze.html`):
```css
model-viewer {
background-color: transparent; --poster-color: transparent; border-radius: 50%;
display: block; flex-shrink: 0; z-index: 5; min-width: 0 !important; min-height: 0 !important; outline: none;
}
model-viewer::part(default-progress-bar), model-viewer::part(default-ar-button), model-viewer::part(default-progress-mask) { display: none; }

.three-planet {
display: block;
flex-shrink: 0;
z-index: 5;
position: relative;
}
```

**JavaScript** (da `distanze.html`):
```javascript
const threePlanetsElements = document.querySelectorAll('.three-planet');
const renderersThree = [];

if(threePlanetsElements.length > 0) {
    const loader = new THREE.GLTFLoader();

    threePlanetsElements.forEach(container => {
        const id = container.id;
        const file = container.getAttribute('data-file');
        const width = parseInt(container.style.width);
        const height = parseInt(container.style.height);

        const scene = new THREE.Scene();

        // [...] Setup luci ambientali e direzionali omesso per brevità

        const camera = new THREE.PerspectiveCamera(45, width / height, 0.1, 5000);
        
        const renderer = new THREE.WebGLRenderer({ antialias: true, alpha: true, powerPreference: "high-performance" });
        renderer.setSize(width, height);
        renderer.setPixelRatio(window.devicePixelRatio);
        container.appendChild(renderer.domElement);

        let modelMesh = null;

        loader.load(`assets/${file}`, (gltf) => {
            const model = gltf.scene;
            const box = new THREE.Box3().setFromObject(model);
            const size = box.getSize(new THREE.Vector3());
            const center = box.getCenter(new THREE.Vector3());

            model.position.set(-center.x, -center.y, -center.z);
            const wrapper = new THREE.Group();
            wrapper.add(model);

            const maxDim = Math.max(size.x, size.y, size.z);
            const scaleFactor = (width * 0.95) / maxDim; 
            wrapper.scale.set(scaleFactor, scaleFactor, scaleFactor);

            // [...] Setup rotazione per Saturno e materiali omesso per brevità

            scene.add(wrapper);
            modelMesh = wrapper;

            const dist = (width / 2) / Math.tan((45 * Math.PI / 180) / 2);
            camera.position.z = dist * 1.05;
            
            renderer.render(scene, camera);
        });

        renderersThree.push({ renderer, scene, camera, getMesh: () => modelMesh });
    });

    // [...] Funzione animateThree() omessa per brevità
}
```


### 2. Dati scientifici in tempo reale (API NASA JPL)
Il rigore della simulazione è garantito dall'integrazione delle API Horizons del NASA JPL. Tramite chiamate asincrone, l'applicazione interroga il database per ottenere i vettori di stato esatti in tempo reale e inietta questi parametri nel DOM o direttamente nelle regole CSS per generare orbite fisicamente accurate. Il sistema implementa anche un array di fallback in caso di fallimento del sync con l'Agenzia Spaziale.

**HTML** (da `distanze.html` e `posizioni.html`):
```html
<p class="info" id="info-Jupiter">Giove (Gigante gassoso)<br>Distanza dal Sole: <span id="disSpa5Km">...</span> km</p>

<div class="orbit orb-mercury"></div>
```

**CSS** (da `posizioni.html`):
```css
/* ORBITE: Rappresentazione geometrica in 2D usando CSS Transform Matrix (NASA JPL style) */
.orbit { 
    position: absolute; 
    border-style: dashed;
    border-color: var(--color-dashed); 
    border-width: 1px; 
    border-radius: 50%; 
    left: 50%; top: 50%; 
    width: calc(var(--semi-a) * 2 * var(--au-to-vmin)); height: calc(var(--semi-b) * 2 * var(--au-to-vmin)); 
    margin-left: calc(var(--semi-a) * var(--au-to-vmin) * -1); margin-top: calc(var(--semi-b) * var(--au-to-vmin) * -1); 
    /* La matematica CSS segue esattamente la proiezione ortografica di J2000 */
    transform: rotateZ(calc(var(--N) * 1deg)) rotateX(calc(var(--i) * 1deg)) rotateZ(calc(var(--w) * 1deg)) translateX(calc(var(--c) * var(--au-to-vmin) * -1)); 
    transform-style: flat;
}
```

**JavaScript** (Estratto Fetch API da `distanze.html`):
```javascript
async function syncWithNasa() {
    for (let i = 1; i < planetsData.length; i++) {
        const p = planetsData[i];
        const url = `https://api.allorigins.win/get?url=${encodeURIComponent(
            `https://ssd.jpl.nasa.gov/api/horizons.api?format=json&COMMAND='${p.nasa}'&OBJ_DATA='NO'&MAKE_EPHEM='YES'&EPHEM_TYPE='VECTORS'&OUT_UNITS='KM-S'&CENTER='500@10'&START_TIME='now'&STOP_TIME='now+1m'&STEP_SIZE='1m'`
        )}`;
        try {
            const r = await fetch(url);
            const j = await r.json();
            const res = JSON.parse(j.contents).result;
            const data = res.split('$$SOE')[1].split('$$EOE')[0].trim().split('\n')[0].split(',');
            
            const x = parseFloat(data[2]), y = parseFloat(data[3]), z = parseFloat(data[4]);
            const vx = parseFloat(data[5]), vy = parseFloat(data[6]), vz = parseFloat(data[7]);
            
            const d = Math.sqrt(x*x + y*y + z*z);
            p.baseDis = d / 1000;
            p.inc = ((x*vx + y*vy + z*vz) / d) / 1000; 

            // [...] Aggiornamento interfaccia domDisKm e proporzioni orbitali
        } catch(e) { 
            console.error("NASA Sync Error per " + p.name, e); 
            p.inc = [0, 0.0042, -0.0001, 0.0005, 0.0021, 0.0015, -0.0012, 0.0008, -0.0002][i];
        }
    }
    // [...]
}
```


### 3. Rendering 2D e Animazioni (Canvas e GSAP)
Per mantenere altissime le prestazioni, gli sfondi stellati con effetto parallasse sono disegnati interamente tramite le API native HTML5 Canvas. Le transizioni complesse (come il viaggio automatico tra i pianeti centrando lo schermo rispetto a parametri dinamici o l'ancoraggio speciale al Sole) sono orchestrate con precisione tramite l'easing avanzato di GSAP.

**HTML** (da `distanze.html`):
```html
<canvas id="stars" class="stars-canvas"></canvas>
<canvas id="stars2" class="stars-canvas"></canvas>
<canvas id="stars3" class="stars-canvas"></canvas>
```

**CSS** (da `distanze.html`):
```css
canvas.stars-canvas {
position: fixed; left: 0; top: 0;
z-index: 0; pointer-events: none; transition: opacity 2s;
}
```

**JavaScript** (da `distanze.html`):
```javascript
// Classe per la generazione e animazione particellare (Canvas API)
class Stars {
    constructor(id, density, maxS, minS, maxSz, minSz) {
        this.canvas = document.getElementById(id); this.ctx = this.canvas.getContext('2d');
        this.density = density; this.maxS = maxS; this.minS = minS; this.maxSz = maxSz; this.minSz = minSz; this.dots = [];
        this.resize(); window.addEventListener('resize', () => this.resize());
    }
    // [...] Funzioni resize() e addDot() omesse per brevità
    draw(delta) {
        const ctx = this.ctx; ctx.clearRect(0, 0, this.canvas.width, this.canvas.height);
        while (this.dots.length < this.num) this.addDot(delta > 0 ? this.rB : this.lB, Math.random() * window.innerHeight);
        for (let i = this.dots.length - 1; i >= 0; i--) {
            const dot = this.dots[i], oldX = dot.x; dot.x -= delta * dot.v;
            ctx.beginPath(); ctx.moveTo(oldX, dot.y + dot.s/2); ctx.lineTo(dot.x, dot.y + dot.s/2);
            ctx.strokeStyle = 'white'; ctx.lineWidth = dot.s; ctx.stroke();
            if (dot.x < this.lB || dot.x > this.rB) this.dots.splice(i, 1);
            else { ctx.fillStyle = 'white'; ctx.fillRect(dot.x, dot.y, dot.s, dot.s); }
        }
    }
}

// GSAP ScrollToPlugin per transizione e centraggio visivo
function autoScroll(targetPla) {
    if (!targetPla || !targetPla.img) return;
    isTraveling = true; traveling.classList.add('traveling-active');
    
    let destX;
    if (targetPla.id === 'Sun') {
        destX = getHomeTargetScrollX();
    } else {
        destX = scrollXToCenter(targetPla.img);
    }

    const abort = () => { gsap.killTweensOf(window); cleanup(); };
    function cleanup() { isTraveling = false; traveling.classList.remove('traveling-active'); window.removeEventListener('wheel', abort); }
    window.addEventListener('wheel', abort, { once: true });
    
    gsap.to(window, {
        duration: 10, 
        scrollTo: { x: destX, autoKill: true }, 
        ease: 'power3.inOut', 
        onUpdate: () => { 
            const r = targetPla.img.getBoundingClientRect(); 
            if (r.right > 0 && r.left < window.innerWidth) traveling.classList.remove('traveling-active'); 
        },
        onComplete: cleanup, onInterrupt: cleanup,
    });
}
```
<br>


## Target e contesto d’uso
Il progetto è rivolto a un pubblico generalista, in particolare a persone con conoscenze limitate o di base sul Sistema solare e sui pianeti, ma interessate alla scoperta dello spazio, alla divulgazione scientifica e alla comprensione dei dati attraverso la visualizzazione.<br>

La piattaforma si inserisce in un contesto di uso principalmente educativo e divulgativo, pensato per essere consultato online in modo autonomo. Può essere utilizzata in ambiti scolastici e formativi, oppure come strumento di esplorazione personale per comprendere in modo intuitivo le proporzioni e le dinamiche del Sistema solare attraverso un’esperienza interattiva.
