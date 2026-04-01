| [Home Page](./) | [data viz examples](dataviz-examples) |[Goverment Debt](debt-gdp-analysis)| [critique by design](critique-by-design) | [final project I](final-project-part-one) | [final project II](final-project-part-two) | [final project III](final-project-part-three) |


# Critique by Design: AI Model Capability Comparison

## Step one: the visualization
**Original visualization:**     

<img width="400" height="500" alt="image" src="https://github.com/user-attachments/assets/7862eb93-1caf-4ece-b9f9-c5fe0d0eba70" />

[Which AI Models Hallucinate the Most?](https://www.voronoiapp.com/technology/Which-AI-Models-Hallucinate-the-Most-7211)  
*Source: Voronoi App, published November 24, 2025. Data from Artificial Analysis's Omniscience Index.*

I chose this visualization because it is directly relevant to my daily life. I use AI tools constantly, for writing, coding, and research. But I rarely stop to ask: which model should I actually trust?

The chart plots AI models across two dimensions: Accuracy Index (higher is better) and Hallucination Index (lower is better). This framing immediately caught my attention. A model can be highly accurate but also highly prone to hallucinating, and that tradeoff matters enormously in real-world applications.

The stakes feel real. The original article notes that over 50 US court cases cited fake AI-generated legal sources in a single month. 
Enterprises lost over $67 billion in 2024 due to AI hallucinations. Picking the wrong model is not just a technical mistake. It can have serious consequences.

That is why I wanted to take this visualization further. The original quadrant chart tells a story, but I felt it could tell it more clearly.

## Step two: the critique
Based on Stephen Few's Data Visualization Effectiveness Profile, the original visualization were evaluated as follows:

## Step Two: The Critique

I used Stephen Few's Data Visualization Effectiveness Profile to evaluate the original 
visualization across seven dimensions.

**Usefulness (8/10):** The topic is directly relevant to anyone using AI tools in their work or research. The chart answers a practical question: which model is both accurate and trustworthy? I rated it an 8 because the core information is genuinely valuable.

**Completeness (6/10):** The two axes cover the key metrics, but there is no explanation of how the Accuracy Index or Hallucination Index are calculated. The two annotation boxes add some context, but only for two models out of seventeen. Most data points are left without supporting explanation.

**Perceptibility: (5/10)** The biggest issue is the X-axis direction. Hallucination increases left to right, meaning "better" is on the left side of the chart. This is counter-intuitive. Most readers expect better performance to sit toward the right or top-right. The company logos are visually appealing but add clutter and make it harder to locate specific models quickly.

**Truthfulness (4/10):** This is where the chart struggles most. The "ideal" quadrant is top-left, which goes against most readers' instincts. The chart does not lie, but the axis orientation creates a strong risk of misreading. A reader scanning quickly could easily conclude that top-right models are the best performers, when in fact they are among the worst.

**Intuitiveness (5/10):** The Proprietary vs Open Weights distinction is clear and easy to follow. But the quadrant logic requires careful reading before it clicks. There is no visual cue, such as an arrow or shaded region, to guide readers toward the "better" corner.

**Aesthetics (8/10):** The design is polished and the logo bubbles give it a distinctive, editorial feel. The color palette is clean and the overall layout is visually appealing.

**Engagement (8/10):** The subject is timely and the format invites comparison. Readers are likely to search for their preferred model and share the chart with others.

**Overall:** The visualization is visually strong but structurally confusing. The inverted X-axis and the absence of a clear "better" direction 
undermine how accurately readers interpret the data. These issues became the central focus of my redesign.

## Step three: Sketch a solution
<img width="500" height="270" alt="Screenshot 2026-04-01 at 3 49 29 PM" src="https://github.com/user-attachments/assets/45453641-6643-4f4e-a51a-f21c3c6418eb" />

<div class='tableauPlaceholder' id='viz1775072115228' style='position: relative'><noscript><a href='#'><img alt='Top-Performing Models ' src='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;AI&#47;AImodeldraft&#47;Sheet2&#47;1_rss.png' style='border: none' /></a></noscript><object class='tableauViz'  style='display:none;'><param name='host_url' value='https%3A%2F%2Fpublic.tableau.com%2F' /> <param name='embed_code_version' value='3' /> <param name='site_root' value='' /><param name='name' value='AImodeldraft&#47;Sheet2' /><param name='tabs' value='no' /><param name='toolbar' value='yes' /><param name='static_image' value='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;AI&#47;AImodeldraft&#47;Sheet2&#47;1.png' /> <param name='animate_transition' value='yes' /><param name='display_static_image' value='yes' /><param name='display_spinner' value='yes' /><param name='display_overlay' value='yes' /><param name='display_count' value='yes' /><param name='language' value='en-US' /><param name='filter' value='publish=yes' /></object></div>                
<script type='text/javascript'>                    
  var divElement = document.getElementById('viz1775072115228');                    
  var vizElement = divElement.getElementsByTagName('object')[0];                    
  vizElement.style.width='100%';vizElement.style.height=(divElement.offsetWidth*0.75)+'px';                    
  var scriptElement = document.createElement('script');                    
  scriptElement.src = 'https://public.tableau.com/javascripts/api/viz_v1.js';                   
  vizElement.parentNode.insertBefore(scriptElement, vizElement);                
</script>

## Step four: Test the solution

| Question | Response |
|----------|----------|
| Can you tell me what you think this is? | A scatter plot comparing AI models on two performance metrics. |
| Can you describe to me what this is telling you? | The larger dots in the top-right area seem to be the best-performing models. The dashed lines divide the chart into four quadrants using averages. |
| Is there anything you find surprising or confusing? | The Y-axis label "1 - Hallucination" requires extra thinking. It is not immediately clear which direction is better. The larger dot size also needs a legend to explain what it means. |
| Who do you think is the intended audience for this? | Researchers, engineers, or students who need to choose an AI tool for a specific use case. |
| Is there anything you would change or do differently? | Rename the Y-axis to something more intuitive. Add a short legend explaining the dot size. Make it clearer that top-right is the "best" zone. |


Synthesis: 

Two patterns emerged from the feedback. First, the Y-axis label "1 - Hallucination" was confusing and required extra mental effort to decode. Second, using dot size to highlight top performers was unclear without a legend.

Based on this, I made two changes in the final redesign. I replaced the red/grey color scheme with company-based colors, so readers can immediately see which provider each model belongs to. This makes the competitive landscape easier to read at a glance. I also added a subtitle "Factuality Score = 1 - Hallucination" directly under the chart title, so readers no longer have to decode the axis label on their own.

## Step five: build the solution

The final redesign addresses the two core issues identified in the critique and user feedback: the confusing axis label and the lack of company context.

The most significant change is the color encoding. Instead of a simple red/grey highlight, each dot is now colored by company. Readers can immediately see that Anthropic (orange) dominates the top-left quadrant, while most other providers cluster in the lower-left. This turns the chart from a simple performance ranking into a story about the competitive landscape.

The subtitle "Factuality Score = 1 - Hallucination" replaces the awkward axis label from the original. Readers no longer need to decode the formula themselves.

The average lines remain, dividing the chart into four quadrants. Models in the top-right quadrant are both highly accurate and highly factual, making them the strongest candidates for trust-critical applications.
<div class='tableauPlaceholder' id='viz1775073921443' style='position: relative'><noscript><a href='#'><img alt='Model Performance Across Accuracy and FactualityFactuality Score = 1 - Hallucination ' src='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;AI&#47;AImodelfinal&#47;Sheet22&#47;1_rss.png' style='border: none' /></a></noscript><object class='tableauViz'  style='display:none;'><param name='host_url' value='https%3A%2F%2Fpublic.tableau.com%2F' /> <param name='embed_code_version' value='3' /> <param name='site_root' value='' /><param name='name' value='AImodelfinal&#47;Sheet22' /><param name='tabs' value='no' /><param name='toolbar' value='yes' /><param name='static_image' value='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;AI&#47;AImodelfinal&#47;Sheet22&#47;1.png' /> <param name='animate_transition' value='yes' /><param name='display_static_image' value='yes' /><param name='display_spinner' value='yes' /><param name='display_overlay' value='yes' /><param name='display_count' value='yes' /><param name='language' value='en-US' /><param name='filter' value='publish=yes' /></object></div>                
<script type='text/javascript'>                    
  var divElement = document.getElementById('viz1775073921443');                    
  var vizElement = divElement.getElementsByTagName('object')[0];                    
  vizElement.style.width='100%';vizElement.style.height=(divElement.offsetWidth*0.75)+'px';                    
  var scriptElement = document.createElement('script');                    
  scriptElement.src = 'https://public.tableau.com/javascripts/api/viz_v1.js';                    
  vizElement.parentNode.insertBefore(scriptElement, vizElement);                
</script>

## References

Few, Stephen. "Data Visualization Effectiveness Profile," 2017.
http://www.perceptualedge.com/articles/visual_business_intelligence/data_visualization_effectiveness_profile.pdf

Pandey, Shashank A. "Which AI Models Hallucinate the Most?" Voronoi App, November 24, 2025.
https://www.voronoiapp.com/technology/Which-AI-Models-Hallucinate-the-Most-7211

Artificial Analysis. "Omniscience Index: Hallucination Rate." Artificial Analysis, 2025.
https://artificialanalysis.ai

## AI acknowledgements
I used Claude & Copilot to assist with this assignment in the following ways:

- Drafting the written content
- Providing critique feedback on the sketch 
- Suggesting design improvements across the three visualization drafts
- Formatting the final markdown, including the side-by-side HTML layout and Tableau embed code

All design decisions, scores in the Stephen Few critique, and visualization builds in Tableau were completed by me.
