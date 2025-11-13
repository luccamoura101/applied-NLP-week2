# Session 2 — Applied NLP

This repository contains the materials for **Session 2** of *Applied NLP*.  
- Slides: see [`slides/`](./slides/) folder  
- Notebooks: see [`notebooks/`](./notebooks/) folder 
---

## 📑 Session Outline

### Topic: Phrases & Collocations

This session explores multi-word expressions and phrase patterns in literary texts. Using two works by the same author (as an example Alice's Adventures in Wonderland and Through the Looking-Glass), you'll learn to:

1. **Bigrams & Trigrams** ([`1_AppliedNLP_Session2_Bi_Trigrams.ipynb`](./notebooks/1_AppliedNLP_Session2_Bi_Trigrams.ipynb))
   - Compute frequent bigrams and trigrams across two texts
   - Compare phrase frequencies using normalized rates
   - Identify distinctive phrases for each work
   - Visualize most characteristic multi-word expressions

2. **Pointwise Mutual Information (PMI)** ([`2_AppliedNLP_Session2_PMI.ipynb`](./notebooks/2_AppliedNLP_Session2_PMI.ipynb))
   - Measure collocation strength using PMI scores
   - Identify strongly associated word pairs beyond raw frequency
   - Compare PMI-based collocations across works
   - Export reproducible analysis artifacts

3. **POS Pattern Frequency** ([`3_AppliedNLP_Session2_POS_Patterns.ipynb`](notebooks/2_AppliedNLP_Session2_POS_Patterns.ipynb))
   - Analyze grammatical patterns in bigrams (ADJ+NOUN, VERB+NOUN, etc.)
   - Apply spaCy POS tagging for syntactic analysis
   - Visualize distribution of POS patterns
   - Compare syntactic phrase structure across texts

4. **Phrase Diversity (n-gram TTR)** ([`4_AppliedNLP_Session2_Phrase_Diversity.ipynb`](./notebooks/4_AppliedNLP_Session2_Phrase_Diversity.ipynb))
   - Measure phrase variety using Type-Token Ratio (TTR)
   - Compare lexical/phrasal diversity across works
   - Analyze diversity trends by section/chapter
   - Interpret TTR as indicator of stylistic formulaicity vs. variety

5. **Collocation Network** ([`5_AppliedNLP_Session2_Collocation_Network.ipynb`](notebooks/3_AppliedNLP_Session2_Collocation_Network.ipynb))
   - Visualize word collocations as network graphs
   - Identify hub words and collocation clusters
   - Explore phrase structure through network topology
   - Compare collocation patterns between texts

### Key Concepts
- **N-grams**: Contiguous sequences of n tokens (bigrams, trigrams)
- **Collocations**: Words that frequently co-occur in predictable patterns
- **PMI**: Statistical measure of association between words in bigrams
- **TTR**: Ratio of unique to total n-grams, measuring diversity
- **POS patterns**: Grammatical templates underlying phrases

### Data
All notebooks work with Project Gutenberg texts in the [`data/`](./data/) folder:
- `Wonderland.txt` — Alice's Adventures in Wonderland by Lewis Carroll
- `Looking-Glass.txt` — Through the Looking-Glass by Lewis Carroll

Notebooks include robust preprocessing to strip Gutenberg headers, normalize quotes, and handle encoding artifacts. For your texts, you should implement different preprocessing steps if needed.

---
## 🚀 Environment Setup

Before starting, please **fork this repository** and create a fresh Python virtual environment.  
All required libraries are listed in `requirements.txt`.

> ⚠️ If you encounter errors during `pip install`, try removing the version pinning for the failing package(s) in `requirements.txt`.  
> On Apple M1/M2 systems you may also need to install additional system packages (the “M1 shizzle”).

---

### macOS / Linux (bash/zsh)

```bash
# Select Python version (if using pyenv)
pyenv local 3.11.3

# Create and activate virtual environment
python -m venv .venv
source .venv/bin/activate

# Upgrade pip and install dependencies
pip install --upgrade pip
pip install -r requirements.txt
```

### Windows (PowerShell)
```bash
# Select Python version (if using pyenv)
pyenv local 3.11.3

# Create and activate virtual environment
python -m venv .venv
.venv\Scripts\Activate.ps1

# Upgrade pip and install dependencies
python -m pip install --upgrade pip
pip install -r requirements.txt
```

### Windows (Git Bash)
```bash
# Select Python version (if using pyenv)
pyenv local 3.11.3

# Create and activate virtual environment
python -m venv .venv
source .venv/Scripts/activate

# Upgrade pip and install dependencies
python -m pip install --upgrade pip
pip install -r requirements.txt
```

You’re now ready to run the session notebooks!

Deactivate the environment when you’re done:
```bash
deactivate
```
