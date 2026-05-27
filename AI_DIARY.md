AI Tools Used:
ChatGPT, Gemini, and Claude: These AI tools were used collaboratively throughout the project. ChatGPT was primarily used for brainstorming the game logic and debugging syntax errors. Gemini was used for structural planning, refining the OOP approach, and optimizing the game loop. Claude was consulted for writing clean, maintainable CSS and improving the readability of the JavaScript code. Using a combination of these tools allowed me to cross-verify the logic and ensure the code met all project requirements.

Development Log:
[2026-05-25] - Initial Architecture Planning
What I asked the AI: "How can I structure a 'Sweet Catch' game using vanilla JavaScript and an OOP approach without using any external frameworks?"
What it gave me: A class-based structure with Game, Basket, and Item entities, along with a spawnLoop() logic.
What was wrong: The AI initially suggested mixing requestAnimationFrame and setTimeout in a way that caused visual stuttering for the falling items.
How I fixed it: I refactored the logic to use requestAnimationFrame solely for the rendering loop, keeping setTimeout only for the item spawning interval (800ms) to ensure smooth performance.
Time lost: ~40 minutes

[2026-05-26] - Collision Detection Logic
What I asked the AI: "Provide a simple AABB (Axis-Aligned Bounding Box) function to detect when the basket catches an item."
What it gave me: A collides(a, b) function comparing X and Y coordinates.
What was wrong: The items were triggering "collision" even when passing just near the basket due to incorrect offset calculations.
How I fixed it: I implemented getBoundingClientRect() to get precise coordinates of the DOM elements relative to the viewport, which accurately aligned the collision detection.
Time lost: ~20 minutes

[2026-05-26] - Handling Chrome's Autoplay Policy
What I asked the AI: "Why is my background music not playing automatically on load?"
What it gave me: An explanation about the browser's Autoplay Policy and a suggestion to use a user-initiated event.
What was wrong: The AI provided the technical reason but didn't suggest a user-friendly way to ask for that interaction.
How I fixed it: I designed a "sound-note-box" overlay on the start screen that prompts the user to click to "unleash the beats," which then triggers the audio.play() function.
Time lost: ~30 minutes

[2026-05-27] - CSS Animation Reset Bug
What I asked the AI: "How do I make the pepper flash effect trigger every time a pepper is caught?"
What it gave me: A CSS class addition via JavaScript (classList.add('pepper-flash')).
What was wrong: The animation worked only the first time. Subsequent triggers didn't animate because the class was already present.
How I fixed it: I used the void element.offsetWidth technique to force a reflow, allowing the browser to re-trigger the CSS animation every time the class is added.
Time lost: ~25 minutes

[2026-05-27] - LocalStorage High Score Logic
What I asked the AI: "How can I save the best score permanently so it stays after refreshing the page?"
What it gave me: Basic localStorage.setItem('score', score) logic.
What was wrong: It was overwriting the high score with the current score even if the current score was lower.
How I fixed it: I added an if (score > highScore) condition to ensure the localStorage is only updated when a new record is achieved.
Time lost: ~15 minutes