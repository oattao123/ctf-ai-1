# TOYOTA CTF — AI Edition 🤖🚩

AI-centric CTF — each challenge's core is a real AI/LLM concept mixed with another
field. Flag format: `TOYOTACTF{...}` · every challenge is worth **100 points**.

| # | Title | AI core | Mixed with |
|---|-------|---------|------------|
| 1 | Byte-Level Tokenizer | byte-level BPE tokenization | hex/byte decoding |
| 2 | The Gatekeeper | indirect prompt injection | encoding (base64) |
| 3 | Raw Logits | argmax greedy decoding | math (logits) |
| 4 | Shifted Memory | training-data extraction | crypto (Caesar) |

Built with **Python / Flask**. Flags are verified **server-side**; the Challenge-2
bot also runs server-side. Each challenge file is shown inline **and** downloadable.

## Run locally
```bash
pip install -r requirements.txt
python3 api/index.py
```
Then open **http://localhost:5000**

## Deploy to Vercel
This repo is Vercel-ready (`vercel.json` + `api/index.py` as a Python serverless
function). To deploy:

1. Go to **https://vercel.com/new**
2. **Import** the GitHub repo `oattao123/ctf-ai-1`
3. Leave the defaults (Vercel auto-detects `vercel.json`) and click **Deploy**

Once connected, every push to the repo auto-deploys. No build settings needed.

## Layout
```
api/index.py     Flask app — all routes, flags (server-side), bot, page & files embedded
vercel.json      Vercel Python serverless config
requirements.txt flask
Mini-KMUTTCTF-2025-AI-Edition.docx   assignment write-up (1.1–1.3 + solutions)
SOLUTIONS.md     full solutions
```

> Solutions are in `SOLUTIONS.md` (no peeking yet 😉).
