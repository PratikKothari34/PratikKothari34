<h1 align="center">Pratik V Kothari</h1>

<p align="center">
  2nd-year Mechatronics Engineering student.<br>
  I build <b>local-first, privacy-preserving tools</b> — software that runs on your machine and keeps your data there.
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/pratik-v-kothari-881816377"><img alt="LinkedIn" src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white"></a>
</p>

---

### About

I follow whatever problem has my attention. Some months that means an LLM pipeline, other months it means wiring an H-bridge and cutting a frame. I picked Mechatronics because it never asks me to choose.

The thread running through all of it: **things should work without the cloud.** I build offline-first — local inference, on-device storage, no API keys and no telemetry. Where a project talks to the network at all, it is opt-in and disclosed in that project's README. That is a design constraint I set on purpose, not a limitation I settled for.

- 🔧 Comfortable on both sides of the hardware/software line
- 🌱 Currently going deeper on RAG and retrieval systems
- 💬 Ask me about local LLMs, Electron, or motor control

---

### Featured

**[TaxDraft India](https://github.com/PratikKothari34/Indian_Income_Tax_Legal_Replying_Agent)** · `Python` `TypeScript` · GPL-3.0

Drafts formal replies to Income Tax Department notices, for professionals who cannot put client data through a cloud API. A local LLM works over a RAG index of the IT Act 2025, key sections of the 1961 Act, the Finance Acts, IT Rules 1962, and CBDT circulars — re-synced from Indian Kanoon daily at noon. Reads PDFs, DOCX, and scanned images via OCR, parses computation sheets and TDS reconciliations from Excel, and emits a formatted `.docx`. Runs `qwen2.5:14b` by default and escalates to `deepseek-r1:14b` for reassessment, search and seizure, penalty, transfer pricing, and DTAA matters.

One ~18 GB download, then drafting runs entirely on the machine — notices, uploads and replies never leave it. The only outbound traffic is the public legal-text sync, and it can be turned off.

<sub>Electron 37 · React 19 · Vite 7 · Fluent UI v9 · FastAPI · Ollama · ChromaDB · sentence-transformers · Tesseract OCR</sub>

<br>

**[Vessel](https://github.com/PratikKothari34/Vessel)** · `JavaScript` · GPL-3.0

Conversations that stay coherent long past the model's context window, running entirely on local hardware. Memory is the whole problem, and Vessel tiers it: a 32K live window holds recent turns verbatim, `gemma3:4b` folds older ones into a rolling summary, and anything archived is embedded with `nomic-embed-text` at 768 dimensions and pulled back by cosine ranking when it becomes relevant again. A second, smaller model handling compression keeps the chat model free to do nothing but write.

Regenerating a reply keeps every variant — you swipe between them, and whichever you pick becomes the canonical one for memory. A director channel takes out-of-character steering that guides the response but is never written into the story or the memory index.

Local-only by default, and the database is encrypted at rest with a key held in the OS keychain. Optional cloud sync runs on your own Turso credentials — and because the sync engine can't encrypt the local file, turning it on trades local encryption for a cloud mirror. If the encrypted database can't be opened with the key on hand, the backend refuses to start rather than quietly reopening your data in plaintext.

<sub>Electron · React · Vite · Node · Express · SQLite/Turso · Ollama · llama-3.1 8b · gemma3:4b · nomic-embed-text</sub>

<br>

**[Lead Screw Position Tracker](https://github.com/PratikKothari34/lead-screw-position-tracker)** · `Python` · MIT

Positions a carriage anywhere along 295 mm of T8 lead screw — a ~30 RPM geared motor turning ~9.4 mm of travel per revolution, so ~4.7 mm/s at full speed. Homes against a limit switch, backs off 10 mm to clear it, then runs calibrated traversals from that reference. Python host talks to an NI cDAQ chassis over `nidaqmx`, with software-timed PWM on a background thread and 50 ms switch polling so a runaway carriage stops before it hits anything.

Includes wiring diagrams, SolidWorks sources and STLs for the 3D-printed bearing blocks and couplers, and the calibration data.

<sub>Python · NI cDAQ · nidaqmx · L298N H-bridge · SolidWorks</sub>

---

### Also building

<table>
<tr>
<td width="50%" valign="top">

**[Residual](https://github.com/PratikKothari34/Residual)** · `TypeScript` · GPL-3.0 · <sub>pre-beta</sub>

Budgeting that reads your bank statements instead of asking you to type them in. Imports CSV, Excel and PDF — including password-protected and column-shifted layouts — and categorizes against Indian merchant and UPI narration patterns, learning from corrections. Chat gets read-only tools: it proposes recategorizations, you approve them row by row.

<sub>Electron 39 · React 18 · Flutter · SQLite/libSQL · Drizzle · Ollama `gemma3:4b` · libsodium</sub>

</td>
<td width="50%" valign="top">

<br>

<sub>More in the [repository list](https://github.com/PratikKothari34?tab=repositories).</sub>

</td>
</tr>
</table>

---

### Tools

<p>
  <img alt="Python" src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white">
  <img alt="TypeScript" src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white">
  <img alt="JavaScript" src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black">
  <img alt="React" src="https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black">
  <img alt="Electron" src="https://img.shields.io/badge/Electron-47848F?style=flat-square&logo=electron&logoColor=white">
  <img alt="Node.js" src="https://img.shields.io/badge/Node.js-5FA04E?style=flat-square&logo=nodedotjs&logoColor=white">
  <img alt="FastAPI" src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white">
  <img alt="Vite" src="https://img.shields.io/badge/Vite-646CFF?style=flat-square&logo=vite&logoColor=white">
  <img alt="SQLite" src="https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white">
  <img alt="Ollama" src="https://img.shields.io/badge/Ollama-000000?style=flat-square&logo=ollama&logoColor=white">
  <img alt="ChromaDB" src="https://img.shields.io/badge/ChromaDB-FFCA28?style=flat-square&logo=databricks&logoColor=black">
  <img alt="Git" src="https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white">
  <img alt="SolidWorks" src="https://img.shields.io/badge/SolidWorks-E31E24?style=flat-square&logo=dassaultsystemes&logoColor=white">
</p>

---

<p align="center">
  <b>Open to internships and collaborations.</b><br>
  <sub>Best reached on <a href="https://www.linkedin.com/in/pratik-v-kothari-881816377">LinkedIn</a>.</sub>
</p>
