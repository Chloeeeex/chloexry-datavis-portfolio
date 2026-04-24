
| [Home Page](./) | [data viz examples](dataviz-examples) |[Goverment Debt](debt-gdp-analysis)| [critique by design](critique-by-design) | [final project I](final-project-part-one) | [final project II](final-project-part-two) | [final project III](final-project-part-three) |


# The final data story
**Shorthand Story:** [Ranked #1, Chosen by Nobody](https://carnegiemellon.shorthandstories.com/ai-model-analysis/index.html)


# Changes made since Part II
The core story stayed the same, but Part III focused on making it accessible. 

User research in Part II revealed that the rank gap concept was the main source of confusion, and that non-technical readers felt left out by the jargon. Three changes shaped the final version.

First, I reframed the opening. Instead of leading with data methodology, the story now opens with a question the audience already has an opinion on: "Does scoring #1 on a test mean anything to you?" This grounds the story before any data appears.
<img width="600" height="250" alt="Screenshot 2026-04-24 at 3 23 04 PM" src="https://github.com/user-attachments/assets/d1fc0ca4-dfa3-4560-b201-642dc4ecbe39" />

Second, I restructured the narrative into two parallel tracks — Test-Based Approach and People-Based Approach — so readers can follow the contrast without needing to understand benchmarking upfront. The MMLU-Pro, GPQA, and HumanEval benchmarks are introduced briefly with plain-language descriptions, not technical definitions.
<img width="716" height="512" alt="Screenshot 2026-04-24 at 3 24 35 PM" src="https://github.com/user-attachments/assets/b05258fd-126a-4bb1-9edc-f44014ad6bb5" />


Third, I pulled the company-level comparison forward. The Google vs. Anthropic finding is the most concrete and surprising result. Making it the narrative climax, rather than a supporting detail, gave the story a clearer emotional arc.

## The audience
The primary audience is **AI product managers and technical leads** who make model selection decisions. They are familiar with AI tools but may not have thought critically about whether benchmark rankings map to user satisfaction.

A secondary audience is **general tech-savvy readers** who use AI tools and form their own preferences. Interview 3 (a general user) told me she "didn't know benchmarks differ" and chooses based on feel. This confirmed that the story needs to work for people who have never seen a leaderboard.

To serve both audiences, I used two layers of content: the narrative text for general readers, and the Tableau visualizations for readers who want to dig into the data. The title "Ranked #1, Chosen by Nobody" is designed to hook both groups — it signals the conclusion without requiring any prior knowledge.


## Final design decisions
**Structure over density.** Part II storyboards had five dense beats. The final version organizes them into named sections with clear transitions, so readers always know where they are in the story.

**Tableau for the data, Shorthand for the story.** I kept the charts in Tableau Public and embedded them in Shorthand rather than using static images. This allows readers to hover and explore, which helps the rank gap visualization in particular — seeing the actual model names on hover makes the finding more concrete.

**Color as signal.** I used a consistent color scheme across charts, where warmer tones highlight models that underperform user expectations and cooler tones highlight models that outperform. This makes the Google vs. Anthropic comparison visually immediate without needing labels.

**Reducing jargon.** Terms like "Arena ELO" and "MMLU-Pro" appear in the story but are always followed by a plain-language explanation. Interview findings showed that even technically literate readers found the terminology abstract on first pass.


## References

## AI acknowledgements
I used Claude throughout this project for Python data cleaning and structuring the story arc. All analytical interpretations, design decisions, and the final narrative are my own. Visualizations were built in Tableau and assembled in Shorthand.

# Final thoughts
The biggest lesson from this project or from the whole lesson is that the hardest part of data storytelling is not finding the insight — it is deciding what *not* to show. I had five strong analytical findings in Part II, but showing all five in a linear sequence made the story feel like a report rather than a narrative. Choosing one central tension (benchmark rank vs. user preference) and building everything else around it made the story more coherent.

I also learned that user research feedback is most useful when you treat it as evidence, not just suggestions. As someone who had spent weeks with the data, I had already internalized what "rank gap" and "Arena ELO" meant. It took an outside reader to show me that these terms created a barrier before the insight even landed. The people closest to the work are often the last to notice what needs explanation.

