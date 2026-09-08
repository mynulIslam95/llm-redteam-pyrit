# Six LLM attacks with JSON + HTML scoring.

The runner is a small custom loop, not Microsoft PyRIT.
Mock 6/6 means the stub refused. It does not prove a live model is safe.

## Setup

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
cp .env.example .env
```

## Tests

```bash
export MOCK_MODE=true
pytest -q
```

## Report

```bash
export MOCK_MODE=true
python -m redteam.run_redteam
```

Open the HTML path printed at the end (or the newest file in `reports/`).

## Layout

```text
redteam/attacks.py
redteam/run_redteam.py
tests/test_attacks.py
results/    JSON (gitignored)
reports/    HTML (gitignored)
```

Mynul Islam
