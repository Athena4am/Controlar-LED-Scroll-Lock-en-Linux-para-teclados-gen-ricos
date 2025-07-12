# Controlar LED Scroll Lock en Linux para teclados genéricos

Este repositorio ayuda a quienes usan teclados genéricos con un solo LED funcional (Scroll Lock) en Linux, y tienen problemas para encenderlo o apagarlo desde el entorno gráfico o terminal.

---

## Problemas comunes

- Solo el LED de **Scroll Lock** funciona.
- Los métodos tradicionales (`setleds`, `xset`) no funcionan bien en Wayland/X11.
- El LED se apaga al salir de la consola TTY.
- Scroll Lock en TTY puede bloquear la salida de la terminal.

---

## Solución con `brightnessctl`

### 1. Instala `brightnessctl`

```bash
sudo pacman -S brightnessctl
