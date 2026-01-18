# Temperature-Controlled Batch Reactor – Siemens S7-300

A complete, simulation-ready batch chemical reactor control system developed in **TIA Portal V18** for **CPU 315F-2 PN/DP**.

##  Process Sequence
1. **Fill** – Until high-level sensor activates  
2. **Heat** – PID-controlled (FB41) to 85°C  
3. **React** – Timed reaction (20s sim / 5 min real)  
4. **Drain** – Until low-level confirmed  
5. **Clean** – Water fill → 30s agitation → dirty drain  
6. **Auto-reset** – Ready for next batch

## Key Features
- **State-machine architecture** (no drum sequencer)
- **Abort-safe**: Stop button halts all phases instantly
- **FB41 "CONT_C" PID controller** in 1-second cyclic OB (OB32)
- **Realistic temperature simulation** with thermal lag (OB33)
- **No hardware required** — fully functional in **PLCSIM**

## Purpose
Built in **7 hours** as a self-directed learning project while transitioning from maintenance management to a **PLC programmer role**.

> All logic is in LAD. The temperature is simulated via software dynamics.
