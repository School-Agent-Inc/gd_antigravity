# Antigravity Task List: Adaptive Lesson Package (Modern Japanese Explanatory Text)

This task list is designed for Antigravity to generate a complete "Adaptive Lesson Package" based on the "Modern Japanese Explanatory Text" unit.

## 1. Documentation & Intent Analysis
- [ ] Read and analyze the following files to understand the pedagogical context:
    - [[教育-認知オンロードと授業デザイン]]
    - [[現代文評論文読解]]
- [ ] Identify the specific "Gap/Dissonance" (齟齬) to be highlighted for this lesson.

## 2. Content Generation (Sourcing/Gemini)
- [ ] **Generate Socratic Interaction Prompts (GEM Setting):**
    - Create a system prompt for a "Socratic GEM" that guides students through analyzing the text without giving away answers.
    - Focus on eliciting the "Why do you feel this way?" from the student.
- [ ] **Create Comparative Material:**
    - Generate two high-quality but distinct sample answers for a central question in the unit.
    - One should focus on a "subjective/experiential" perspective.
    - The other should focus on a "text-based/structural" perspective.

## 3. Implementation (Web-based Interface)
- [ ] **Develop an Interactive Worksheet (HTML/JS):**
    - Feature a "Comparison Slider" or similar UI for the two sample answers.
    - Include a reflection log area that stores student "Dissonance" notes.
    - Ensure the UI feels premium (glassmorphism, smooth transitions).

## 4. Verification & Output
- [ ] **Automated Verification:**
    - Use the integrated browser to test the worksheet's interactivity.
    - Verify that the reflection log correctly captures input.
- [ ] **Final Artifact Generation:**
    - Produce a `walkthrough.md` explaining the design choices (why these specific samples were chosen to create "cognitive onloading").
