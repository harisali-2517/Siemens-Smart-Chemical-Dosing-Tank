# Smart-Chemical-Dosing-Tank

A sequential batch processing and adaptive flow-control system programmed on a **Siemens S7-1200 (CPU 1215C)** using **TIA Portal**. 

### 🧪 Project Highlights
* **Sequential State Machine:** Programmed a 3-liquid batching sequence (Fill A/B/C ➔ Mix ➔ Drain) integrated with `CTU` batch counters and continuous automatic cycle resets.
* **Adaptive Flow Correction:** Implemented dynamic math to calculate real-time flow rates (`Flow Rate = Δ Level / Δ Time`). The logic automatically adjusts timer presets on the fly to compensate for simulated pump wear and valve clogging.
* **Safety Interlocks:** Engineered high-priority fault logic using comparators and `MOV` instructions to immediately freeze cycle states, isolate all active pumps, and trigger visual alarms upon detecting high-level fault conditions.

### 📂 Repository Files
* **Chemical_Dosing_Logic.pdf:** PDF export of the Main OB1 ladder logic and sequential function blocks.
* **Network_Screenshots:** Visual captures of the adaptive flow rate arithmetic and safety interlock networks.
* **Chemical_Dosing_System.zap15:** Raw TIA Portal V15 archive file.
