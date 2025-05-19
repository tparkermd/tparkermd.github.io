# Management

- Weekly 1:1s (as desired - this is your time!)
- Values and career goals alignment when we start working together
- Common 1:1 topics
    - What do you do well overall?
    - What have you done well here?
    - What do you like to do?
    - What do you want to do/learn more?
    - What is your understanding of your current level?
    - What is your understanding of the next level?
    - What is your understanding of the delta between the two?
    - What are the actions you want to take to get to that level?
    - How do you feel you have grown towards your goals in the last (week|month|year)?
    - What did you learn this week?
- You are welcome to funnel all questions and feedback through me, although this is a good skill to develop as you grow in your career.
    - This is a skill we can work together to develop.
- If your performance review is ever a surprise to you, something has gone awry in my communication to you on your progress in the last 6 months.
- I highly recommend keeping a brag doc, which we can review and maintain together.

# Tech Leading

- I try to avoid taking the most time-sensitive work because my time is not a guarantee.
- I am happy to set up weekly pairing time as desired.
- I will review all MRs but my review is not necessarily blocking. I will follow up if I have any retroactive concerns.
- No stakeholders beyond our team should be pinging you directly. Nudge them either my way or our PM’s way for updates, prioritization, or requests.
- I am not the sole owner of our roadmap! Please add any ideas more than one ticket to our [Technical Roadmap](https://docs.google.com/spreadsheets/d/1FD7Ohsjdn1Zcyky1A8bvMaZMpGlxBSPQ3_7NAA1hALE/edit?usp=sharing) and single ticket items to our Engineering Backlog.
- Team Agreements:
    - Comments should be avoided. All code should be readable like a book via variable names, function names, etc. Comments are often forgotten or ignored during code updates and can become outdated. This rarely, if ever, happens with variable names.
        - Example of what this can look like:
        
        ```jsx
        // check if we are looking at the sky and it is blue
        if (eyeTarget.destination === "sky" && eyeTarget.color === "blue")
        ```
        
        versus
        
        ```jsx
        const isLookingAtBlueSky = eyeTarget.destination === "sky" && eyeTarget.color === "blue";
        if (isLookingAtBlueSky)
        ```
        
        - Exceptions to this rule are things like complex utility functions, code decisions that are not immediately intuitive to the reader, or TODO comments ***with a ticket URL**.*
    - Only one ticket should be in progress at one time. If more than one ticket is in progress, your focus is being split and something is wrong with our prioritization process.
        - Occasionally there is a ticket that is “on your radar” but requires monitoring or communication over the course of a few days. *Ideally* the ticket could be put into `Hold` but this can be an exception to the rule.
    - All MRs should have an associated ticket. All tickets should have a description.
        - Pretend you are an engineer looking at this code 5-10 years from now. Would you feel like you have enough context on why something was done without a well defined ticket in the commit message?
    - Similarly, all decisions that change the outcome of a ticket should be communicated on the ticket. Links to Slack messages are not enough.
    - I fully believe in following the [Boy Scout Rule](https://deviq.com/principles/boy-scout-rule) when possible. However, be mindful that following the Boy Scout Rule doesn’t impede you from shipping. Remember that all code you write or change in an MR is fair game for review!
        - If you determine something should be improved but it is far beyond the scope of your ticket, this should be ticketed out and put into the engineering backlog.
    - No extracurricular work - if you’re working on something it should be in the Sprint. This helps me protect your time and avoids burnout from being pulled multiple directions.
        - If you are specifically collaborating with another team, add a placeholder in the Sprint so we can make sure we are planning for your time allocation to that ticket.
    - Tickets should be kept in the most up-to-date status on the Sprint board. This makes it easy for me to relay to stakeholders the status of our Sprint.
    - **Think hard before you persist anything to a database.** The moment something is stored is the moment we have committed to a future migration.
