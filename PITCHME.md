---
marp: true
theme: default
paginate: true
---

# Day 2

## CS Hardware - Transistors

---

# Goal For Today

By the end of today you will:

- Understand what a transistor does
- Learn the three transistor pins (Base, Collector, Emitter)
- Build transistor-controlled LED circuits and logic gates
- Understand how transistors are the foundation of computing

![bg contain right](assets/transistor-closeup.jpeg)

---

# Review From Day 1

Yesterday we learned:

- Voltage pushes current
- Resistance limits current
- LEDs have polarity
- Ohm's Law: **V = I × R**
- Multimeters help us debug circuits

---

# Today

Today we add a new idea: **CONTROL**

A small electrical signal can control a larger one.

---

# Today's Workflow

1. Learn what transistors do
2. Build a transistor-controlled LED circuit
3. Explore amplification and switching
4. Build logic gates using transistors
5. Connect logic gates to computer hardware concepts

---

<!-- Bell at the opening of the long-distance line from New York to Chicago in 1892 -->
![bg contain](assets/alexander-graham-bell-phone-call.jpg)

---

# Problem

In the early 1900s, telephone systems had a huge challenge: *Weak signals*

As voices traveled long distances through wires:

- signals became weaker
- noise increased
- calls became unreliable



<!-- 
---

# Need

Telephone providers needed a way to:

- amplify signals
- switch calls electronically
- do it reliably at massive scale 

-->

---

Existing technology like tubes and relays were:

- large
- fragile
- expensive
- generated heat
- consumed lots of power
- failed often

This limited communication systems.

![bg contain right](assets/vaccuum-tube.jpeg)

---

![bg contain](assets/eniac.jpg)

<!-- 

ENIAC

One of the first large electronic computers.

It used:

~18,000 vacuum tubes
huge amounts of power
massive cooling
constant maintenance

Key teaching point:

Transistors replaced thousands of fragile glowing tubes.

-->

---

![bg contain](assets/eniac-tubes.webp)

---

# Transistor to the Rescue

![bg contain right](assets/eniac-on-chip.jpg)

---

# What Is a Transistor?

<!-- Kind of like a valve / faucet -->

A transistor is an electronically controlled switch.

It can:

- Turn current ON or OFF
- Control larger current using smaller current
- Amplify signals
- Build logic circuits

![bg contain right](assets/transistor-diagram.jpeg)

---

# Real-World Examples

Modern computers contain **billions** of transistors.

Transistors are everywhere:

- CPUs
- GPUs
- RAM
- Phones
- Amplifiers
- Sensors
- and more...

![bg contain right](assets/cpu-closeup.jpeg)

---

# Water Analogy

Think of a transistor like a valve.

- Small movement of the valve handle
- Controls larger water flow In electronics:
  - Small current at the base
  - Controls larger current through the transistor
  
![bg contain right](assets/water-valve-analogy.jpeg)

---

# NPN Transistor

There are different types of transistors.

Today we will use an NPN transistor.

Three pins:

- Base (B)
- Collector (C)
- Emitter (E)

<!-- The base controls current flow. -->

![bg contain right](assets/water-valve-analogy.jpeg)

<!--
---

# Transistor As A Switch

A tiny current into the base allows a larger current to flow.
This is called: **Switching**
Small input → large output

 ![bg contain right](assets/transistor-switch-diagram.png)
 
-->

---

# Demo: Transistor Emitter Follower

Today's demo modifies yesterday's LED brightness circuit.

## Yesterday

- resistor controlled current manually

## Today

- transistor helps control larger current

<!-- ![bg contain right](assets/transistor-led-circuit.png) -->

<!--

INSTRUCTOR NOTES:

Show:
- transistor pinout
- LED brightness changing
- small current controlling larger current

Questions:
- Why not connect LED directly?
- What happens if base is disconnected?
- What changes brightness now? 

-->

---

# What Is Happening?

The transistor acts like a gate.

- Base current opens the gate
- Collector-emitter current powers the LED

Important idea: **Small signal controls large signal**

This idea powers all digital electronics.

<!--
---

# Transistor Current Flow

- A transistor allows current to flow from collector to Emitter ONLY when enough current enters the base

 ![bg contain right](assets/transistor-current-flow.png)
 
-->

<!-- 

# Why Is This Important?

Transistors solve a major problem: **Small circuits often cannot directly power larger devices**

Examples:

- Microcontrollers controlling motors
- CPUs controlling memory
- Sensors controlling alarms
- Tiny signals driving speakers

---

-->

---

# Troubleshooting

If your circuit does NOT work:

- check transistor orientation
- verify pinout
- check LED polarity
- verify resistor placement
- test power rails
- test continuity

Remember: **Debugging is expected**

---

# Lab Breakout #1

## Transistor LED Control

Goal: Build a transistor-controlled LED circuit.

Try:

- changing base resistance
- changing LED resistance
- disconnecting the base
- measuring voltage/current

<!-- ![bg contain right](assets/transistor-led-breadboard.jpg) -->

---
<!--

# Reflection Questions:

- What controlled the LED brightness?
- What role did the transistor play?
- Why is amplification useful?
- What changed compared to Day 1?

---

-->

# Computers Use Binary

Computers use only two states:

| State | Meaning |
| --- | --- |
| 0 | OFF |
| 1 | ON |

This is called **binary**

Transistors can switch between ON and OFF extremely quickly.

<!-- ![bg contain right](assets/binary-ones-zeroes.jpg) -->

---

# Logic Gates

Logic gates are built from transistors. They make decisions using binary signals.

Examples:

- NOT
- AND
- OR
- NAND

Logic gates are the building blocks of CPUs.

<!-- ![bg contain right](assets/logic-gates.png) -->

---

# Demo: Transistor Logic Gates

We will build:

- Buffer gate
- NOT gate
- AND gate
- OR gate
- NAND gate

<!-- 

Using:

- transistors
- buttons / switches
- LEDs
- resistors
- wire

-->

<!-- ![bg contain right](assets/transistor-logic-demo.jpg) -->

<!--

INSTRUCTOR NOTES:

Connect buttons as logical inputs
Questions:

- Which button combinations light the LED?
- Why is NAND important?
- How could many gates combine into a computer? 

-->

---

# Boolean Logic

Boolean logic uses TRUE/FALSE values.

| Electrical | Boolean |
| --- | --- |
| ON | TRUE |
| OFF | FALSE |

<!-- 
- Buttons/Switches are inputs
- LEDs are logical outputs
-->

---

# Buffer Gate

A Buffer gate just matches the input.

| Input | Output |
| --- | --- |
| 1 | 1 |
| 0 | 0 |

![bg contain right](assets/transistor-switch.png)

[Example](https://www.101computing.net/creating-logic-gates-using-transistors/)

---

# NOT Gate

A NOT gate reverses the input.

| Input | Output |
| --- | --- |
| 0 | 1 |
| 1 | 0 |

![bg contain right](assets/transistor-NOT-Gate.png)

---

# AND Gate

AND only outputs ON if BOTH inputs are ON.

| A | B | Output |
| --- | --- | --- |
| 0 | 0 | 0 |
| 0 | 1 | 0 |
| 1 | 0 | 0 |
| 1 | 1 | 1 |

![bg contain right](assets/transistor-AND-Gate.png)

---

# OR Gate

OR outputs ON if EITHER input is ON.

| A | B | Output |
| --- | --- | --- |
| 0 | 0 | 0 |
| 0 | 1 | 1 |
| 1 | 0 | 1 |
| 1 | 1 | 1 |

![bg contain right](assets/transistor-OR-Gate.png)

---

# NAND Gate

NAND outputs ON only if both inputs are not on at the same time.

<!-- NAND is one of the most important gates in computing. Modern CPUs are built largely from NAND gates. -->

| A | B | Output |
| --- | --- | --- |
| 0 | 0 | 1 |
| 0 | 1 | 1 |
| 1 | 0 | 1 |
| 1 | 1 | 0 |

![bg contain right](assets/transistor-NAND-Gate.png)

---

# Integrated Circuit (IC)

<!-- An integrated circuit (IC) is a set of electronic circuits on one small flat piece of semiconductor material (or "chip") -->

<!-- A modern processor contains billions of tiny transistor switches. -->

![bg contain right](assets/logic-gates-AND-chip.png)

---

# Lab Breakout #2

## Transistor Logic Gates

Goal: Build logic gates using transistors.

Try:

- Buffer gate
- NOT gate
- AND gate
- OR gate
- NAND gate

<!-- Use buttons or touch sensors as inputs. Use LEDs as outputs. -->

---

<!--

# Reflection

- Which gate was easiest?
- Which gate was hardest?
- Why are NAND gates so important?
- How do logic gates relate to CPUs?

---

-->

# Key Takeaways

<!-- 

- Transistors are electronically controlled switches
- Small current can control larger current
- Transistors can amplify and switch
- Logic gates are built from transistors
- CPUs are made from billions of transistor switches
- Modern computing depends on binary logic

-->


<!-- https://www.101computing.net/creating-logic-gates-using-transistors/ -->