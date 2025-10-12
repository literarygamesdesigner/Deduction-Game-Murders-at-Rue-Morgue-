# Deduction Game: Murders at Rue Morgue
Solve the impossible locked-room mystery of Rue Morgue. A choice-driven visual novel proving deduction skills are key.  Based on Edgar A Poe's story.


A Twine project demonstrating conditional logic and stat-tracking in interactive fiction.

This project adapts "The Murders in the Rue Morgue" to practice implementing branching narratives based on player choices and hidden analytical skills. It serves as a proof-of-concept for creating mystery VNs.

📖 About This Game
Project Goal: To transform a linear mystery story into an interactive, choice-driven experience where the player's deduction skills influence the outcome.

Player Role: You take on the role of C. Auguste Dupin's unnamed companion (the narrator). Your task is to analyze evidence and witness testimony alongside Dupin.

Key Game Mechanics
This VN uses a hidden stat-tracking system to determine the quality of your conclusion:

Hidden Stat

How It's Used

Observation ($Obs)

Gained by focusing on physical clues (e.g., the tuft of hair).

Logic ($Logic)

Gained by focusing on deductive truths (e.g., the untouched money).

Interrogation ($Interro)

Gained by analyzing witness voices and testimony.

Branching Fork: The player's accumulated score in $Obs + $Logic determines whether they have the "strong evidence" needed to successfully convince Dupin of the shocking truth in Scene 3.



▶️ How to Play
This game is self-contained within the HTML file.

Direct Access: Open the file named Rue Morgue Deduction VN.html directly in any web browser (Chrome, Firefox, Edge, etc.).

Gameplay: Click the underlined text options to advance the story and make choices.

🛠️ Technical Details (For Developers)
This draft was built using the Twine 2 application with the Harlowe 3.3.9 Story Format.

The core mechanics rely on the explicit use of the (link:) and (go-to:) macros to ensure actions are executed conditionally:

(link: "Clue Choice")[
    (set: $Obs to $Obs + 5)
    (go-to: "Next Scene")
]



The final branching logic uses a reliable (if:) / (else:) block to check the cumulative score against a threshold (8 points):

(if: $Logic + $Obs >= 8)[
    (link: "Strong Evidence Choice")...
]
(else:)[
    (link: "Low Confidence Choice")...
]



Note: This file is a developmental proof-of-concept and does not contain all art assets, sound, or final polish.
