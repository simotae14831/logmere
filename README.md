# logmere

Keep your log directories small without thinking about it

Small but I use it weekly.

## Examples

```bash
# show what would be cleaned, change nothing
logwash ./logs --older-than 30 --dry-run

# archive logs older than 30 days
logwash ./logs --older-than 30 --archive ./backup
```

## What it does

- Exit codes friendly for cron and CI
- Filter by age (--older-than) or size (--larger-than)
- Archive matched logs into a timestamped .tar.gz
- Scan directories for log files by glob pattern
- Dry-run mode shows what would happen, touches nothing

## Installation

```bash
pip install -r requirements.txt
python -m logwash --help
```

## Project structure

```text
├── .github/
│   ├── ISSUE_TEMPLATE/
│   │   └── bug_report.md
│   ├── workflows/
│   │   └── ci.yml
│   └── dependabot.yml
├── docs/
│   ├── configuration.md
│   ├── development.md
│   └── usage.md
├── examples/
│   └── quickstart.md
├── logwash/
│   ├── __init__.py
│   ├── __main__.py
│   ├── cli.py
│   ├── errors.py
│   └── utils.py
├── tests/
│   └── test_cli.py
├── .editorconfig
├── .gitignore
├── CHANGELOG.md
├── CONTRIBUTING.md
├── LICENSE
├── pyproject.toml
└── requirements.txt
```

## License

MIT - see [LICENSE](LICENSE).
