# PerplexityVoiceModeCaseStudy
PerplexityVoiceMode-Limitation
# Perplexity AI Voice Mode Enhancement Case Study

This project analyzes a user experience limitation in Perplexity AI’s voice-to-voice mode and proposes a solution to improve efficiency and engagement. Based on my personal usage, I identified that archived voice conversations cannot be resumed in voice mode, forcing users to type or restart, which disrupts flow. I propose adding a “Resume in Voice Mode” button to seamlessly continue conversations.

## Problem Statement
As a frequent user of Perplexity AI’s voice-to-voice mode, I encountered a limitation: after a voice conversation ends and is archived in the library, I cannot resume it in voice mode—I’m forced to use text input. This disrupts my conversational flow, creates frustration, and decreases engagement over time. For example, if a new question arises later, I either spend extra time typing (which takes longer than speaking) or restart a new voice conversation, requiring me to re-explain the context.

## Impact Analysis
Perplexity AI users spend an average of 6 minutes and 25 seconds (385 seconds) per session, primarily in text mode (source: [Perplexity AI via X, 2025]). Voice mode, designed for faster conversational use, likely takes less time per interaction, but specific voice vs. text data isn’t available. When forced to resume an archived voice conversation via text, I estimate it takes me 90 seconds to type a follow-up question, compared to 20 seconds speaking—a 350% increase in interaction time. If 10% of voice users (e.g., 100,000 users) face this issue daily, this inefficiency could waste significant time, reducing user satisfaction and app engagement.

### Mock Data Analysis
If I had access to Perplexity’s user data, I’d run this SQL query to compare session times for voice vs. text interactions:
```sql
SELECT mode, AVG(interaction_time) as avg_time, COUNT(sessions) as session_count
FROM user_interactions
WHERE resumed = 'yes'
GROUP BY mode;
