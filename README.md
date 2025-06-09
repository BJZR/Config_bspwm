
‎````markdown
‎# BSPWM Configuración Estética y Funcional
‎
‎Este repositorio contiene una configuración base y funcional para usar `bspwm` como gestor de ventanas, junto con herramientas esenciales como `sxhkd`, `lemonbar`, `rofi`, `picom`, `dunst`, `xclip`, y utilidades para brillo, volumen y portapapeles.
‎
‎---
‎
‎## 🧰 Aplicaciones necesarias
‎
‎Asegúrate de tener instaladas las siguientes aplicaciones:
‎
‎```sh
‎xbps-install -S bspwm sxhkd feh rofi dunst picom xclip xbacklight alsa-utils kitty i3lock
‎````
‎
‎---
‎
‎## 🗂️ Estructura del directorio
‎
‎```
‎.config/
‎└── bspwm/
‎    ├── bspwmrc              # Config principal de bspwm
‎    ├── sxhkdrc              # Atajos de teclado
‎    ├── autostart.sh         # Lanzadores automáticos (feh, picom, etc.)
‎    ├── lemonbar.sh          # Barra de estado básica
‎    ├── lock.sh              # Bloqueo de pantalla
‎    ├── config/
‎    │   ├── picom.conf       # Config de transparencia y efectos
‎    │   ├── dunstrc          # Config del sistema de notificaciones
‎    │   ├── wallpaper.jpg    # Fondo de pantalla
‎    │   └── rofi-theme.rasi  # Tema personalizado para Rofi
‎    └── utils/
‎        ├── brightness.sh    # Control de brillo
‎        ├── volume.sh        # Control de volumen
‎        └── clipboard.sh     # Mostrar portapapeles
‎```
‎
‎---
‎
‎## ⚙️ Instalación
‎
‎1. Clona o descarga este repositorio.
‎2. Copia el contenido a tu `~/.config/`:
‎
‎   ```sh
‎   cp -r .config/bspwm ~/.config/
‎   ```
‎3. Da permisos de ejecución a los scripts:
‎
‎   ```sh
‎   chmod +x ~/.config/bspwm/*.sh ~/.config/bspwm/utils/*.sh
‎   ```
‎
‎---
‎
‎## ⌨️ Atajos de teclado destacados
‎
‎* `Super + Enter` → Abrir Kitty
‎* `Super + D` → Abrir Rofi
‎* `Super + Shift + X` → Bloquear pantalla
‎* `XF86Audio*` → Control de volumen
‎* `XF86MonBrightness*` → Control de brillo
‎
‎---
‎
‎## 💡 Notas
‎
‎* Puedes personalizar los colores y fuentes modificando los archivos de configuración.
‎* El archivo `autostart.sh` se encarga de iniciar los servicios al entrar al entorno gráfico.
‎
‎---
‎
‎## 🎨 Créditos
‎
‎Configuración personalizada por **Brayan José Zambrano Ruíz**
‎*"Un chico con más ganas de aprender."*
‎
