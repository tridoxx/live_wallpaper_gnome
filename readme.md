# GNOME Video Wallpaper (Wayland, GNOME 49)

A personal project to create a **Wallpaper Engine-like experience** for GNOME on **Wayland**, currently tested on **GNOME 49**.

This project is a **GNOME Shell extension** that allows playing videos as desktop backgrounds using **Clutter, GTK, and GStreamer**. The goal is to provide a smooth, visually appealing solution for users running Wayland without monitor Hz limitations.

---

## Features

- Plays video files as the desktop background.
- Fully compatible with **Wayland** on GNOME 49.
- Uses **Clutter.Video** for rendering.
- Supports looping and autoplay of videos.
- Easy to install as a GNOME Shell extension.

---

## Installation

1. **Clone the repository** or download the ZIP:

```bash
git clone https://github.com/yourusername/gnome-video-wallpaper.git
```

2. **Copy the extension folder** to your GNOME Shell extensions directory:

```bash
mkdir -p ~/.local/share/gnome-shell/extensions/
cp -r gnome-video-wallpaper@julian ~/.local/share/gnome-shell/extensions/
```

3. **Place your video** in the `~/Videos/` folder with the filename `ElephantsDream.mp4` (or update the filename in `extension.js` accordingly).

---

## Enable the Extension

**Wayland Note:** You cannot reload GNOME Shell with `Alt+F2 → r`. You need to log out and log back in.

Then, enable the extension:

```bash
gnome-extensions enable gnome-video-wallpaper@julian
```

To disable:

```bash
gnome-extensions disable gnome-video-wallpaper@julian
```

---

## Development & Debugging

1. **Looking Glass**: Press `Alt+F2` → type `lg` → Enter.
   - Check logs, run JS commands, and reload extensions interactively:

```javascript
Main.extensionManager.reloadExtension("gnome-video-wallpaper@julian");
```

2. **Shell logs**: In a terminal:

```bash
journalctl /usr/bin/gnome-shell -f
```

3. Use `log("message")` inside `extension.js` for debug messages.

---

## Requirements

- **GNOME 49** on **Wayland**
- **GStreamer** installed with support for your video format (MP4/WebM)
- GNOME Shell extensions enabled
- Python (optional, if you want to automate video setup)

---

## Notes

- This is currently a work-in-progress. Documentation for dynamic wallpapers on Wayland is limited.
- Multi-monitor support is not implemented yet; only the primary monitor is used.
- Contributions, suggestions, or resources for working with **Clutter.Video**, **GStreamer**, or GNOME Shell extensions are highly appreciated.

---

## License

MIT License
