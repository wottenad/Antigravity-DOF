# DOF Builder | Multi-Layer Edition - User Guide

## What is this tool?

The **DOF Builder** is a specialized web-based utility designed for configuring lighting effects for **Direct Output Framework (DOF)**, which is commonly used in Virtual Pinball cabinets to control addressable LEDs (like Teensy/Wemos strips) and other toys.

This specific "Multi-Layer Edition" allows users to visually design complex, layered lighting animations without manually writing cryptic configuration strings. It simulates how different effects (like strobes, pulses, or solid colors) look when stacked on top of each other.

## Key Features

- **Multi-Layer Mixing**: Design up to 4 simultaneous layers of effects. For example, you can have a steady Blue background (Layer 1) with Red sparkles flickering on top (Layer 2).
- **Real-Time Simulation**: A visual "LED Strip" preview shows exactly how your combined effects will look in real-time.
- **Advanced Effect Controls**:
  - **Effect Types**: Static, Blink, Pulse, and Flicker/Strobe.
  - **Colors**: Select from a massive palette of named DOF colors (e.g., `Red`, `IceBlue`, `Gold`).
  - **Sequencing**: Use "Start Delay" and "Duration" to create timed sequences (e.g., Flash Red for 500ms, then wait and Flash Green).
  - **Density (Sparkles)**: Create "sparkle" or "noise" effects by reducing density (e.g., only lighting up 10% of LEDs at random).
  - **Positioning**: Map effects to specific parts of a strip (e.g., only the bottom 50%).
- **Section Management**: Pre-loaded with common Virtual Pinball cabinet sections (e.g., `PF Left Effects MX`, `Undercab Complex`, `Flipper Buttons`).
- **Export Workflow**: "Stage" your designs for different sections and generate a final CSV code snippet ready for your `directoutputconfig.ini` or similar configuration files.
- **Auto-Save**: Work is automatically saved to your browser's local storage so you don't lose progress if you refresh.

## Why might someone use it?

1. **Simplifying Complex Configs**: Writing raw DOF config strings manually (e.g., `Red Blink 500 / Blue On`) is error-prone and hard to visualize. This tool provides a GUI to generate them.
2. **Visualizing "Additive" Mixing**: One of the hardest things to predict in LED programming is how colors mix (e.g., Red + Blue = Magenta). This tool simulates that physics, showing users why "White sparkles on a White background" won't be visible.
3. **Designing Custom Toy Effects**: Users can create unique light shows for specific game events (switches, solenoids, or "E Codes") without knowing the underlying syntax.
4. **Rapid Prototyping**: You can quickly test ideas like "What if the undercab light pulses purple while the flipper buttons flash yellow?" without needing to load a table in Visual Pinball.

## How to Use

1. **Select a Target Section**: Choose which part of your cabinet you are designing for (e.g., "Right Magnasave").
2. **Configure Layers**:
   - Pick a **Color**.
   - Choose an **Effect** (e.g., Flicker).
   - Adjust **Duration** and **Delay**.
3. **Preview**: Watch the LED strip simulation at the bottom.
4. **Apply**: Click "Apply Layers to Section" to save that design to the staging area.
5. **Export**: Once all sections are designed, click "Generate Final CSV" to get the code string.
