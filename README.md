# Hi, I'm Fikret Palas

I worked as engine room crew on merchant ships and as a CNC cutting operator in shipyards; now I develop the software that drives these machines. I hold an associate degree in Air Conditioning and Refrigeration from Uludağ University. I work with STM32CubeIDE and Arduino for firmware, along with Lazarus / Free Pascal, AutoCAD and Blender. I am open to job opportunities in embedded software, CNC / industrial automation and technical software.

---

### What I work with

| Area | Tools and skills |
|---|---|
| Embedded firmware | STM32 with STM32CubeIDE, Arduino / AVR (ATmega328P), timers and interrupts, step generation, serial protocols |
| Development tools | STM32CubeIDE, Lazarus IDE, AutoCAD, Blender, Arduino IDE |
| Desktop software | Lazarus / Free Pascal, Win32 API, multithreaded serial I/O, Mach3 plugins |
| CNC and motion control | Trajectory slicing, jog acceleration, limit / probe / E-Stop handling, position recovery |
| Design and 3D | AutoCAD, Blender (3D modelling and animation) |
| Education and background | Air Conditioning and Refrigeration Technician (2-year associate degree, Uludağ University Vocational School), ship engine department crew |

---

### Featured project: SafCNC

A complete USB motion controller for **Mach3**, built from scratch: an Arduino board generates the step
signals, a Mach3 plugin feeds it with motion data.

| Repository | What it is |
|---|---|
| [SafCNC_Arduino](https://github.com/fikretpalas/SafCNC_Arduino) | Firmware for Arduino Uno / Nano (C++) |
| [SafCNC_Mach3Plugin_en](https://github.com/fikretpalas/SafCNC_Mach3Plugin_en) | Mach3 plugin, English source (Free Pascal) |
| [SafCNC_Mach3Plugin_tr](https://github.com/fikretpalas/SafCNC_Mach3Plugin_tr) | Mach3 plugin, Turkish source (Free Pascal) |

Highlights:

- 3-axis DDA step generator in a 32 kHz timer interrupt, all axes pulsed together
- Own packet protocol: sequence counter, 16-bit checksum, 200 ms link watchdog
- One second of motion buffered on the card, streamed in 5 ms slices
- Separate reader and writer threads with overlapped I/O, so Mach3 never waits for USB
- Exact position recovery after any stop, from the slice and sub-tick reported by the card
- Safety first: limits, probe and E-Stop handled on the card, independently of the PC
- The card reports its own speed to the plugin: Arduino 32 kHz, STM32 hardware up to 100 kHz

---

### Education

- **Uludağ University** - Air Conditioning and Refrigeration (graduate)

### Experience

* Engine department crew on merchant ships
- **CNC cutting operator** in shipyards

---

### Türkçe
Ticari gemilerde makinacı, tersanelerde CNC kesim
operatörü olarak çalıştım; şimdi bu makineleri süren yazılımları geliştiriyorum. Uludağ Üniversitesi
İklimlendirme-Soğutma mezunuyum. STM32CubeIDE ve Arduino ile kart yazılımı, Lazarus / Free Pascal, AutoCAD
ve Blender ile çalışıyorum. Gömülü yazılım, CNC / endüstriyel otomasyon ve teknik yazılım alanlarında iş
fırsatlarına açığım.

---

**Contact:** safcnc@tutamail.com
