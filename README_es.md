# Simple terminal (st) de gerardet46

Esta es mi versión configurada de [simple terminal](https://st.suckless.org/), de suckless. Está inspirado en la configuración de [luke
smith](https://github.com/lukesmithxyz/st) pero se ha creado a partir de la versión 0.8.4 oficial a suckless.org, añadiendo los parches que encontraba necesarios.

[ README en català ](README.md)

## Tabla de contenidos
1. [ Filosofía ](#filo)
2. Características

2.1. [ Características de Luke Smith ](#luke)

2.2. [ Atajos de teclado ](#tecles)

2.3. [ Parches y temas ](#draps)

3. [ Nota por los emoji ](#emoji)
4. [ Instalación y configuración ](#make)

<a name="filo"></a>
## Filosofía
Siguiendo un poco la filosofía de _suckless_, esta versión de `st` no permitirá que se pueda cambiar la configuración con ficheros clásicos de configuración. Para cambiarla,
se tendrá que cambiar y compilar el propio código fuente, que lo hace más seguro y rápido.

Por eso, si queréis instalar otro tema, por ejemplo, simplemente editáis los colores en el fichero `config.h`, que es el fichero donde se configura el terminal y compiláis para
hacer realidad los cambios.

También se puede cambiar el archivo `~/.Xresources`, usando la clase `St` (ver `config.h`) para cambiar la estética del terminal

<a name="luke"></a>
## Características de luke smith
- **Seguir enlaces** presionando `alt-l`
- **Copiar enlaces** presionando `alt-y`
- **Copiar salida de las órdenes** con `alt-o`
- **Editar texto del terminal en el editor** con `alt-e`

<a name="tecles"></a>
## Atajos de teclado añadidas
Se pueden cambiar en `config.h`
- Desplazamiento _rápido_ con `shift-Re/*Av pàg`
- Desplazamiento _gradual_ con `alt-↑/↓`
- Zoom (hacer más grande la fuente): `ctrl-+/-`
- se ha añadido el buen funcionamiento de la tecla `Supr`, adaptado ahora por los teclados `es` como en mi caso.

<a name="draps"></a>
## Parches y temas
Todos los parches se pueden ver en la raíz del respositori como ficheros `.diff`
- `xresources` para configurar la estética `~/.Xresources`
- `alpha` por transparencia
- `font2` para los emojis
- `blinking cursor` por cursor típico parpadejant
- `externalpipe` para emplear `dmenu` dentro de `st`
- `scrollback` por desplazamiento vertical
- `newterm` para abrir un nuevo terminal con `C-S-Enter`
- Utiliza la fuente **Ubuntu Mono** por defecto

<a name="emoji"></a>
## Nota por los emojis
El software puede salir inesperadamente al insertar emojis. Por eso es recomendable hacer lo siguiente:
- Instalar una fuente de emojis (`noto-fonts-emoji` a la AUR, por ejemplo)
- Tener instalado `libxft-bgra` (está disponible a la AUR, suprimir `libxft` en caso de conflictos)

<a name="make"></a>
## Instalación y configuración
Se puede instalar clonando el repositorio y compilando el código fuente:
```bash
git clone https://github.com/gerardet46/st
cd st
sudo make install clean
```
Para configurarlo se puede editar el fichero `config.h`, que es donde se guardan las configuraciones del terminal para después compilarlas.

Por más personalización, se pueden añadir parches o editar directamente el código fuente
