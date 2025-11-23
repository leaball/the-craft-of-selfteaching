# CLAUDE.md - AI Assistant Guide

## Repository Overview

**Project Name**: 自学是门手艺 (The Craft of Self-teaching)
**Author**: 李笑来 (Li Xiaolai)
**Primary Language**: Chinese (中文)
**Format**: Jupyter Notebooks (.ipynb) + Markdown (.md)
**License**: CC-BY-NC-ND
**Purpose**: Educational book teaching self-learning skills through Python programming

This is a comprehensive self-teaching guide that uses programming as an entry point to develop self-learning abilities. The book emphasizes that self-teaching is a learnable craft, not a talent, and provides practical exercises through interactive Jupyter notebooks.

## Core Philosophy

> "自学是门手艺" - Self-teaching is a craft (a skill that can be learned through practice)

The book's central thesis:
- Self-learning is not about innate talent but about deliberate practice
- 99% of people never develop true self-learning ability
- Programming is used as a practical vehicle to develop this meta-skill
- Proof of Work (PoW) concept: readers prove their learning through Git commits

## Repository Structure

### Root Directory

```
the-craft-of-selfteaching/
├── *.ipynb                          # Main content (Jupyter notebooks)
├── markdown/                        # Markdown versions of all content
├── from-readers/                    # Community contributions and success stories
├── my-notes/                        # Space for reader's personal notes
├── images/                          # Image assets
├── README.md                        # Main documentation (Chinese)
├── mycode.py, that.py              # Sample Python scripts
├── *.txt                           # Data files for exercises
└── test-file.txt                   # Test file for file I/O exercises
```

### Content Organization

The book is structured in **3 main parts** plus appendices:

#### **Part 1: Foundation & Basic Python** (Part.1.*.ipynb)
- **A**: Why master self-teaching ability?
- **B**: Why start with coding?
- **C**: Learning through reading
- **D**: Preparation for reading
- **E.1-E.7**: Core Python basics
  - E.1: Entrance
  - E.2: Values and operators
  - E.3: Control flow
  - E.4: Functions
  - E.5: Strings
  - E.6: Containers (data structures)
  - E.7: Files
- **F**: Dealing with forward references
- **G**: Official Python Tutorial

#### **Part 2: Functions & Deliberate Practice** (Part.2.*.ipynb)
- **A**: Clumsiness and patience
- **B**: Deliberate practicing
- **C**: Why start from writing functions?
- **D.1-D.8**: Advanced function concepts
  - D.1: Function arguments (part 1)
  - D.2: Function arguments (part 2)
  - D.3: Lambda functions
  - D.4: Recursion
  - D.5: Docstrings
  - D.6: Modules
  - D.7: Test-Driven Development (TDD)
  - D.8: Executable Python files
- **E**: Deliberate thinking

#### **Part 3: Advanced Topics & Philosophy** (Part.3.*.ipynb)
- **A**: Conquering difficulties
- **B.1-B.5**: Advanced Python concepts
  - B.1: Classes - OOP introduction
  - B.2: Classes - Python implementation
  - B.3: Decorators, Iterators, Generators
  - B.4: Regular expressions (regex)
  - B.5: BNF, EBNF, PEBNF
- **C**: Breaking things down (分解)
- **D**: Indispensable illusion (rigid requirements illusion)
- **E**: Being thorough - the ultimate state of self-teaching
- **F**: Social aspects of self-teaching
- **G**: The golden age and Google
- **H**: Preventing focus drift

#### **Additional Sections**
- **00.cover**: Cover page
- **01.preface**: Preface
- **02.proof-of-work**: How to prove you've read this book (Git workflow)
- **Q.good-communication**: How to be an excellent communicator
- **R.finale**: The endpoint of self-learners
- **S.whats-next**: What's next after completing the book?

#### **Appendices** (T-appendix.*.ipynb)
- **jupyter-installation-and-setup**: Jupyterlab setup guide
- **git-introduction**: Git basics
- **editor.vscode**: VS Code installation and configuration
- **symbols**: What do these symbols mean?

### Directory Details

- **`markdown/`**: Contains Markdown (.md) versions of all Jupyter notebooks
  - Same filename structure as root notebooks
  - Easier for web viewing and version control diffs
  - Auto-generated from notebooks (added March 23, 2019)

- **`from-readers/`**: Community success stories and contributions
  - Reader experiences with self-teaching
  - Subdirectories for individual contributor stories
  - Submitted via Pull Requests
  - Subject to community voting for inclusion

- **`my-notes/`**: Personal notes directory
  - Readers can store their learning notes here
  - Tracked in personal forks
  - Contains example notes showing merge workflows

- **`images/`**: Image assets for the book
  - Screenshots for Git/GitHub tutorials
  - Diagrams and illustrations
  - CC license images

## Development Workflow

### Git Workflow Philosophy

This book uses Git as a **Proof of Work** system inspired by blockchain concepts:
- Every commit is proof that learning occurred
- Reading progress is verifiable through commit history
- Community contributions validated through Pull Requests

### Standard Reader Workflow

1. **Fork** the repository to your own GitHub account
2. **Clone** your fork locally
3. **Create a branch** (e.g., `study`) for personal learning
4. **Read and modify** notebooks in Jupyterlab
5. **Commit changes** regularly to track progress
6. **Push** to your fork as proof of work

### Contributing Corrections (校对)

When submitting corrections or improvements:

1. **Sync your fork** with upstream first (see 02.proof-of-work.ipynb)
2. **Create a new branch** from updated master (name: `from-<username>`)
3. **Make targeted changes** - one small fix per branch
4. **Write clear commit messages** explaining the change
5. **Submit Pull Request** with detailed description
6. **Wait patiently** for review

**Important**: Never submit PR from a "玩残了" (messed up) fork. Always start fresh from latest upstream.

### Branch Strategy

- **`master`**: Main branch, kept in sync with upstream
- **`study`** (or personal branch): Your learning journey with all modifications
- **`from-<username>`**: Short-lived branches for submitting corrections

## File Conventions

### Naming Patterns

Files follow a hierarchical naming convention:

```
[Section].[Subsection].[Topic].ipynb

Examples:
- Part.1.E.5.strings.ipynb       → Part 1, Section E (basics), Topic 5 (strings)
- Part.2.D.7-tdd.ipynb           → Part 2, Section D (functions), Topic 7 (TDD)
- T-appendix.git-introduction.ipynb → Technical appendix on Git
```

**Prefix meanings**:
- `Part.1` → Foundation
- `Part.2` → Practice
- `Part.3` → Advanced
- `T-appendix` → Technical appendix
- `Q`, `R`, `S` → Supplementary content
- `00`, `01`, `02` → Front matter

### Jupyter Notebook Structure

All `.ipynb` files follow consistent patterns:

1. **Title cell** (markdown): `# [Chapter Title]`
2. **Content cells**: Mix of markdown (text) and code (Python)
3. **Navigation cell** (markdown): `[Next Page](./next-file.ipynb)` at the end
4. **Code cells**: Executable Python examples
5. **Practice exercises**: Code cells for reader experimentation

### Markdown Versions

- Located in `markdown/` directory
- Identical structure to `.ipynb` files
- Auto-generated for better web readability
- Code blocks use triple backticks with `python` language tag

## Python Code Conventions

### Style

- **Simple and readable**: Code prioritizes clarity over cleverness
- **Progressive complexity**: Early chapters use basic syntax, later chapters introduce advanced patterns
- **Interactive learning**: All code is meant to be modified and re-run
- **Chinese comments**: Many comments and variable names use Chinese for Chinese readers

### Common Patterns

```python
# Philosophical pseudo-code (from README)
def teach_yourself(anything):
    while not create():
        learn()
        practice()
    return teach_yourself(another)

teach_yourself(coding)
```

### Data Files

Several text files are included for exercises:
- `words_alpha.txt` (4.2MB): English word list for text processing
- `hdi-china-1870-2015.txt`: Historical data for data analysis
- `life-expectancy-china-1960-2016.txt`: Statistical data
- `regex-target-text-sample.txt`: Sample text for regex practice
- `test-file.txt`: Basic file I/O testing

## Working with This Repository

### Reading the Book

**Recommended approach**:
1. Install Jupyterlab locally (see T-appendix.jupyter-installation-and-setup.ipynb)
2. Clone your fork
3. Open `.ipynb` files in Jupyterlab
4. Execute code cells with `Ctrl+Enter` or `Shift+Enter`
5. Modify code to experiment
6. Take notes in separate cells

**Alternative**: Read markdown versions on GitHub web interface

### Making Changes

**For personal learning**:
- Modify any file freely in your `study` branch
- Add cells, change code, write notes
- Commit regularly to track your progress
- Your changes prove your work

**For contributing corrections**:
- Only modify on fresh branches from latest master
- Keep changes minimal and focused
- Provide clear explanations in commit messages
- Target actual errors or improvements, not personal preferences

### Common Tasks

**Update fork from upstream**:
```bash
# Method 1: Command line (if upstream remote configured)
git fetch upstream
git merge upstream/master

# Method 2: GitHub web UI
# See detailed steps in 02.proof-of-work.ipynb
```

**Create learning branch**:
```bash
git branch study
git checkout study
# Make changes...
git add .
git commit -m "Completed Part 1.E.5 - practiced string methods"
git push origin study
```

**Submit a correction**:
```bash
git checkout master
git pull origin master
git checkout -b from-myusername
# Make correction...
git add .
git commit -m "Fix typo in Part.1.E.5.strings.ipynb line 42"
git push origin from-myusername
# Then create Pull Request on GitHub
```

## Key Concepts for AI Assistants

### When Helping with This Repository

1. **Respect the learning journey**: Don't just fix code - explain why
2. **Maintain Chinese context**: Keep Chinese text/comments unless specifically asked to translate
3. **Preserve educational value**: Code examples should remain simple and instructive
4. **Honor the license**: CC-BY-NC-ND means No Derivatives without permission
5. **Understand dual formats**: Changes to .ipynb may need corresponding .md updates

### Content Philosophy

- **Self-teaching first**: Solutions should encourage independent thinking
- **Process over product**: The journey of learning matters more than the end result
- **Proof of work**: Visible progress (commits) is part of the pedagogy
- **Old truths, not new tricks**: The book deliberately avoids "新鲜" (novelty) in favor of proven methods
- **Everyone can learn**: No talent required, only patience and practice (熟能生巧)

### Common Reader Issues

Based on the book's design, readers often:
1. Struggle with Git/GitHub workflow initially
2. Need encouragement to actually execute and modify code
3. Want to skip ahead (forward references are a known challenge)
4. Need reminders that "clumsiness is normal" (笨拙与耐心)
5. Benefit from the community aspect (from-readers/ stories)

### Technical Context

- **Python version**: Generally Python 3.x (check notebooks for specifics)
- **Jupyter**: Designed for Jupyterlab, but works in classic Jupyter
- **No external dependencies**: Most examples use standard library only
- **Platform agnostic**: Works on Windows, Mac, Linux

## Special Files

### Configuration Files

- **`.gitignore`**: Standard Python/Jupyter ignore patterns
- **`.vs/VSWorkspaceState.json`**: Visual Studio workspace state (can be ignored)

### Sample Code Files

- **`mycode.py`**: Example Python script file for module exercises
- **`that.py`**: Additional sample code for import demonstrations
- **`symbols.numbers`**: Binary/data file for file handling exercises (164KB)
- **`results.txt`**: Output file from exercises (37KB)

## Cultural and Linguistic Notes

### Chinese-English Mix

The repository uses both languages strategically:
- **Chinese**: Main content, philosophical discussions, cultural references
- **English**: Code, technical terms, Git commands, some comments
- **Pinyin**: Occasionally for transliteration

### Key Chinese Terms

- **自学** (zìxué): Self-teaching, self-learning
- **手艺** (shǒuyì): Craft, skill, handicraft
- **老生常谈** (lǎoshēng chángtán): "Old student's constant talk" - clichés, platitudes (but treated positively)
- **刚需幻觉** (gāngxū huànjué): "Rigid requirements illusion"
- **积累** (jīlěi): Accumulation (key concept - gradual progress)
- **刻意练习** (kèyì liànxí): Deliberate practice
- **積ん読** (tsundoku): Japanese loan word - books bought but never read

### Author's Voice

Li Xiaolai (李笑来) writes in a:
- Direct, conversational tone
- Self-deprecating style ("老生" - old student)
- Encouraging but realistic manner
- Philosophy-meets-practice approach
- Sometimes uses "chicken soup" (鸡汤) metaphor for motivational content

## Git Branch Guidelines

### Current Branch Context

When working on this repository, note the branch name format:
- Branch names starting with `claude/` are for AI assistant work
- Format: `claude/claude-md-<session-id>`
- Example: `claude/claude-md-mibl3qgd41dhflo4-01AzPp7Haq55W4X5prNZuf3i`

### Push Requirements

- Always use: `git push -u origin <branch-name>`
- Branch MUST start with `claude/` for AI assistant commits
- Branch MUST end with matching session ID
- Network failures: retry up to 4 times with exponential backoff (2s, 4s, 8s, 16s)

## Version Control Best Practices

### For AI Assistants

1. **Always read files before editing**: Understand context first
2. **Commit atomic changes**: One logical change per commit
3. **Write descriptive messages**: Explain "why" not just "what"
4. **Respect existing structure**: Don't reorganize without reason
5. **Test code changes**: Ensure Python examples still run
6. **Preserve formatting**: Maintain existing indentation and style

### Commit Message Style

Based on existing history:
```
# Good examples (Chinese is acceptable)
替换了一下这几行的顺序，这样能更清晰地表明s这个字符串被用于下面的三个方法，也更易懂一些
Update 00.cover.ipynb
修改了一个单词
Update Part.1.E.5.strings.md

# Pattern: Clear, specific, humble tone
```

## Integration Points

### External References

The book references several external resources:
- **Official Python Tutorial**: Part.1.G.The-Python-Tutorial-local.ipynb
- **GitHub**: https://github.com/selfteaching/the-craft-of-selfteaching
- **Jupyterlab**: Installation guide included
- **VS Code**: Editor setup guide included

### Community Platforms

- **GitHub Issues**: For bug reports
- **Pull Requests**: For corrections and reader stories
- **Forks**: Each reader's personal workspace
- **Votes**: Community decides which reader stories get merged

## Maintenance Notes

### What to Update

When helping maintain this repository:
- ✅ Fix typos and grammatical errors
- ✅ Correct code errors or deprecated syntax
- ✅ Update broken links
- ✅ Improve clarity of explanations
- ✅ Add to CLAUDE.md as repository evolves

### What to Preserve

- ❌ Don't change the author's voice or philosophy
- ❌ Don't reorganize structure without explicit request
- ❌ Don't translate Chinese to English (it's intentional)
- ❌ Don't "modernize" intentionally simple code
- ❌ Don't add complex dependencies

## Summary for AI Assistants

This repository is a **teaching tool** that uses:
1. **Git as pedagogy**: Commits prove learning happened
2. **Jupyter for interactivity**: Code must be runnable and modifiable
3. **Chinese as primary language**: Culturally grounded learning
4. **Simplicity as principle**: Clarity over cleverness
5. **Community as motivation**: Reader stories inspire others

When working with this repository, prioritize:
- **Educational value** over technical sophistication
- **Reader experience** over perfect code
- **Cultural context** over translation
- **Process documentation** over just results
- **Encouragement** balanced with honesty

The ultimate goal: help readers develop the meta-skill of self-teaching by practicing on a concrete skill (programming).

---

**Last Updated**: 2025-11-23
**Repository**: https://github.com/selfteaching/the-craft-of-selfteaching
**License**: CC-BY-NC-ND
