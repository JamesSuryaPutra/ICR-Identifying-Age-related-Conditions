# Rock, Paper, Scissors

# Description
Rock, Paper, Scissors (sometimes called roshambo) has been a staple to settle playground disagreements or determine who gets to ride in the front seat on a road trip. The game is simple, with a balance of power. There are three options to choose from, each winning or losing to the other two. In a series of truly random games, each player would win, lose, and draw roughly one-third of games. But people are not truly random, which provides a fun opportunity for AI.

Studies have shown that a Rock, Paper, Scissors AI can consistently beat human opponents. With previous games as input, it studies patterns to understand a player’s tendencies. But what happens when we expand the simple “Best-of-3” game to be “Best-of-1000”? How well can artificial intelligence perform?

In this simulation competition, you will create an AI to play against others in many rounds of this classic game. Can you find patterns to make yours win more often than it loses? It’s possible to greatly outperform a random player when the matches involve non-random agents. A strong AI can consistently beat predictable AI.

This problem is fundamental to the fields of machine learning, artificial intelligence, and data compression. There are even potential applications in human psychology and hierarchical temporal memory. Warm up your hands and get ready to Rock, Paper, Scissors in this challenge.

# Evaluation
Each day, your team is able to submit up to 5 agents (bots) to the competition. Each submission will play episodes (games) against other bots on the ladder that have a similar skill rating. Over time, skill ratings will go up with wins or down with losses. Every bot submitted will continue to play games until the end of the competition. On the leaderboard, only your best scoring bot will be shown, but you can track the progress of all of your submissions on your Submissions page.

Each Submission has an estimated Skill Rating which is modeled by a Gaussian N(μ,σ2) where μ is the estimated skill and σ represents our uncertainty of that estimate which will decrease over time.

When you upload a Submission, we first play a Validation Episode where that Submission plays against copies of itself to make sure it works properly. If the Episode fails, the Submission is marked as Error. Otherwise, we initialize the Submission with μ0=600 and it joins the pool of All Submissions for ongoing evaluation.

We repeatedly run Episodes from the pool of All Submissions and try to pick Submissions with similar ratings for fair matches. We aim to run ~8 Episodes a day per Submission, with an additional slight rate increase for the newest-submitted Episodes to give you feedback faster.

After an Episode finishes, we'll update the Rating estimate for all Submissions in that Episode. If one Submission won, we'll increase its μ and decrease its opponent's μ; if the result was a draw, then we'll move the two μ values closer towards their mean. The updates will have magnitude relative to the deviation from the expected result based on the previous μ values and also relative to each Submission's uncertainty σ. We also reduce the σ terms relative to the amount of information gained by the result. The score by which your bot wins or loses an Episode does not affect the skill rating updates.

At the submission deadline, additional submissions will be locked. One additional week will be allotted to continue to run episodes. At the conclusion of this week, the leaderboard is final.
