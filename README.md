# Identifying Distinctive Terms in Presidential Papers Using TF*IDF
Isaac Wink and Brice Bowrey

## Use Case
The Public Papers of the Presidents of the United States series, published by the Federal Register, contains the official public communications, including speeches and written messages, of the US presidents. HTRC Analytics includes a workset of more than 650 volumes, from Hoover to Obama. The text of the papers provides an opportunity to identify historical trends in topics addressed by presidents and how those topics have changed over time. Educators may be interested in using visualizations of terms distinctive to a certain presidency to highlight for students what topics were relevant to that president, and historians may be interested in longer tables of distinctive terms to identify new areas of research.

## Description
We were interested in identifying the most distinctive terms associated with the papers of different presidents, defining “distinctiveness” as term frequency x inverse document frequency. Our theory is that looking for distinctive terms can help identify new issues covered in the papers that may have been a significant focus of a president but would not otherwise surface looking exclusively at term frequency. These issues could then be the start of new historical inquiries using traditional methods. 

Our code visualizes the most distinctive terms by volume in a wordcloud but also produces CSVs containing individual TF*IDF scores for more granular analysis. It unfortunately took a long time to run, so we made a couple sacrifices: Rather than work with the full workset of more than 650 volumes of presidential papers, we chose a subset of six from different administrations. Additionally, we had to limit TF*IDF calculations to 10,000 terms per volume. However, we hope to continue working on this project in the future and eventually be able to expand our analysis. 

While we were working specifically with presidential papers, we also tested our code with the Toni Morrison dataset and produced what appear to be meaningful results. 


## Tasks 
 * Wrote functions for retrieving individual volumes for testing, posting worksets, and retrieving aggregated volume features from worksets
 * Developed a corpus dataframe containing term frequencies for tokens by volume
 * Wrote functions to calculate TF*IDF scores
 * Calculated TF*IDF scores for a subset of tokens in six volumes of presidential papers from different presidents
 * Saved CSVs containing TF*IDF scores and visualized results in wordclouds showing most distinctive terms 

![pres_wordclouds](https://github.com/igwink/HTRC_Hackathon_Presidents/assets/35858990/02c6960c-c72c-4527-a98e-54d831a2cd28)

## Next Steps
 * Gain a stronger familiarity with the contents of the Public Papers of the Presidents of the United States series so we can interpret our results and understand potential limitations. 
 * Use LLM to tag volumes by presidential administration to be able to expand beyond our original six volumes
 * Optimize our code to reduce runtime
 * Use LLM tags to make programmatic comparisons of presidential administrations by identifying distinctive tokens in each “document”
 * Calculate individual TF*IDF scores for each volume to analyze change over time based on appearance and disappearance of distinctive words 
