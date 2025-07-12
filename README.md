# Controlar LED Scroll Lock en Linux para teclados genéricos

Este repositorio ayuda a usuarios con teclados genéricos que solo tienen un LED funcional (Scroll Lock) y que no pueden controlar las luces desde el entorno gráfico o TTY usando métodos tradicionales como `setleds`.

---

## Problema común

- Solo el LED de **Scroll Lock** funciona físicamente.
- El LED de Scroll Lock puede bloquear la terminal en TTY, haciendo que no se muestre lo que escribes.
- Los comandos tradicionales (`setleds`, `xset`) no funcionan bien en entornos gráficos modernos (Wayland/X11).
- El LED se apaga al salir de la consola TTY.

---

## Solución efectiva

Usar [`brightnessctl`](https://github.com/Hummer12007/brightnessctl) para controlar directamente el LED físico desde `/sys/class/leds`.

### Pasos

1. Instalar `brightnessctl`:

```bash
sudo pacman -S brightnessctl
