# INSA AI Model - retrained by Yusuf

Llama 3.1 8B fine-tuned (QLoRA, Unsloth) on a dataset about INSA (Information Network Security Administration of Ethiopia) and cyber security fundamentals. Final project of the INSA Cyber Talent Summer Camp.

## Dataset
- `dataset.json`: 319 instruction-response examples (INSA, creator and cyber security Q&A)
- Each INSA fact appears with several question phrasings, and unknown details have "I do not have confirmed information" answers to reduce hallucination.

## Sources
- INSA website: https://insa.gov.et (blog, duties and responsibilities)
- INSA Cyber Talent Summer Camp announcements (3rd, 4th, 5th rounds), talent portal https://talent.insa.gov.et
- Fana Broadcasting, AllAfrica, The EastAfrican, Capital Ethiopia (INSA statistics and camp news)
- Bahir Dar University and Debre Berhan University news pages (2026)
- Information Network Security Agency Re-establishment Proclamation No. 808/2013
- Information Technology Products Security Clearance and Control Proclamation No. 1310/2023
- General cyber security knowledge (CIA triad, OWASP, NIST, MITRE ATT&CK, etc.)

## Training
Base model: `unsloth/Meta-Llama-3.1-8B-bnb-4bit`, LoRA r=32, 6 epochs, learning rate 2e-4, cosine schedule, Google Colab T4. Exported as GGUF Q4_K_M.

## Run with Ollama
Download the `.gguf` and `Modelfile` from Hugging Face into one folder:

    ollama create insa-model -f Modelfile
    ollama run insa-model

Model on Hugging Face: https://huggingface.co/yusufnesredin/insa-ai-model-retrained-by-yusuf

## Author and Developer

**Prepared and developed by:** Yusuf Nesredin
**Grade:** 9th grade student
**Project:** Final project of the 5th INSA Cyber Talent Summer Camp

Thankyou!!