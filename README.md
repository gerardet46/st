# Simple terminal (st) de gerardet46

Això és la meva versió configurada de [simple terminal](https://st.suckless.org/), de suckless. Està inspirat en la configuració de 
[luke smith](https://github.com/lukesmithxyz/st) però s'ha creat a partir de la versió 0.8.4 oficial a suckless.org, afegint els pedaços que trobava necessaris.

## Taula de continguts
1. [ Filosofia ](#filo)
2. Característiques

      2.1. [ Característiques de Luke Smith ](#luke)
  
      2.2. [ Dreceres de teclat ](#tecles)
  
      2.3. [ Pedaços i temes ](#draps)
  
3. [ Nota pels emoji ](#emoji)
4. [ Instal·lació i configuració ](#make)

<a name="filo"></a>
## Filosofia
Seguint un poc la filosofia de _suckless_, aquesta versió de `st` no permetrà que es pugui cnaviar la configuració amb fitxers clàssics de configuració. Per canviar-la,
s'haurà de canviar el propi codi font, que ho fa més segur i ràpid.

Per això, si voleu instal·lar un altre tema, simplement editau els colors al fitxer `config.h`, que és el fitxer on es configura el terminal però no
s'implementar

<a name="luke"></a>
## Característiques de luke smith
- **Seguir enllaços** pressionant `alt-l`
- **Copiar enllaços** pressionant `alt-y`
- **Copiar sortida de les ordres** amb `alt-o`

<a name="tecles"></a>
## Dreceres de teclat afegides
Es podem canviar a `config.h`
- Desplaçament _ràpid_ amb `shift-Re/Av pàg`
- Desplaçament _gradual_ amb `alt-↑/↓`
- Zoom (fer més gran la font): `ctrl-+/-`
- s'ha afegit el bon funcionament de la tecla `Supr`, adaptat ara pels teclats `es` com el meu

<a name="draps"></a>
## Pedaços i temes
Tots els pedaços es poden veure en l'arrel del respositori com a fitxers `.diff`
- `Dracula`: tema per defecte (i l'únic instal·lat)
- `alpha` per transparència
- `blinking cursor` per cursor típic parpadejant
- `externalpipe` per emprar `dmenu` adins `st`
- `scrollback` per desplaçament vertical
- Utilitza la font **Ubuntu Mono** per defecte

<a name="emoji"></a>
## Nota pels emojis
El programari pot sortir inesperadament al inserir emojis. Per això és recomanable fer el següent:
- Instal·lar una font d'emojis (`noto-fonts-emoji` a l'AUR, per exemple)
- Tenir instal·lat `libxft-bgra` (és disponible a l'AUR, suprimir `libxft` en cas de conflictes)

<a name="make"></a>
## Instal·lació i configuració
Es pot instalar clonant el repositori i compilant el codi font:
```bash
git clone https://github.com/gerardet46/st
cd st
sudo make install clean
```
Per configurar-lo es pot editar el fitxer `config.h`, que és on es desen les configuracions del terminal per després compilar-les.

Per més personalització, es poden afegir pedaços i/o editar directament el codi font
