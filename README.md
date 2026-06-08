# Auto Tagging Support Tickets Using LLM

## Objective
Automatically tag support tickets into predefined categories using a large language model, comparing zero‑shot and few‑shot approaches.

## Methodology
- **Model**: `facebook/bart-large-mnli` (zero‑shot classification)
- **Categories**: billing, technical issue, account management, cancellation, product inquiry, refund request
- **Techniques**:
  - Zero‑shot: direct classification without examples
  - Few‑shot: prompt with example tickets to guide prediction
- **Output**: Top‑3 tags with confidence scores for each ticket
- **Deployment**: Gradio web app (live demo available)

## Results
- Zero‑shot works well for clear categories (e.g., “billing” for duplicate charges).
- Few‑shot shows different score distributions, demonstrating prompt sensitivity.
- Example output for “I was charged twice” → `[('billing', 0.80), ('account management', 0.08), ('refund request', 0.05)]`

## Files
- `task5_auto_tagging.ipynb` – full implementation
- `ticket_tags.csv` – output for test tickets
- `requirements.txt` – dependencies

## How to Run
1. Clone this repository.
2. Install dependencies: `pip install -r requirements.txt`
3. Run the notebook or convert to `.py`.
4. The Gradio interface will launch with a public link (valid 72 hours).

## Live Demo
[https://7078be4f10193d4ad2.gradio.live/]
