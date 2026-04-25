| [Home Page](./) | [data viz examples](dataviz-examples) |[Goverment Debt](debt-gdp-analysis)| [critique by design](critique-by-design) | [final project I](final-project-part-one) | [final project II](final-project-part-two) | [final project III](final-project-part-three) |



# Outline
Every week, a new AI model claims the top spot on a benchmark leaderboard. But a closer look at the data tells a different story. Models that score highest on standardized tests are not always the ones users actually prefer. The gap between what benchmarks reward and what people choose is not random. It reflects something more systematic about how we measure intelligence, what those tests actually capture, and which qualities matter most in real-world use.

This project uses data to explore that gap. By combining benchmark scores from standardized tests with user preference data from Chatbot Arena, I examine whether leaderboard rankings reflect real user satisfaction, or whether the models users return to are often the ones that rank lower on paper. I also look at patterns by company and model type to investigate what kinds of models users favor, and where benchmarks fall short as a signal.


**One sentence summary**
AI benchmark rankings consistently diverge from real user preferences, revealing a disconnect between how we measure model performance and how users actually experience it.

As a reader, I want to recognize that benchmark rankings reflect narrow test performance rather than real-world usefulness, so that I can think more critically about how the AI industry defines "the best." I can do this by looking beyond leaderboard scores when evaluating AI tools and paying attention to user preference signals.



## Initial sketches
<img width="2165" height="1114" alt="IMG_0637" src="https://github.com/user-attachments/assets/5d10103c-ad4c-4e34-b3d4-1084ab11828d" />



# The data
This project draws on three datasets.

The first is Chatbot Arena ELO scores from HuggingFace, covering user preference rankings for major AI models based on head-to-head comparisons. Each model's ELO score reflects how often real users chose it over alternatives.
The second is benchmark and model metadata scraped from openlm.ai, which aggregates standardized test scores including MMLU-Pro, GPQA, and HumanEval. These scores represent how models perform on academic and reasoning tasks.
The third is the ShareChat dataset from HuggingFace, which contains real user conversation data across major AI models including ChatGPT, Claude, Gemini, Grok, and Perplexity. This provides a second signal for real-world usage patterns beyond the Arena voting system.

All three datasets were cleaned and merged in Python, producing a final dataset of 188 models with both benchmark and user preference scores.

| Name | URL | Description |
|------|-----|-------------|
| Chatbot Arena ELO Scores | [mathewhe/chatbot-arena-elo](https://huggingface.co/datasets/mathewhe/chatbot-arena-elo) | User preference rankings based on head-to-head comparisons across major AI models |
| Benchmark Metadata | [openlm.ai/chatbot-arena](https://openlm.ai/chatbot-arena) | Standardized benchmark scores (MMLU-Pro, GPQA, HumanEval) per model, scraped via pd.read_html() |
| ShareChat Dataset | [tucnguyen/ShareChat](https://huggingface.co/datasets/tucnguyen/ShareChat) | Real user conversation data across AI models including ChatGPT, Claude, Gemini, Grok, and Perplexity |

# Method and medium
The project is built using Shorthand as the primary storytelling platform, with data visualizations created in Tableau and embedded throughout the narrative. Data cleaning, merging, and analysis were done in Python using pandas. The final output is an interactive, scrollable story published on Shorthand, with supporting code and datasets documented in a GitHub repository.

## References
He, M. (2024). Chatbot Arena ELO Scores [Dataset]. HuggingFace.
https://huggingface.co/datasets/mathewhe/chatbot-arena-elo

openlm.ai. (2024). Chatbot Arena Model Benchmark Scores [Web scrape].
https://openlm.ai/chatbot-arena. Accessed April 2026.

Yan, Y., Nguyen, T., Su, B., Lieffers, M., & Le, T. (2025). ShareChat: A Dataset of
Chatbot Conversations in the Wild. arXiv:2512.17843.
https://huggingface.co/datasets/tucnguyen/ShareChat

Zheng, L. et al. (2023). Judging LLM-as-a-judge with MT-Bench and Chatbot Arena.
arXiv:2306.05685. https://arxiv.org/abs/2306.05685

## AI acknowledgements
Claude (Anthropic) was used. Specifically, it assisted with brainstorming and refining the project topic, drafting and editing the outline and high-level summary, structuring the story arc.
