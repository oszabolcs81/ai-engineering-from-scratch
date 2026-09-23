# My AI Engineering Path
<!-- Managed by the ai-engineering-from-scratch learning skills.
     Repo: https://github.com/rohitg00/ai-engineering-from-scratch -->

## Mission
Elsődleges cél: mélyebben megérteni, hogyan működik az AI (nem csak API-hívás
szinten), majd erre építve saját AI-terméket/agentet építeni. A tanulás a
meglévő 20+ éves IT tapasztalat kibővítése, nem karrierváltás.

## Placement
- Date: 2026-09-22
- Score: 6/10 — Matek & statisztika: 1/2, Klasszikus ML: 2/2, Deep Learning: 0/2, NLP & Transformerek: 1/2, Alkalmazott AI: 2/2
- Entry point: Phase 7: Transformers Deep Dive (nyers pontszám alapján), de a Deep Learning terület 0/2 miatt Phase 3 is Review-ra emelve — a valódi belépési sorrend Phase 0-tól indul, majd Phase 1/3/5 Review, aztán lineárisan Phase 7-18, végül Phase 19 Capstone
- Pace: ~5 óra/hét

## Hardware profile
- Gép: ThinkPad P53 — Intel i7-9750H, 32 GB RAM, Quadro T1000 4 GB VRAM, Windows 11 + WSL2 (Ubuntu)
- [BECSLÉS ±20%] Édes pont lokális LLM inferenciára: 8-12B paraméter, Q4 kvantálás
- [BECSLÉS ±20%] 4 GB VRAM → teljes GPU-tréning nem reális; CPU-mód + részleges GPU offload várható — token/sec méréssel megerősítendő
- Következmény: Phase 1-3 helyben (CPU/GPU) elvégezhető; Phase 4+ nagyobb tréningnél Google Colab (ingyenes T4, 16 GB VRAM) ajánlott VRAM-korlát miatt, nem elvi okból

## Path
| Phase | Name | Status | Est. hours (official) | Est. hours (personal) |
|-------|------|--------|------------------------|------------------------|
| 0 | Setup & Tooling | Do | 14 | **2.7** (mért, l. lent) |
| 1 | Math Foundations | Review | 23 | 17.7 |
| 2 | ML Fundamentals | Skip | -- | -- |
| 3 | Deep Learning Core | Review | 15 | 11.5 |
| 4 | Computer Vision | Skip | -- | -- |
| 5 | NLP Foundations to Advanced | Review | 30 | 23.1 |
| 6 | Speech & Audio | Skip | -- | -- |
| 7 | Transformers Deep Dive | Do | 14 | 10.8 |
| 8 | Generative AI | Do | 14 | 10.8 |
| 9 | Reinforcement Learning | Do | 13 | 10.0 |
| 10 | LLMs from Scratch | Do | 26 | 20.0 |
| 11 | LLM Engineering | Do | 17 | 13.1 |
| 12 | Multimodal AI | Do | 65 | 50.0 |
| 13 | Tools & Protocols | Do | 24.5 | 18.8 |
| 14 | Agent Engineering | Do | 42 | 32.3 |
| 15 | Autonomous Systems | Do | 20 | 15.4 |
| 16 | Multi-Agent & Swarms | Do | 28 | 21.5 |
| 17 | Infrastructure & Production | Do | 32 | 24.6 |
| 18 | Ethics, Safety & Alignment | Do | 31 | 23.8 |
| 19 | Capstone Projects | Do | 620 | 476.9 |

### Személyes kalibráció (miért tér el az official-tól)
20+ éves IT-háttér miatt két eltérő szorzót alkalmazunk:
- **Fázis 0 (eszköz-fókuszú, ~5x gyorsulás):** a lecke-tartalom nagy része
  (Git, terminál, Linux, Python env, editor) már ismert eszközhasználat, nem
  új fogalom. Lecke-szintű méréssel igazolva: 01 és 02 ténylegesen ~10-15
  perc volt a hivatalos 45-75 perc helyett (a hibakeresési idő — WSL
  fájlrendszer, GitHub PAT — kivéve, mert egyszeri akadály, nem a lecke
  tartalma). A 2.7 óra ebből a lecke-szintű újrabecslésből jön, nem egyetlen
  szorzóból.
- **Review/Do fázisok, Fázis 1-19 (tartalom-fókuszú, ~1.3x gyorsulás):** itt
  valódi új anyag van (matek, DL, transformerek, agentek), ahol a
  Placement-eredmény (0-1/2 pontok Math/DL/NLP-ben) valós hiányt jelez — ott
  nem várható az 5x-ös gyorsulás, csak annyi, amennyit a gyors
  kódolvasás/eszközhasználat ad.
- **Módszer:** ez becslés, nem mérés — minden lecke után frissítjük a
  Progress logot a tényleges idővel, és ha a mintázat eltér, itt
  újrakalibráljuk a szorzót fázisonként.

Összesen (Review + Do, Capstone nélkül) — official: ~408.5 óra, személyes becslés: ~306 óra → ~5 óra/hét mellett kb. 61 hét (~1.2 év).
Capstone-nal (Phase 19) együtt — official: ~1028.5 óra, személyes becslés: ~783 óra → kb. 157 hét (~3 év) ~5 óra/hét mellett.

## Progress log
| Date | Lesson | Quiz | Note |
|------|--------|------|------|
| 2026-09-22 | Placement quiz | 6/10 | find-your-level kvíz, terület-bontás fent |
| 2026-09-23 | Phase 0 / 01 Dev Environment | -- | verify.py PASS (Python 3.12.14, Git 2.43.0); repo áthelyezve /mnt/c-ről ~/projects-be (WSL hardlink hiba miatt) |
| 2026-09-23 | Phase 0 / 02 Git & Collaboration | -- | saját `my-progress` branch a fork-on (oszabolcs81/ai-engineering-from-scratch), fine-grained PAT beállítva (Contents + Workflows: Read and write), .gitignore commit pusholva |

## Review queue
- Phase 1: valószínűségszámítás / Bayes-tétel (dobás-valószínűség kérdés hibázva)
- Phase 3: backpropagation / chain rule, ResNet skip connection célja (mindkettő hibázva)
- Phase 5: attention mechanizmus Q/K/V fogalma (hibázva)

## Fogalomtár
<!-- Élő szakasz: minden lecke után bővítjük az újonnan előkerült fogalmakkal. -->

| Fogalom | Mire való, dióhéjban |
|---|---|
| **uv** | Gyors Python csomag- és verziókezelő (pip+venv helyett). Telepíti a Python-t, kezeli a virtuális környezetet és a csomagokat. |
| **venv / virtuális környezet** | Elszigetelt Python "buborék" projektenként, hogy a csomagverziók ne ütközzenek más projektekkel. |
| **PATH** | A rendszer listája, hogy a terminál hol keressen futtatható programokat. Ha egy frissen telepített program nincs a PATH-ban, a shell "command not found"-ot ír, pedig a program megvan. |
| **WSL2** | "Windows Subsystem for Linux" — valódi Linux-kernelt futtat Windows alatt, hogy Linux-parancsokat/eszközöket natívan használhass. |
| **/mnt/c vs. Linux natív fs (`~`)** | A `/mnt/c/...` a Windows-lemez WSL-en belüli elérése — ott a Linux-jogosultságkezelés (hardlink, symlink) nem működik jól. A `~/...` valódi Linux ext4 fájlrendszer, ahol minden simán megy. Ezért költöztünk oda. |
| **Git — add / commit / push** | `add`: kijelölöd, mi kerüljön a mentésbe. `commit`: elmented egy pillanatképet lokálisan, üzenettel. `push`: felküldöd a mentést a GitHub-ra (távoli szerver). |
| **Branch** | Párhuzamos munkaág a kódban, hogy a saját változtatásaid ne keveredjenek a fő (`main`) ággal. Nálunk ez a `my-progress`. |
| **Fork** | GitHub-on egy másik felhasználó repójának saját másolata a te fiókodban, amire már van írási jogod (az eredetihez nincs). |
| **PAT (Personal Access Token)** | Jelszó helyett használt, jogosultságokra szabható belépési kulcs a GitHub API-hoz/git push-hoz. "Fine-grained" típusnál pontosan meg kell adni, mihez (Contents, Workflows stb.) és milyen szinten (read/write) férhet hozzá. |
| **nvidia-smi** | Parancssoros eszköz, ami megmutatja az NVIDIA GPU állapotát: driver-verzió, CUDA-verzió, VRAM-használat, hőmérséklet, futó folyamatok. |
| **CUDA** | NVIDIA platformja, ami lehetővé teszi, hogy programok (pl. PyTorch) a GPU-n futtassák a számításokat, nem csak a CPU-n. |
| **VRAM** | A GPU saját, gyors memóriája (nálad 4 GB) — korlátozza, mekkora modell fér el rajta egyszerre. Elkülönül a rendszer RAM-tól (nálad 32 GB). |
| **fp16 / kvantálás (pl. Q4)** | A modell számainak tárolási pontossága. fp16 = 16 bites lebegőpontos (fele akkora hely, mint a szokásos 32 bit). Q4 = 4 bites kvantálás, még kisebb méret, kis pontosságvesztéssel — ezért fér el egy 8-12B-s modell is kis VRAM-ban. |
| **Google Colab** | Ingyenes, böngészőből elérhető Jupyter-környezet Google-től, GPU-hozzáféréssel (T4, 16 GB VRAM) — ha a saját géped VRAM-ja nem elég egy feladathoz. |
