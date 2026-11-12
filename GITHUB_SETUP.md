# GitHub publishing guide

## Repository metadata

- Name: `pdf-rag-assistant`
- Description: `PDF question answering with Qwen, Sentence Transformers, and FAISS, featuring page citations, quotation validation, and a Colab workflow.`
- Topics: `rag`, `llm`, `pdf`, `question-answering`, `faiss`, `sentence-transformers`, `qwen`, `python`, `google-colab`, `generative-ai`
- Suggested first commit: `Add PDF RAG notebook and project documentation`

## Upload with the GitHub website

1. Extract the ZIP and open the `pdf-rag-assistant` folder.
2. On GitHub, create a new repository named `pdf-rag-assistant`.
3. Choose the visibility you want. Do not generate another README because one is included.
4. Select the option to upload existing files, or use Add file → Upload files.
5. Upload the contents of the extracted folder, not the ZIP or its outer folder. Make sure `.gitignore` is included; your file browser may hide it.
6. Commit with the suggested message above.
7. Add the description and topics in the repository About section.
8. Confirm that README.md renders on the repository home page.

The gitignore file helps local Git staging. It is not an upload filter for files you manually choose on the website.

## Optional command-line upload

After creating an empty repository and authenticating Git with GitHub, run from the extracted project folder. Replace YOUR_USERNAME first.

```bash
git init
git branch -M main
git add README.md GITHUB_SETUP.md requirements.txt .gitignore PDF_RAG_AI_Assistant.ipynb
git commit -m "Add PDF RAG notebook and project documentation"
git remote add origin https://github.com/YOUR_USERNAME/pdf-rag-assistant.git
git push -u origin main
```

## What to add after a real demo run

- A screenshot showing a question, answer, page reference, and quotation from a document you may publish.
- The actual evaluated sample size and metrics, including failed cases.
- A license you have chosen for your code.
- A Streamlit app only after implementing and testing it; then update the README and requirements.

Do not claim high accuracy, zero hallucinations, agentic tool use, or Streamlit deployment based on the current notebook. Do not upload private PDFs, index files, model weights, credentials, or notebook outputs containing document text.

## Optional Open in Colab badge

After publishing, replace YOUR_USERNAME and add this line near the top of README.md:

```markdown
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/YOUR_USERNAME/pdf-rag-assistant/blob/main/PDF_RAG_AI_Assistant.ipynb)
```

## Portfolio description

Built a PDF question-answering prototype using Qwen2.5, Sentence Transformers, and FAISS, with overlapping text chunks, page-level source references, quotation validation, and an exact-match/token-F1 evaluation template.

## Package validation

The copied notebook has its saved outputs, execution counts, and cell metadata cleared. Original code cells are preserved. Non-shell cells were checked for Python syntax. Model downloads, GPU inference, PDF extraction, and end-to-end performance were not executed during packaging.
