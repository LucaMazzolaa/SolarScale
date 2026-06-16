SUPSI 2026  
Corso d’interaction design, CV429.01  
Docenti: A. Gysin, G. Profeta  

Progetto 1: La conquista dello spazio

# SolarScale
Autore: Luca Mazzola \
[SolarScale](https://lucamazzolaa.github.io/SolarScale/)


## Introduzione e tema
Questo progetto esplora il Sistema Solare a partire da una criticità evidente: molte delle rappresentazioni diffuse risultano poco accurate nel restituire le reali proporzioni tra dimensioni dei pianeti e distanze che li separano nello spazio. La scala del Sistema è infatti così vasta da rendere impossibile una visualizzazione fedele all’interno di un’unica immagine, portando spesso a semplificazioni e alterazioni che ne compromettono la comprensione.<br>

Per affrontare questo limite, il progetto scompone il Sistema Solare in tre elementi principali: dimensioni dei pianeti, posizioni e movimenti nel tempo, e distanze dal Sole. Ne deriva una visualizzazione interattiva capace di tradurre dati scientifici in un’esperienza visiva immediata, rendendo percepibili proporzioni normalmente astratte e restituendo in modo efficace la reale struttura e scala del Sistema Solare.


## Riferimenti progettuali
<img width="4000" height="750" alt="immagini" src="https://github.com/user-attachments/assets/055426aa-bca7-48fc-af18-38c913d98b09" />

A livello di funzione e di visualizzazione, il progetto si è basato su tre riferimenti principali, scelti in relazione ai tre temi in cui il Sistema Solare è stato scomposto, con l’obiettivo di avvicinarsi il più possibile a una rappresentazione chiara e fedele delle proporzioni. Per il tema delle dimensioni, il riferimento principale è il seguente [video](https://www.youtube.com/watch?v=i93Z7zljQ7I&t=29s) che mette in evidenza in modo immediato e comparativo le reali scale tra i pianeti. La sua efficacia risiede nella capacità di tradurre dati numerici complessi in un confronto visivo diretto. Per posizioni e rotazioni, è stato utilizzato come base lo [strumento interattivo](https://ssd.jpl.nasa.gov/tools/orbit_viewer.html) che permette di osservare in modo semplificato i movimenti orbitali in tempo reale e comprendere le relazioni dinamiche tra i corpi celesti. Per le distanze dal Sole, il riferimento chiave è la [pagina web](https://joshworth.com/dev/pixelspace/pixelspace_solarsystem.html) che rappresenta in modo efficace la reale vastità degli spazi tra i pianeti, rendendo percepibile ciò che normalmente risulta astratto.


## Design dell’interfaccia e modalità di interazione
Il design è concepito per offrire un’esperienza immersiva e minimale. L’interfaccia si ispira all’immaginario dell’esplorazione spaziale e della ricerca scientifica, utilizzando uno sfondo nero profondo arricchito da un campo di piccole stelle che immerge immediatamente l’utente nell’ambiente cosmico. La tipografia bianca, basata sul font Neue Montreal, garantisce chiarezza e leggibilità, mentre un cursore personalizzato si adatta dinamicamente agli elementi interattivi. L’interfaccia segue il principio della rivelazione progressiva. L’utente accede inizialmente a uno spazio minimale e, man mano che esplora i contenuti, vengono introdotti nuovi livelli di informazione e strumenti di navigazione, accompagnando la scoperta delle visualizzazioni in modo graduale e intuitivo.

### Pagine del sito
| N. | File | Pagina | Contenuto |
| :--- | :--- | :--- | :--- |
| 1 | **`index.html`** | SolarScale | Introduzione tipografica al progetto |
| 2 | **`sizes.html`** | Sizes | Confronto scala pianeti |
| 3 | **`positions.html`** | Positions | Mappa orbitale con movimenti dei pianeti |
| 4 | **`distances.html`** | Distances | Distanze tra i pianeti |
| 5 | **`measurement.html`** | Measurement Methods | Sezione informativa sui metodi di misurazione |
| 6 | **`credits.html`** | Credits | Informazioni di autore e contesto |


### Menu globale fisso
<img width="1919" height="106" alt="menu" src="https://github.com/user-attachments/assets/3699adfd-65c9-4108-8c85-2df229837fce" />

Il menu superiore costituisce l’elemento di navigazione principale e rimane costante in tutte le pagine per garantire orientamento e coerenza visiva. A sinistra sono presenti il logo e il nome del progetto SolarScale, seguiti sulla destra dalle sezioni Sizes, Positions e Distances. Sulla parte destra del menu si trovano invece le sezioni Measurement Methods e Credits, completando la struttura e garantendo una chiara organizzazione gerarchica dei contenuti e un accesso diretto alle diverse aree del progetto.


### Logo
<img width="4000" height="750" alt="logo" src="https://github.com/user-attachments/assets/2d181193-5229-4b65-b59d-a841a38d0a86" />

Il logo del progetto si ispira a uno dei più antichi simboli associati al Sole, rappresentato da un cerchio con un punto centrale. Utilizzato nel corso della storia in ambito astronomico, astrologico e simbolico, questo segno identifica il Sole come centro e origine di un sistema.
La scelta di questo simbolo è strettamente legata al contenuto del progetto. Nel Sistema Solare il Sole rappresenta infatti il punto centrale attorno al quale orbitano tutti i pianeti e costituisce il principale riferimento per comprenderne dimensioni, posizioni e distanze. Il marchio sintetizza quindi il concetto di centralità, orientamento e relazione tra i corpi celesti, traducendo in forma grafica il tema stesso dell’esplorazione delle proporzioni del Sistema Solare.


### 1. SolarScale (index.html)
<img width="4000" height="1994" alt="03_1920_1080" src="https://github.com/user-attachments/assets/b4d11310-72dd-49f8-9d62-fd6b777c1a3d" />

La pagina iniziale si presenta come un’introduzione tipografica al progetto e al tema della rappresentazione delle proporzioni del Sistema Solare. L’interfaccia, volutamente essenziale, funge da punto di ingresso all’esperienza e accompagna l’utente verso l’esplorazione delle sezioni successive. Inoltre, piccole animazioni circolari integrate nel testo richiamano i temi di dimensioni, posizioni e distanze, anticipando visivamente le visualizzazioni che verranno approfondite nelle pagine dedicate.


### 2. Sizes (sizes.html)
<img width="4000" height="1994" alt="03_1920_10802" src="https://github.com/user-attachments/assets/0bf639cb-52c9-4ddd-916d-cb007793de50" />

La pagina Sizes è dedicata al confronto delle dimensioni dei pianeti attraverso una visualizzazione che ne mostra le reali proporzioni. La pagina si apre con un titolo e un breve testo introduttivo che contestualizzano il contenuto. Attraverso il principio "Scroll to explore", l’utente dissolve progressivamente questa introduzione e accede alla visualizzazione interattiva sottostante, navigabile orizzontalmente. La navigazione è supportata da una barra con le icone dei pianeti posizionata nella parte inferiore dello schermo, che consente di raggiungere rapidamente i diversi corpi celesti. Ai lati compaiono inoltre frecce di navigazione che mostrano in anteprima il nome del pianeta e il relativo diametro, facilitando il confronto tra le diverse scale.


### 3. Positions (positions.html)
<img width="4000" height="1994" alt="03_1920_10803" src="https://github.com/user-attachments/assets/12c3f065-a933-4a65-a34d-c6a4e802885e" />

La pagina Positions presenta una mappa orbitale interattiva che visualizza le posizioni e i movimenti dei pianeti nel tempo. Anche in questo caso l’accesso alla simulazione avviene attraverso il gesto "Scroll to explore", che trasforma l’introduzione testuale in uno spazio di osservazione dinamico. Nella parte inferiore è presente un pannello di controllo che permette di modificare la velocità della simulazione, mettere in pausa il sistema, avanzare nel tempo e monitorare la data visualizzata. I controlli di zoom, collocati nell'angolo inferiore destro, consentono invece di osservare il Sistema Solare a differenti livelli di dettaglio.


### 4. Distances (distances.html)
<img width="4000" height="1994" alt="03_1920_10804" src="https://github.com/user-attachments/assets/2ad7107f-ea9f-4900-a0e4-8d3e00207c7e" />

La pagina Distances esplora le reali distanze tra i pianeti e il Sole, mettendo in evidenza la vastità degli spazi interplanetari. Attraverso il gesto "Scroll to explore", l’utente avanza progressivamente all’interno della visualizzazione e scopre le relazioni spaziali tra i diversi corpi celesti. Una barra di navigazione posta nella parte inferiore permette di spostarsi rapidamente tra i pianeti, rappresentati in modo proporzionale lungo il percorso. Le frecce laterali mostrano invece informazioni sintetiche sulle distanze tra un pianeta e l’altro, facilitando la comprensione delle reali scale del sistema.


### 5. Measurement Methods (measurement.html)
<img width="4000" height="1994" alt="03_1920_10805" src="https://github.com/user-attachments/assets/d99aac3b-0eb6-43f2-8f95-d681108b7ebf" />

La pagina Measurement Methods è concepita come uno spazio informativo dedicato ai metodi utilizzati per misurare dimensioni, posizioni e distanze nel Sistema Solare. A differenza delle altre sezioni, l’interazione segue il principio "Scroll to read" e si basa esclusivamente sulla lettura dei contenuti. Lo scorrimento verticale guida l’utente attraverso testi esplicativi, immagini e materiali video senza l’introduzione di ulteriori strumenti di navigazione o pannelli di controllo.


### 6. Credits (credits.html)
<img width="4000" height="1994" alt="03_1920_10806" src="https://github.com/user-attachments/assets/9c6e99a6-ff4f-497d-88f1-3e96fd73f728" />

La pagina Credits raccoglie le informazioni relative all’autore del progetto e al contesto di realizzazione.


## Tecnologia usata

Il progetto poggia su una solida architettura front-end nativa, sviluppata in **HTML5, CSS3 e JavaScript (ES6)**. HTML definisce la struttura semantica dell’interfaccia, mentre CSS ne gestisce l’estetica attraverso un design system basato su variabili, calcoli fluidi e tipografia personalizzata. JavaScript funge da motore logico dell’applicazione: orchestra il DOM, gestisce gli eventi dell’utente e sincronizza l’interfaccia con i dati e le librerie esterne.<br>

Di seguito vengono presentati tre estratti di codice chiave tratti dal file **`distances.html`**, fondamentali per lo sviluppo del progetto in quanto rappresentano le principali logiche di interazione e visualizzazione. Questo file integra infatti l’intero sistema di navigazione e gestione dei dati della sezione, combinando struttura, comportamento e relazione tra i diversi elementi dell’interfaccia.<br>


### 1. Motore grafico 3D (Three.js e Model-Viewer)
Per la rappresentazione visiva dei corpi celesti si è optato per un approccio ibrido. Il web component `<model-viewer>` delega al browser il rendering efficiente dei modelli più leggeri (pianeti terrestri), mentre Three.js gestisce il rendering avanzato dei giganti gassosi e della stella. Le prestazioni sono ulteriormente ottimizzate da un `IntersectionObserver` nativo che sospende il ricalcolo dei frame per i modelli 3D non attualmente visibili nel viewport.

**HTML**
```html
<model-viewer id="Earth" src="./assets/earth.glb" auto-rotate rotation-per-second="3.44deg" disable-zoom interaction-prompt="none" camera-orbit="0deg 75deg 105%" style="width:13px;height:13px;" touch-action="none" shadow-intensity="0" exposure="1.5"></model-viewer>

<div id="Jupiter" class="three-planet" data-file="jupiter.glb" data-rot="8" style="width:143px;height:143px;"></div>
```

**CSS**
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

**JavaScript**
```javascript
const threePlanetsElements = document.querySelectorAll('.three-planet');
const renderersThree = [];

// Ottimizzazione tramite Intersection Observer
let planetObserver = null;
if (window.IntersectionObserver) {
    planetObserver = new IntersectionObserver((entries) => {
        entries.forEach(entry => {
            const r = renderersThree.find(obj => obj.container.id === entry.target.id);
            if (r) r.isVisible = entry.isIntersecting;
        });
    }, { rootMargin: '100% 0px 100% 0px' });
}

if(threePlanetsElements.length > 0) {
    const loader = new THREE.GLTFLoader();

    threePlanetsElements.forEach(container => {
        // [...] Setup scena, luci, camera e renderer omesso per brevità
        
        loader.load(`assets/${file}`, (gltf) => {
            const model = gltf.scene;
            // [...] Adattamento mesh e materiali omesso per brevità
            scene.add(wrapper);
            modelMesh = wrapper;
        });

        const renderObj = { renderer, scene, camera, getMesh: () => modelMesh, container, isVisible: false };
        renderersThree.push(renderObj);
        
        if (planetObserver) planetObserver.observe(container);
    });

    function animateThree() {
        requestAnimationFrame(animateThree);
        renderersThree.forEach(r => {
            // Renderizza solo se l'elemento è effettivamente visibile sullo schermo
            if (r.isVisible || !planetObserver) {
                const mesh = r.getMesh();
                if (mesh) mesh.children[0].rotation.y += 0.001;
                r.renderer.render(r.scene, r.camera);
            }
        });
    }
    animateThree();
}
```


### 2. Dati scientifici in tempo reale (API NASA JPL)
Il rigore della simulazione è garantito dall’integrazione delle API Horizons del NASA JPL. Tramite chiamate asincrone, l’applicazione interroga il database per ottenere i vettori di stato esatti in tempo reale. Questi parametri vengono iniettati nel DOM per aggiornare i chilometri di distanza e per calcolare matematicamente la proporzione visiva tra perielio e afelio adattando dinamicamente la larghezza dei blocchi strutturali CSS.

**HTML**
```html
<div class="planetdiv" id="div-Mercury">
    <div class="perihelion"><div></div></div>
    <div class="planet-cell">
        <model-viewer id="Mercury" src="./assets/mercury.glb" ...></model-viewer>
        <div class="info" id="info-Mercury">
            <div class="info-title"><span style="font-weight:500;">Mercury</span> (Terrestrial planet)</div>
            <div class="data-brackets">
                <div class="info-grid">
                    <span>Distance from the Sun</span><span><span id="disSpa1Km">...</span> km</span>
                </div>
            </div>
        </div>
    </div>
    <div class="aphelion"><div></div></div>
</div>
```

**CSS**
```css
.perihelion, .aphelion { 
    flex-shrink: 0; 
    height: 10px; 
    background-image: url("data:image/svg+xml,..."); 
    background-repeat: repeat-x; 
    background-position: left center;
    align-self: center; 
}
.perihelion > div, .aphelion > div { 
    display: block; height: 100%; width: 100%; 
}
```

**JavaScript**
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

            // Calcolo flessibile della rappresentazione visiva perielio/afelio
            if (p.periEl && p.aphEl && p.totalFlex > 0) {
                let progress = (p.baseDis - p.peri) / (p.aph - p.peri);
                if (progress < 0) progress = 0;
                if (progress > 1) progress = 1;
                
                let periW = p.totalFlex * progress;
                p.periEl.style.width = periW + "px";
                p.aphEl.style.width = (p.totalFlex - periW) + "px";
            }
            
            // Aggiornamento posizione navigatore in sidebar
            if (p.sidebarItemDiv && p.id !== 'Sun') {
                p.sidebarItemDiv.style.left = (p.baseDis / shrinkerFactor) + "px";
            }
        } catch(e) { 
            console.error("NASA Sync Error for " + p.name, e); 
            // Vettori di scorta in caso di indisponibilità del server
            p.inc = [0, 0.0042, -0.0001, 0.0005, 0.0021, 0.0015, -0.0012, 0.0008, -0.0002][i];
        }
    }
}
```


### 3. Rendering 2D e animazioni (Canvas e GSAP)
Per mantenere altissime le prestazioni durante la navigazione orizzontale, gli sfondi stellati con effetto parallasse sono disegnati e calcolati interamente tramite le API native HTML5 Canvas. Le transizioni complesse (come il viaggio automatico tra i pianeti centrando perfettamente lo schermo rispetto ai parametri dinamici o il ritorno rapido al Sole) sono orchestrate tramite il motore di animazione ScrollToPlugin di GSAP.

**HTML**
```html
<canvas id="stars"  class="stars-canvas"></canvas>
<canvas id="stars2" class="stars-canvas"></canvas>
<canvas id="stars3" class="stars-canvas"></canvas>
```

**CSS**
```css
canvas.stars-canvas {
    position: fixed; left: 0; top: 0;
    z-index: 0; pointer-events: none; transition: opacity 2s;
}
```

**JavaScript**
```javascript
/// Classe di generazione particellare per i layout stellati
class Stars {
    constructor(id, density, maxS, minS, maxSz, minSz) {
        this.canvas = document.getElementById(id); this.ctx = this.canvas.getContext('2d');
        this.density = density; this.maxS = maxS; this.minS = minS; this.maxSz = maxSz; this.minSz = minSz; this.dots = [];
        this.resize(); window.addEventListener('resize', () => this.resize());
    }
    // [...] Funzioni logiche resize() e addDot() omesse per brevità
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

// Navigazione assistita e calcolo viewport con GSAP ScrollToPlugin
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


## Target e contesto d’uso
Il progetto è rivolto a un pubblico generalista internazionale, proveniente da diverse aree geografiche, con conoscenze limitate o di base sul Sistema Solare e sui pianeti, ma interessato alla scoperta dello spazio, alla divulgazione scientifica e alla comprensione dei dati attraverso la visualizzazione. L’interfaccia è pensata per essere accessibile a utenti di età eterogenea, indicativamente da adolescenti e studenti fino a un pubblico adulto, senza richiedere competenze scientifiche o tecniche specifiche.<br>

La piattaforma si inserisce in un contesto di uso principalmente educativo e divulgativo, pensato per essere consultato online in modo autonomo. Può essere utilizzata in ambiti scolastici e formativi, oppure come strumento di esplorazione personale per comprendere in modo intuitivo le proporzioni e le dinamiche del Sistema Solare attraverso un’esperienza interattiva.
