| [Home Page](./) | [data viz examples](dataviz-examples) |[Goverment Debt](debt-gdp-analysis)| [critique by design](critique-by-design) | [final project I](final-project-part-one) | [final project II](final-project-part-two) | [final project III](final-project-part-three) |

# Wireframes / storyboards
This project examines whether AI benchmark scores actually reflect what users prefer. Using three datasets — Chatbot Arena ELO scores, MMLU-Pro benchmark results, and the ShareChat real-world conversation corpus — I built a series of visualizations that trace the gap between how models perform on standardized tests and how users actually vote with their feet.

The story unfolds in five beats:

**Beat 1: Benchmarks and user preference are correlated — but imperfectly.**
The scatter plot below shows MMLU-Pro scores vs. Arena ELO for the top 50 models. There is a general upward trend, but the spread is wide. Some models score high on benchmarks yet rank lower in user preference, and vice versa.

**Beat 2: Some models wildly over- or underperform expectations.**
The rank gap chart reveals which models benchmark scores predict poorly. Gemma and Mistral models consistently score higher on MMLU-Pro than their Arena rank suggests. Claude models consistently do the opposite — users prefer them far more than their benchmark scores would predict.

**Beat 3: This pattern holds at the company level.**
Anthropic has an average rank gap of -17.2, meaning users prefer Claude models roughly 17 ranking positions higher than benchmarks suggest. Google has a gap of +16.8, meaning its models benchmark well but users choose them less often than expected.

**Beat 4: Open source models are systematically underestimated by benchmarks.**
Open source models have an average rank gap of -19.0 vs. +0.5 for proprietary models. Benchmarks do not capture the qualities users value in open models.

**Beat 5: Real-world usage data tells a similar story.**
ShareChat data from 130,000 publicly shared conversations shows ChatGPT dominates in volume, but Claude users have the second-deepest conversations by average turn count (4.6 turns), despite Claude having the fewest shared conversations. This suggests Claude users are highly engaged even if fewer in number.

<img width="1988" height="1229" alt="image" src="https://github.com/user-attachments/assets/f993fed9-7915-43f6-9708-970f468eb7e4" />


# User research 

## Target audience
> Include your approach to identifying representative individuals, and who you hope to reach with your story. 

Text here!

## Interview script
The goal of this research is to understand whether the story is clear to readers with different backgrounds, whether the visualizations communicate the key findings without explanation, and whether the call to action resonates.

| Goal | Questions to Ask |
|------|------------------|
| Understand first impressions | What do you think this story is about? What is the main takeaway? |
| Test chart readability | Looking at the rank gap chart, what does a negative number mean to you? |
| Test whether the finding is surprising | Does it surprise you that Claude scores lower on benchmarks but users prefer it? Why or why not? |
| Test relevance to audience | Would this information change how you choose or evaluate an AI model? |
| Identify confusion points | Is there anything confusing or that you would want more explanation on? |
| Test call to action | After seeing this, what do you think we should do differently when evaluating AI models? |


## Interview findings
This story is aimed at two types of audiences. 
The primary audience are AI product managers and technical leads who make model selection decisions for their products. They care about whether benchmark scores are a reliable proxy for user satisfaction. The secondary audiences are general tech-savvy readers who use AI tools regularly and have opinions about which models they prefer.

To find representative interviewees, I looked for people who use at least one AI assistant regularly, have some awareness of model differences, and come from different professional backgrounds. I interviewed one person with a technical background, one with a product/business background, and one general user.

| Questions               | Interview 1 (briefly describe) | Interview 2 | Interview 3 |
|-------------------------|--------------------------------|-------------|-------------|
| What is the main takeaway? | Benchmarks ≠ real user value; correlation exists but not enough for decision-making | Benchmarks are directional, but product experience matters more | I choose based on feel; didn’t know benchmarks differ |
| What does a negative rank gap mean to you? | Benchmarks overrate model; weak real-world alignment | Over-optimized for evals, not real use | Confusing; “good score but worse experience” |
| Surprised by Claude finding? | Not really; matches alignment expectations | Yes; expected stronger performance | Yes; thought it was top-tier |
| Would this change how you evaluate AI? | Yes; rely more on hands-on testing | Yes; consider use-case fit more | Slightly; still won’t check benchmarks |
| Anything confusing? | Rank gap unclear initially | Too many metrics without explanation | Most terms and charts are hard to understand |
| What should we do differently? | Add concrete use-case comparisons | Tie insights to decision-making | Simplify language; clearer takeaway |




# Identified changes for Part III

| Research synthesis                       | Anticipated changes for Part III                                                |
|------------------------------------------|---------------------------------------------------------------------------------|
| Rank gap is hard to interpret            | Add a one-line definition + simple visual cue (e.g., arrows or labels)         |
| Metrics feel too abstract                | Include 2–3 concrete task examples (e.g., coding, writing, search)             |
| Missing decision guidance for PMs        | Add “When to choose which model” summary section                               |
| Too many technical terms                 | Simplify wording; reduce jargon (Arena, MMLU) or add quick explanations        |
| General audience feels excluded          | Add plain-language takeaway box (“What this means for you”)                     |
| Over-focus on benchmarks                 | Balance with real-world usage insights and qualitative interpretation          |
| Claude result not well explained         | Add brief explanation of why (alignment vs benchmark optimization)             |



Overall, the story is directionally strong and insightful, but the main gap is accessibility. While technical audiences can follow the analysis, both product and general users need clearer interpretation and actionable takeaways. The next iteration should focus on bridging the gap between metrics and real-world decisions, making the insights easier to understand and apply.
## References
_List any references you used here._

## AI acknowledgements
I used Claude (Anthropic) extensively throughout Part II. Specifically, write Python code to download and clean data from HuggingFace, merge multiple datasets into a single analysis-ready file. Claude also helped structure the story arc and suggested the framing around benchmark vs. user preference gaps.

All interpretations of the data, final design decisions, and the overall narrative direction were my own. The visualizations shown here are drafts and will be rebuilt in Tableau and shorthand for the final submission.
