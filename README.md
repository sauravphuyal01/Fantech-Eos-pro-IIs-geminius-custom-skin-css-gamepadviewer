# Fantech EOS Pro II S (Geminus Edition) — Custom GamepadViewer Skin

A custom, high-precision visual skin for GamepadViewer matching the Fantech EOS Pro II S (WGP15V2S) Geminus Edition wireless controller.

---

## Features

- Accurate Geminus Faceplate: Designed specifically around the Geminus colorway detailing with an integrated central Turbo button accent.
- Stationary Analog Wells: Radial gradient-shaded base wells under both thumbsticks prevent visual clipping and empty gaps during full deflection.
- Pseudo-3D Mechanical D-Pad: True 8-way directional press physics using CSS 3D perspective transforms (rotateX, rotateY) and contextual dynamic drop-shadows.
- Recessed Button Feedback: ABXY and menu buttons use localized brightness and contrast drop-shadows to simulate real mechanical switch depression without shifting coordinate positions.
- Pure CSS: Fully driven by hardware-accelerated CSS transforms and filters with zero external JavaScript dependencies.

---

## Repository Structure

- Components/
  - full.png: Main controller shell (with integrated Turbo accent)
  - disconnected.png: Disconnected state graphic
  - Stick.png: Thumbstick cap graphic
  - Dpad.png: D-Pad directional disc
  - select.png: Back / Select button graphic
  - start.png: Start button graphic
  - bumper.png: Pressed bumper graphic
  - bumper unpressed.png: Resting bumper graphic
- CREDITS.md: Detailed project credits and third-party asset licenses
- Fantech-Geminius.css: Primary stylesheet containing all mappings and styling
- README.md: Repository documentation

---

## CSS Architecture and Mapping

The skin maps directly over the standard GamepadViewer Xbox One template (.controller.custom).

Base Dimensions:
- Canvas: 582px x 460px
- Scale Factor: scale(1.30434) translate(-50%, -50%)
- Stylesheet URL: https://cdn.jsdelivr.net/gh/sauravphuyal01/Fantech-Eos-pro-IIs-geminius-custom-skin-css-gamepadviewer@832fa0a09551f4946c27950c3fb1a316a553b133/Fantech-Geminius.css

Element Mapping:
- Body Shell: .controller.custom (582px x 460px base container)
- Thumbstick Wells: .custom .sticks::before and ::after (Stationary radial-gradient dark recesses)
- Thumbsticks: .custom .stick.left and .right (112px x 112px circular caps)
- D-Pad Base: .custom .dpad::before (Stationary base disc)
- D-Pad Directionals: .custom .face.[dir].pressed (3D perspective tilts: perspective(220px))
- Action Buttons: .custom .button.[a,b,x,y] (SVG vector assets with zero-shift depression filters)
- Select Button: .custom .back (478px x 239px container, select.png)
- Start Button: .custom .start (70px x 35px scaled container, start.png)

---

## Credits and Acknowledgments

Author and Maintainer:
- Author: Saurav Phuyal (https://github.com/sauravphuyal01)
- Contribution: Custom CSS architecture, physical component alignment, Photoshop graphic integration (Geminus shell with integrated Turbo accent), pseudo-3D D-pad mechanics, and stationary stick well shaders.

Upstream Projects and Assets:
- Framework: GamepadViewer (https://gamepadviewer.com/) by Christopher Hebert — HTML5 Gamepad API visualization engine.
- Action Buttons (ABXY): Adapted from frolovlife/gamepadviewer-skins (https://github.com/frolovlife/gamepadviewer-skins) by frolovlife — high-DPI vector SVG button assets.

Disclaimer:
- Fantech and the Fantech EOS Pro II S (WGP15V2S) product designs are trademarks of Fantech. This skin is an independent community project created for live stream overlays and personal use; it is not affiliated with, endorsed by, or sponsored by Fantech.
