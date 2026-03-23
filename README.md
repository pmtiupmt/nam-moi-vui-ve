New Year Fireworks - From pmt with luv 🩵

A visually rich **HTML Canvas fireworks animation** with sound effects and a delayed New Year greeting message.

---

Overview

This project simulates a New Year fireworks display using **pure JavaScript and HTML5 Canvas**.
It includes background fireworks, layered explosion sounds, and a special animation where particles form a greeting text after a delay.

---

Features

* Random background fireworks (continuous loop)
* Layered explosion sound effects (no audio cut-off)
* Rocket animation with explosion trigger
* Text rendering using particle system: **"NĂM MỚI VUI VẺ"**
* Delayed message display (after 5 seconds)
* Start button to control animation
* Fully client-side (no libraries required)

---

## Technologies Used

* **HTML5 Canvas**
* **CSS3**
* **Vanilla JavaScript**
* **Audio API (HTMLAudioElement.cloneNode)**

---

## Project Structure

```
project-folder/
│── index.html      # Main file (contains everything)
│── boom.mp3        # Explosion sound effect
```

---

## How It Works

### Background Fireworks

* Random explosions are generated continuously
* Each explosion creates ~100 particles
* Timing is randomized (200ms → 1200ms)

---

### Sound System

* Uses:

```js
boomBase.cloneNode()
```

Allows multiple explosion sounds to play simultaneously (no overlap cut)

---

### Rocket + Text Effect

* After 5 seconds:

  * A rocket launches
  * Explodes into particles
  * Forms text using pixel mapping

---

### Text Rendering Logic

* Text is drawn to an offscreen canvas
* Pixel data is extracted
* Particles move toward text coordinates

---

## Customization

### Change text

In `prepareText()`:

```js
tctx.fillText("NĂM MỚI VUI VẺ", canvas.width/2, canvas.height/2);
```

---

### Change delay

```js
setTimeout(() => {
    showText = true;
}, 5000);
```

---

### Change sound

Replace:

```
boom.mp3
```

---

### Adjust firework density

```js
for(let i=0;i<100;i++)
```

---

## Notes

* Audio may not autoplay without user interaction (browser policy)
* Performance depends on device (many particles = heavier load)

---

## Preview

(Add screenshot or GIF here)

---

## Learning Highlights

This project demonstrates:

* Canvas animation loop (`requestAnimationFrame`)
* Particle systems
* Sound layering in JavaScript
* Rendering text from pixel data
* Event-driven animation control

---

## Contributing

Feel free to fork and improve:

* Add colors to text particles
* Add multiple rockets
* Add music background

---

## License

MIT License

---

## Credits

Made with ❤️ by **pmt**

---

## Happy New Year!
