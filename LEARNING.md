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
| Phase | Name | Status | Est. hours |
|-------|------|--------|------------|
| 0 | Setup & Tooling | Do | 14 |
| 1 | Math Foundations | Review | 23 |
| 2 | ML Fundamentals | Skip | -- |
| 3 | Deep Learning Core | Review | 15 |
| 4 | Computer Vision | Skip | -- |
| 5 | NLP Foundations to Advanced | Review | 30 |
| 6 | Speech & Audio | Skip | -- |
| 7 | Transformers Deep Dive | Do | 14 |
| 8 | Generative AI | Do | 14 |
| 9 | Reinforcement Learning | Do | 13 |
| 10 | LLMs from Scratch | Do | 26 |
| 11 | LLM Engineering | Do | 17 |
| 12 | Multimodal AI | Do | 65 |
| 13 | Tools & Protocols | Do | 24.5 |
| 14 | Agent Engineering | Do | 42 |
| 15 | Autonomous Systems | Do | 20 |
| 16 | Multi-Agent & Swarms | Do | 28 |
| 17 | Infrastructure & Production | Do | 32 |
| 18 | Ethics, Safety & Alignment | Do | 31 |
| 19 | Capstone Projects | Do | 620 |

Összesen (Review + Do, Capstone nélkül): ~408.5 óra → ~5 óra/hét mellett kb. 82 hét (~1.5 év).
Capstone-nal (Phase 19) együtt: ~1028.5 óra → kb. 206 hét (~4 év) ~5 óra/hét mellett.

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
