### Hi, I'm Omar.

I build local-first AI tooling that runs on your own machine, on your own
hardware, with no account and no cloud in the middle. Everything below is
written in Rust and works offline.

**[Last AI](https://github.com/TheSyrianDev/LastAI)** — the assistant. A desktop
app and a terminal client that talk to a small local core over localhost. Your
models, your memory, your spend, your files; a permission rule decides what an
agent may touch.

**LH** — the harness underneath it. The core, the clients, memory, tools,
provider layer, spend limits. Plain and unopinionated: give it a model and a
goal, it runs the turn loop. No downloader, no inference engine.

**[LastEngine](https://github.com/TheSyrianDev/LastEngine)** — the inference
engine. One backend trait, several implementations (CUDA, CPU, Vulkan, ROCm,
Metal), picked at startup by probing what the machine can actually do.

**[hf-dl](https://github.com/TheSyrianDev/hf-dl)** — the downloader. Fetching
models and datasets from the Hugging Face Hub with resumable, verified
transfers.

The four fit together as Last AI, but each stands on its own. The engine runs
without the app, the harness runs against any OpenAI-compatible server, and the
downloader is just a downloader.

---

Working in the open at [TheSyrianDev](https://github.com/TheSyrianDev).
Releases are on each project's page; the pre-release builds are honest about
being pre-release.
