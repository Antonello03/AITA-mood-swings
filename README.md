# r/AmITheAsshole Analysis Project
This is the repository for the AITA Subreddit Exploration & Web and Social Media Analysis project being developed by Antonello Di Rita, Alessandro Longato, Emirhan Kayar, for the Web and Social Networks course final year of the Bachelor of Science in Artificial Intelligence (a.y. 2024/2025).

## Overview
This research project analyzes the subreddit [r/AmITheAsshole](https://www.reddit.com/r/AmITheAsshole) to understand user interaction patterns, sentiment dynamics and temporal events. There exists seven different tags in this sub, however, our research team only examine posts judged as "YTA" (You're the Asshole) versus "NTA" (Not the Asshole).   

## Data
The main dataset consists of 500 posts (250 tagged "YTA" and 250 tagged "NTA") retrieved using [Reddit-API](https://developers.reddit.com/docs/api)'s top search algorithm, ensuring high engagement. Each post includes attributes such as submission ID, author, tag, timestamp, upvote ratio, score, title, body text, and number of comments. We filtered the data to include only posts from 2019 to 2023.

The comments dataset extends this by including comments up to three levels deep. For sentiment analysis, reply relationships were discarded. Each comment record contains the year, depth level, text, author, and the parent post’s tag (YTA/NTA).

The reply graph dataset was built from a random subset of 40 posts (20 YTA, 20 NTA) for which we collected complete comment trees. This dataset retains comment IDs and authors to reconstruct reply chains.

The user-interaction graph dataset includes data from all 450 posts. We focused on interactions beyond the first level (excluding OP to top-level comments) to emphasize community dynamics. For each reply (responder to original commenter), we recorded the comment score, any vote tags (YTA/NTA), and the usernames. Multiple interactions between user pairs were aggregated into weighted edges. Upvotes per user were summed to identify highly appreciated commenters. We also computed a vote tendency metric for each user: Vote Tendency = (Total YTA votes) − (Total NTA votes).



