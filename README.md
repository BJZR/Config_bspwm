
‎# Configuración personalizada para bspwm
‎
‎Este repositorio contiene una configuración organizada y lista para usar de **bspwm** junto con herramientas complementarias como **sxhkd**, **lemonbar**, **rofi**, **dunst**, **picom**, y utilidades personalizadas para brillo y portapapeles. Todo está centralizado dentro de la carpeta `~/.config/bspwm/` para facilitar la personalización y mantenimiento.
‎
‎---
‎
‎## Estructura de carpetas y archivos
‎
‎```
‎
‎.config/
‎└── bspwm/
‎├── bspwmrc              # Configuración principal de bspwm
‎├── sxhkdrc              # Configuración de atajos de teclado (sxhkd)
‎├── autostart.sh         # Script para iniciar aplicaciones al arrancar bspwm
‎├── lemonbar.sh          # Barra de estado personalizada con lemonbar
‎├── lock.sh              # Script para bloqueo de pantalla (usando i3lock)
‎├── config/
‎│   ├── picom.conf       # Configuración de picom (compositor)
‎│   ├── dunstrc          # Configuración para notificaciones dunst
‎│   ├── wallpaper.jpg    # Imagen para fondo de pantalla
‎│   └── rofi-theme.rasi  # Tema personalizado para rofi
‎└── utils/
‎├── brightness.sh    # Script para controlar brillo de pantalla
‎├── volume.sh        # Script para controlar volumen
‎└── clipboard.sh     # Script simple para portapapeles (xclip)
‎
‎````
‎
‎---
‎
‎## Requisitos
‎
‎Antes de usar esta configuración, asegúrate de tener instaladas las siguientes aplicaciones y herramientas:
‎
‎- `bspwm`
‎- `sxhkd`
‎- `feh`
‎- `rofi`
‎- `dunst`
‎- `picom`
‎- `xclip`
‎- `xbacklight`
‎- `amixer`
‎- `kitty`
‎- `i3lock`
‎
‎Puedes instalar estas aplicaciones mediante tu gestor de paquetes (por ejemplo, `xbps-install` en Void Linux):
‎
‎```bash
‎sudo xbps-install -S bspwm sxhkd feh rofi dunst picom xclip xbacklight alsa-utils kitty i3lock
‎````
‎
‎---
‎
‎## Instalación
‎
‎1. Clona este repositorio o descarga y descomprime el archivo `.zip`:
‎
‎```bash
‎unzip bspwm-config.zip -d ~/
‎```
‎
‎2. Da permisos de ejecución a los scripts:
‎
‎```bash
‎chmod +x ~/.config/bspwm/*.sh ~/.config/bspwm/utils/*.sh
‎```
‎
‎3. Inicia `bspwm` (por ejemplo, configurando tu gestor de inicio de sesión para usarlo o arrancándolo desde `.xinitrc`):
‎
‎```bash
‎exec bspwm
‎```
‎
‎---
‎
‎## Uso
‎
‎* Los atajos de teclado se manejan con `sxhkd`. Para iniciar:
‎
‎```bash
‎sxhkd -c ~/.config/bspwm/sxhkdrc &
‎```
‎
‎* La barra está configurada con `lemonbar`, se inicia automáticamente con `autostart.sh`.
‎
‎* El fondo de pantalla se configura con `feh` desde `autostart.sh`.
‎
‎* El compositor es `picom`, iniciado también desde `autostart.sh`.
‎
‎* Las notificaciones se manejan con `dunst`.
‎
‎* Los scripts en `utils/` controlan el brillo, volumen y portapapeles, y están enlazados a atajos en `sxhkdrc`.
‎
‎---
‎
‎## Personalización
‎
‎* Cambia el wallpaper reemplazando `~/.config/bspwm/config/wallpaper.jpg`.
‎
‎* Modifica el tema de `rofi` en `~/.config/bspwm/config/rofi-theme.rasi`.
‎
‎* Ajusta `picom.conf` para efectos de composición.
‎
‎* Agrega o modifica atajos en `sxhkdrc`.
‎
‎---
‎
‎## Bloqueo de pantalla
‎
‎El script `lock.sh` usa `i3lock` para bloquear la pantalla:
‎
‎```bash
‎./lock.sh
‎```
‎
‎Puedes personalizar el color o cambiar el método de bloqueo si lo deseas.
