# Let's start 
# Everything You Need to Know About Blink

**Blink** can refer to several prominent concepts depending on the domain: the **open-source browser rendering engine** developed by Google, Malcolm Gladwell's famous **book on rapid decision-making**, or **Blink Home Security** owned by Amazon. 

Below is an overview of each major topic.

---

## 1. Blink (Web Browser Engine)

**Blink** is an open-source browser layout engine developed primarily by **Google** as part of the Chromium project. It powers Google Chrome, Microsoft Edge, Opera, Brave, Vivaldi, and many other web browsers.

### Key Features
* **Multi-Process Architecture:** Separates browser tabs and components into distinct processes to improve security and stability.
* **High Performance:** Designed for rapid rendering, smooth animations, and optimized JavaScript execution via integration with the V8 engine.
* **Modern Web Standards:** Implements cutting-edge HTML5, CSS3, WebGL, and JavaScript APIs rapidly to maintain web compliance.

### History & Evolution
* **Forked from WebKit:** Google announced Blink in April 2013, forking it from WebKit (which itself originated from KHTML).
* **Reason for Creation:** To simplify the codebase and allow Chromium to innovate faster without compatibility constraints shared with Apple's WebKit.

---

## 2. *Blink: The Power of Thinking Without Thinking* (Book)

Written by **Malcolm Gladwell** and published in 2005, *Blink* explores the science of split-second decision-making and intuitive judgment.

### Core Concepts
* **Thin-Slicing:** The ability of our minds to find patterns in situations based only on narrow "slices" of experience or data.
* **Adaptive Unconscious:** The mental process where the brain processes information quickly and quietly without conscious awareness.
* **Strengths & Flaws of Intuition:** While rapid intuition can lead to expert decisions, it can also be skewed by unconscious bias, prejudice, or stress.

---

## 3. Blink Home Security (Amazon)

**Blink** is also a popular brand of smart home security cameras and video doorbells acquired by Amazon in 2017.

### Features
* **Long Battery Life:** Powered by lithium AA batteries, often lasting up to two years on a single set.
* **Cloud & Local Storage:** Offers options for storing motion detection clips on the cloud or locally via a Sync Module.
* **Smart Home Integration:** Deeply integrated with Amazon Alexa for voice commands, live viewing, and automated routines.

---

## Summary Comparison

| Concept            | Domain                | Key Takeaway                                               |     |
| :----------------- | :-------------------- | :--------------------------------------------------------- | --- |
| **Blink Engine**   | Web Technology        | Powers most modern Chromium-based web browsers.            |     |
| **Blink (Book)**   | Psychology & Business | Explores rapid intuitive judgment and "thin-slicing".      |     |
| **Blink Security** | Consumer Electronics  | Battery-powered smart cameras and home security solutions. |     |

# ບົດການທົດລອງ: ການຕໍ່ວົງຈອນ ແລະ ເປີດ-ປິດ ຫລອດໄຟ LED ດ້ວຍ Arduino Uno

  

## 1. ອຸປະກອນທີ່ຕ້ອງກະກຽມ (Equipment List)

- **Arduino Uno** 1 ເຄື່ອງ

- **Breadboard** (ໂຟໂຕະບອດ) 1 ອັນ

- **ຫລອດໄຟ LED** 1 ດອກ

- **ຕົວຕ້ານທານ (Resistor)** 220Ω 1 ໂຕ

- **ສາຍສຽບ (Jumper Wires)**

  

---

  

## 2. ຂັ້ນຕອນການຕໍ່ວົງຈອນ (Circuit Connection)

1. ນຳຫລອດໄຟ **LED** ແລະ **ຕົວຕ້ານທານ (Resistor 220Ω)** ໄປສຽບລົງໃສ່ **Breadboard**.

2. ສຽບຕົວຕ້ານທານ (Resistor) ເຂົ້າກັບ **ຂາບວກ (Anode - ຂາຍາວ)** ຂອງຫລອດໄຟ LED.

3. ຕໍ່ສາຍ Jumper ຈາກປາຍອີກດ້ານໜຶ່ງຂອງຕົວຕ້ານທານ ເຂົ້າໄປຫາ **Pin 13** ຂອງບອດ Arduino Uno.

4. ຕໍ່ສາຍ Jumper ຈາກ **ຂາລົບ (Cathode - ຂາສັ້ນ)** ຂອງຫລອດໄຟ LED ເຂົ້າໄປຫາຂາ **GND** ຂອງບອດ Arduino Uno.

  

---

  

## 3. ໂຄດຄຳສັ່ງ (Arduino Source Code)

  

```cpp

void setup() {

  // put your setup code here, to run once:

  pinMode(13, OUTPUT);

  

}

  

void loop() {

  // put your main code here, to run repeatedly:

  

  digitalWrite(13, HIGH);

  delay(100);

  

  digitalWrite(13, LOW);

  delay(100);

  

}

```

  

---

  

## 4. ອະທິບາຍການເຮັດວຽກຂອງ Code

* `pinMode(ledPin, OUTPUT);` : ເປັນການຕັ້ງຄ່າໃຫ້ Pin 13 ສາມາດສົ່ງສັນຍານໄຟຟ້າອອກມາໄດ້.

* `digitalWrite(ledPin, HIGH);` : ສັ່ງໃຫ້ Pin 13 ຈ່າຍໄຟຟ້າ (5V) ເຮັດໃຫ້ LED ລຸງ/ແຈ້ງ.

* `digitalWrite(ledPin, LOW);` : ສັ່ງໃຫ້ Pin 13 ຍຸດຈ່າຍໄຟຟ້າ (0V) ເຮັດໃຫ້ LED ມອດ.

* `delay(1000);` : ຄຳສັ່ງໜ່ວງເວລາ 1,000 ມິນລິວິນາທີ (ເທົ່າກັບ 1 ວິນາທີ).