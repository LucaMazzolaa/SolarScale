SUPSI 2026  
Corso d’interaction design, CV429.01  
Docenti: A. Gysin, G. Profeta  

Progetto 1: La conquista dello spazio

# SISTEMA SOLARE IN SCALA
Autore: Luca Mazzola \
[SISTEMA SOLARE IN SCALA](https://lucamazzolaa.github.io/NASA70/)


## Introduzione e tema
Questo progetto esplora il Sistema solare a partire da una criticità evidente: molte delle rappresentazioni diffuse risultano poco accurate nel restituire le reali proporzioni tra dimensioni dei pianeti e distanze li separano nello spazio. La scala del Sistema è infatti così vasta da rendere impossibile una visualizzazione fedele all’interno di un’unica immagine, portando spesso a semplificazioni e alterazioni che ne compromettono la comprensione.<br>

Per affrontare questo limite, il progetto scompone il Sistema solare in tre elementi principali: dimensioni dei pianeti, posizioni e movimenti nel tempo, e distanze dal Sole. Questa scelta permette di costruire visualizzazioni più chiare, leggibili e coerenti.<br>

Ne deriva una visualizzazione interattiva capace di tradurre dati scientifici in un’esperienza visiva immediata, rendendo percepibili proporzioni normalmente astratte e restituendo in modo efficace la reale struttura e scala del Sistema solare.


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



## Design dell’interfaccia e modalità di interazione
Facilisis magna etiam tempor orci eu. Felis donec et odio pellentesque diam volutpat commodo. Dis parturient montes nascetur ridiculus mus mauris vitae. Nisi vitae suscipit tellus mauris a diam maecenas sed enim. Accumsan sit amet nulla facilisi. Ultricies leo integer malesuada nunc vel risus. Est lorem ipsum dolor sit. Ultrices neque ornare aenean euismod elementum nisi. Ultrices mi tempus imperdiet nulla malesuada pellentesque elit eget gravida. Placerat duis ultricies lacus sed turpis tincidunt id aliquet. Arcu dictum varius duis at consectetur lorem donec massa sapien. Pellentesque habitant morbi tristique senectus. Turpis massa sed elementum tempus egestas sed sed risus pretium. Eros donec ac odio tempor orci. Pellentesque id nibh tortor id aliquet lectus. Risus feugiat in ante metus dictum at. Quam pellentesque nec nam aliquam sem et tortor consequat id. Feugiat nibh sed pulvinar proin gravida hendrerit lectus a. Sit amet dictum sit amet justo donec enim.

https://github.com/user-attachments/assets/38d1768e-a90e-45dd-b12b-1ac0aa1151b3

[<img src="doc/cards.gif" width="500" alt="Magic trick">]()


## Tecnologia usata
Nunc consequat interdum varius sit amet mattis vulputate. Vehicula ipsum a arcu cursus vitae congue. Odio ut sem nulla pharetra. Accumsan lacus vel facilisis volutpat est velit egestas dui id. Quisque egestas diam in arcu cursus. Eget nulla facilisi etiam dignissim diam. Aenean sed adipiscing diam donec adipiscing tristique. Porttitor massa id neque aliquam. Sem viverra aliquet eget sit amet tellus cras. Scelerisque eu ultrices vitae auctor eu augue ut lectus. Nunc aliquet bibendum enim facilisis gravida neque convallis a. Lacus sed turpis tincidunt id aliquet risus feugiat.


```JavaScript
const image = new Image();
image.onload = () => {
	gl.bindTexture(gl.TEXTURE_2D, texture);
	gl.texImage2D(
		gl.TEXTURE_2D,
		level,
		internalFormat,
		srcFormat,
		srcType,
		image
	);
	if (isPowerOf2(image.width) && isPowerOf2(image.height)) {
		gl.generateMipmap(gl.TEXTURE_2D);
	} else {
		gl.texParameteri(gl.TEXTURE_2D, gl.TEXTURE_WRAP_S, gl.CLAMP_TO_EDGE);
		gl.texParameteri(gl.TEXTURE_2D, gl.TEXTURE_WRAP_T, gl.CLAMP_TO_EDGE);
		gl.texParameteri(gl.TEXTURE_2D, gl.TEXTURE_MIN_FILTER, gl.LINEAR);
	}
};
image.src = url;
```

## Target e contesto d’uso
Sed enim ut sem viverra aliquet eget sit. Iaculis at erat pellentesque adipiscing commodo. Et pharetra pharetra massa massa ultricies mi quis hendrerit dolor. At tempor commodo ullamcorper a lacus vestibulum sed arcu. Ipsum faucibus vitae aliquet nec ullamcorper sit. Tempus quam pellentesque nec nam aliquam sem et tortor. Turpis egestas sed tempus urna et pharetra pharetra massa. Ridiculus mus mauris vitae ultricies leo integer malesuada nunc vel.
