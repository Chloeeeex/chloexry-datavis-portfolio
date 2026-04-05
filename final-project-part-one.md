| [Home Page](./) | [data viz examples](dataviz-examples) |[Goverment Debt](debt-gdp-analysis)| [critique by design](critique-by-design) | [final project I](final-project-part-one) | [final project II](final-project-part-two) | [final project III](final-project-part-three) |



# Outline
Every February, the Grammy Award for Album of the Year is treated as the definitive verdict on music. But a closer look at the data tells a different story. Over the past two decades, Grammy winners have repeatedly underperformed their nominated peers in streaming numbers, long-term popularity, and cultural staying power. The gap between what the Recording Academy rewards and what listeners actually embrace is not random. It reflects something more systematic about who votes, what they value, and which sounds get legitimized by the industry.    

This project uses data to explore that gap. By combining Grammy nomination and winner records with Spotify audio features and popularity metrics, I will examine whether the Album of the Year award reflects broader cultural impact, or whether the albums that resonate most with listeners tend to be the ones that lose. I will also use clustering and predictive modeling to investigate what kinds of albums Grammy voters have historically favored, and whether any patterns emerge in who gets overlooked.

**One sentence summary**
The Grammy Award for Album of the Year consistently overlooks the albums that actually shaped culture, revealing a disconnect between industry recognition and real-world impact.

As a reader, I want to recognize that award shows reflect insider taste rather than cultural truth, so that I can think more critically about how the music industry defines "the best." I can do this by looking beyond award wins when discovering music and paying attention to who got snubbed.
<img width="1229" height="597" alt="Screenshot 2026-04-05 at 5 06 03 PM" src="https://github.com/user-attachments/assets/0a2e0644-cce3-4d77-b1df-46ff6ed5cb40" />


## Initial sketches
![IMG_0631](https://github.com/user-attachments/assets/0717cae8-f485-4399-9f6f-6bee51a2af5f)
Section 2: "The winner isn't always the most popular"
Section 3(The pattern): "Average audio feature profile of all winners vs. all non-winners"(Radar chart) & "Cluster plot of all the nominated albums"
Section 5(Why it happens): "Feature importance from the predictive model. "


# The data
This project draws on two types of data: Grammy Award records and Spotify track-level audio and popularity data.

The Grammy dataset covers all nominees and winners from 1965 to 2024. From this, I will filter for the Album of the Year category and extract each year's nominees, the winner, and the associated artist and focus on the recent two decades. This gives me the foundation for comparing awarded albums against their nominated peers.

The Spotify data comes from two datasets. The first covers 114,000 tracks across 125 genres and includes both audio features (danceability, energy, valence, tempo, acousticness) and a popularity score from 0 to 100. The second extends coverage back to 1921 with over 600,000 tracks, which helps ensure that older Grammy nominees are represented. Since both datasets are track-level, I will aggregate tracks by album using Python to derive album-level popularity scores. The combined Spotify data will then be matched to Grammy nominees by artist name and album name, producing a merged dataset that supports both visualization in Tableau and downstream clustering and predictive modeling.
For those Grammy-nominated albums that cannot be matched in either Spotify dataset, I will manually retrievedata using the Spotify Web API or supplementary sources to ensure complete coverage across all years.

| Name | URL | Description |
|------|-----|-------------|
|Grammy Winners and Nominees 1965–2024|[Grammy dataser 1965-2024](https://www.kaggle.com/datasets/johnpendenque/grammy-winners-and-nominees-from-1965-to-2024)|All Grammy nominees and winners across categories from 1965 to 2024, used to extract Album of the Year nominees and winners|
|Spotify Tracks Dataset|[114,000 Spotify tracks](https://www.kaggle.com/datasets/maharshipandya/-spotify-tracks-dataset)|114,000 Spotify tracks with audio features and popularity scores across 125 genres|
|Spotify Dataset 1921–2020|[1921-2020 Spotify Tracks](https://www.kaggle.com/datasets/yamaerenay/spotify-dataset-19212020-600k-tracks)|600,000+ Spotify tracks from 1921 to 2020. Used to supplement coverage for older Grammy nominees not found in the first dataset|

# Method and medium
The project will be built using Shorthand as the primary storytelling platform, with data visualizations created in Tableau and embedded throughout the narrative. Data cleaning, merging, and analysis will be done in Python, including clustering and predictive modeling to identify patterns in Grammy voting. The final output will be an interactive, scrollable story published on Shorthand, with supporting code and datasets documented in a GitHub repository.

## References
Pendenque, J. (2024). Grammy winners and nominees 1965–2024 [Dataset]. Kaggle. https://www.kaggle.com/datasets/johnpendenque/grammy-winners-and-nominees-from-1965-to-2024   

Pandya, M. (2023). Spotify tracks dataset [Dataset]. Kaggle. https://www.kaggle.com/datasets/maharshipandya/-spotify-tracks-dataset   

Erenay, Y. (2020). Spotify dataset 1921–2020, 600k+ tracks [Dataset]. Kaggle. https://www.kaggle.com/datasets/yamaerenay/spotify-dataset-19212020-600k-tracks

## AI acknowledgements
Claude (Anthropic) was used. Specifically, it assisted with brainstorming and refining the project topic, drafting and editing the outline and high-level summary, structuring the story arc.
