# Frontend Mentor - Social links profile solution

This is a solution to the [Social links profile challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/social-links-profile-UG32l9m6dQ).

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [AI Collaboration](#ai-collaboration)
  - [Continued development](#continued-development)
- [Author](#author)

## Overview

### The challenge

Users should be able to:

- See hover and focus states for all interactive elements on the page.

### Screenshot

![Croquis](./assets/images/tada%20local-remote.png)

### Links

- Solution URL: [https://github.com/ezra1492/frontend-mentor-social-links](https://github.com/ezra1492/frontend-mentor-social-links)
- Live Site URL: [https://ezra1492.github.io/social-links-profile/](https://ezra1492.github.io/social-links-profile/) [3]

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties (Design Token Vault)
- Flexbox (Magnetic Containment)
- Mobile-first workflow
- BEM Methodology (Block-Element-Modifier)

### What I learned

During this project, I refined the architectural foundations of my CSS and interaction logic.

#### 1. Layered Spacing: Primitives and Semantics

I perfected the use of **Primitive spacing** as a "tape measure" or a _tatami_ mat (the base unit). **Semantic spacing** represents functional roles—the width of a door, the height of a window, or the dimensions of a room.

- A small study (3 tatamis).
- A tea room (4.5 tatamis).
- A living room (8 tatamis).
  By tying all semantic roles to primitive measures, systemic maintenance becomes effortless.

```css
:root {
  /* Primitive: The raw unit */
  --sp-100: 0.5rem;
  /* Semantic: The functional role */
  --br-btn: var(--sp-100);
}
```

![Design Token Vault](assets/images/Desig%20Token%20Vault%20+%20rule%20body-card.png)

#### 2. Layout Dynamics: Block-level Links

I reinforced my understanding of element behavior within the box model.
**Lists:** To remove bullet points from an unordered list, the `list-style-type` property must be assigned directly to the `ul` element.
**Gas Expansion:** Links are inline by default and lack the "ceiling" and "walls" required to exert force. By converting them to `display: block`, they expand to fill the parent container's width like a gas, creating a robust, predictable hit area.

```css
.social-card__links {
  display: flex;
  flex-direction: column;
  gap: var(--sp-200);
  list-style-type: var(--lst-ul); /* remove bullet points */
}

.social-card__btn {
  display: block;
  padding: var(--pd-btn);
  font-size: var(--fs-14);
  font-weight: var(--fw-600);
  background-color: var(--clr-grey-700);
  color: var(--clr-white);
  border-radius: var(--br-btn);
  text-decoration: var(--td-btn);
}
```

![Block-level anchor](assets/images/rule%20btn.png)

#### 3. Asymmetric Interaction Timing

I implemented a professional "hydraulic" interaction feel.
**The Entry:** A snappy, immediate transition is assigned to the `:hover` and `:focus-visible` states.
**The Exit**: A slower, elegant return transition is assigned to the base rule (the "mother rule"), ensuring a smooth fade-out when the interaction ends.

```css
.social-card__btn {
  transition: all 0.5s ease-in-out; /* The slow Exit */
}

.social-card__btn:hover {
  transition: all 0.1s ease-out; /* The snappy Entry */
}
```

![Asymetric transition](assets/images/Hover%20figma-live%20preview.gif)

### Continued development

In future projects, I intend to refine my command of the following areas:

- **Flexbox Mastery:** While I have established a solid foundation in "Magnetic Containment" and viewport orchestration, I want to further explore complex alignment patterns and flexible layouts to ensure total control over responsive designs.
- **Advanced List Properties:** I plan to dive deeper into the varied properties of list containers and items, particularly regarding how they interact with accessibility markers and unconventional layout structures.
- **Dynamic Interaction & Transitions:** Building on my work with asymmetric timing, I aim to perfect my use of transitions and animations to create more sophisticated and tactile user experiences.

### AI Collaboration

I leveraged an iterative feedback loop from my previous Frontend Mentor projects (QR Code, Blog Preview, and NFT Preview) to engineer a high-fidelity **Context Prompt** using NotebookLM. This prompt established a professional architectural framework for this challenge.

- **Methodology:** We strictly followed an **"Outside-In Property Sort Rule"** (Layout → Box Model → Typography → Visuals) to maintain a clean and predictable CSS structure.
- **Evolution of Workflow:** In earlier projects, my focus was primarily on the mechanics of HTML/CSS. Now I'm prioritizing **Conventional and Atomic Commits** to track architectural movements. The integration of **Gitmojis** has been instrumental in making the repository's history legible and intent-driven.
- **Documentation:** I continue to utilize "swimming pool lanes" (systemic comment blocks) within the CSS. These serve as architectural reminders of _why_ specific semantic tags or property declarations were chosen, ensuring the code remains self-documenting and resilient.
- **Technical Audits:** The AI performed rigorous stress-tests on my "Design Token Vault" (Primitive vs. Semantic abstractions) and validated BEM (Block-Element-Modifier) naming conventions to prevent selector leakage.

## Author

- Frontend Mentor - [@ezra1492](https://github.com/ezra1492)
- X / Twitter - [@RayG1492](https://x.com/RayG1492)
- Discord - `rayg._86220`
