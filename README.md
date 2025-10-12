The Murders in the Rue Morgue: Deduction Game
A Twine project demonstrating conditional logic and hidden stat-tracking.

This document details a proof-of-concept visual novel (VN) adaptation of Edgar Allan Poe's classic short story, "The Murders in the Rue Morgue." This project was created specifically to practice transforming a linear narrative into a robust, non-linear, choice-driven game. It showcases the core implementation of branching narratives and hidden stat-tracking using the Twine engine, an essential skill for developing mystery and interactive fiction titles.

📖 Project Rationale and Gameplay
The Rue Morgue is used as a template to constrain the development focus purely to deduction mechanics, avoiding unnecessary external complications.

Player Role: You act as C. Auguste Dupin's assistant (the narrator). Your goal is to analyze the bizarre crime scene and witness testimony, making analytical choices that determine your proficiency.

Key Mechanics: Success relies on three hidden stats: Observation ($Obs), Logic ($Logic), and Interrogation ($Interro). Each choice you make awards points to one of these variables. The combined score of $Obs and $Logic is the crucial determinant for the True End. If your score meets the threshold (8 points), your final deduction is presented with "strong evidence," leading to the most satisfying conclusion. If insufficient, your correct guess is delivered with "low confidence," reflecting a lack of mastery.

▶️ Technical Execution
This draft was built in the Twine 2 application using the Harlowe 3.3.9 Story Format. The robust and often verbose conditional point allocation is handled by combining the (link:) and (go-to:) macros to guarantee action execution upon a click. The final branching logic is managed by explicit (if:)/(else:) checks.

To play, open the Rue Morgue Deduction.html file directly in any web browser.
