# Workspace Instructions

FastAPI-based Social Bingo game. Requires **Python 3.13+** and **uv**.

---

## ✅ MANDATORY DEVELOPMENT CHECKLIST

**Run before every commit:**

```bash
# 1. Format code
uv run ruff format .

# 2. Lint code  
uv run ruff check .

# 3. Run all tests
uv run pytest
```

If any step fails, fix issues before committing.

---

## 🚀 Quick Start

```bash
uv sync                                      # Setup dependencies
uv run uvicorn app.main:app --reload        # Run server (http://localhost:8000)
uv run pytest                                # Run tests
uv run ruff check . && uv run ruff format .  # Lint & format
```

---

## 📁 Project Structure

```
app/
├── main.py           # FastAPI routes & server
├── game_logic.py     # GameBoard class & win detection
├── game_service.py   # Game session management
├── models.py         # Pydantic schemas
├── data.py           # Bingo questions
├── static/           # CSS, JS, images
└── templates/        # Jinja2 HTML
tests/                # Pytest tests
workshop/             # Lab guides
```

---

## 🎮 Common Tasks

**Add bingo questions:** Edit `app/data.py` QUESTIONS list → restart server

**Modify game logic:** Edit `app/game_logic.py` or `app/game_service.py` → run `uv run pytest` → restart

**Style components:** Add CSS to `app/static/css/app.css` → use in templates

**Add routes:** Edit `app/main.py` → add FastAPI route → test with `uv run pytest`

---

## 🧪 Testing

```bash
uv run pytest              # Run all tests
uv run pytest -v           # Verbose output
uv run pytest -x           # Stop on first failure
uv run pytest -s           # Show print statements
```

Tests use **httpx** for API testing. Examples in `tests/` folder.

---

## 🔧 Code Quality

- **Linter:** Ruff (PEP 8, target Python 3.13+, line length 88)
- **Enabled rules:** E (errors), F (pyflakes), I (imports), N (naming), W (warnings)
- **Auto-fix:** `uv run ruff check . --fix`

---

## 📚 Resources

- **Lab guides:** See `workshop/` folder
- **FastAPI:** https://fastapi.tiangolo.com/
- **Pytest:** https://docs.pytest.org/
- **Ruff:** https://docs.astral.sh/ruff/

---

**Deploy to GitHub Pages:** Auto-deploys on push to `main` (ensure tests pass first)

**Need help?** Check workshop guides, review existing tests, or open an issue.

---

**Happy coding! 🚀**
