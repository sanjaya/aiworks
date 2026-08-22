# aiworks

Examples of prompt engineering techniques using Google's [`google-genai`](https://pypi.org/project/google-genai/) library and the Gemini API.

## Contents

- [`notebooks/Google_AI.ipynb`](notebooks/Google_AI.ipynb) — a Colab notebook walking through core prompting techniques with the Gemini API.

## Techniques covered

- **Client setup** — installing `google-genai` and authenticating with a `GEMINI_API_KEY`.
- **Writing clear, specific instructions** — using delimiters (backticks, quotes) to separate instructions from content.
- **Structured output** — asking the model to respond in JSON or HTML.
- **Condition checking** — having the model verify whether conditions are met before acting (e.g. rewriting instructions only if present in the text).
- **Few-shot prompting** — steering output style with example input/output pairs.
- **Giving the model time to "think"** — specifying multi-step tasks explicitly, and asking the model to work out its own solution before judging one.
- **Model limitations / hallucinations** — demonstrating how models can generate plausible but incorrect information.
- **Iterative prompt development** — refining a product description prompt through several rounds (length limits, audience focus, structured tables, HTML output).
- **Image generation** — generating an image with a Gemini image model and saving it locally.

## Setup

1. Install the library:
   ```bash
   pip install -U google-genai
   ```
2. Set your Gemini API key as an environment variable:
   ```bash
   export GEMINI_API_KEY="your-api-key"
   ```
   (In Colab, the notebook pulls this from Colab Secrets via `userdata.get('GEMINI_API_KEY')`.)
3. Open and run [`notebooks/Google_AI.ipynb`](notebooks/Google_AI.ipynb) in Jupyter or Google Colab.

## Requirements

- Python 3.9+
- A Gemini API key ([Google AI Studio](https://aistudio.google.com/))
- `google-genai`, `Pillow` (for image handling)
