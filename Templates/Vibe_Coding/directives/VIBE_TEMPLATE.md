# VIBE SPEC: [Template Name]

## 1. The Goal (The Aesthetic)
Describe the feeling and visual impact of the UI.
- **Keywords:** [e.g., Sleek, Futuristic, Minimal, Vibrant]
- **Target Audience:** [Who is this for?]

## 2. Design System Tokens
- **Primary Color:** [e.g., #6366f1]
- **Surface Theme:** [e.g., Frosted Glass, Dark Mode with gradients]
- **Typography:** [e.g., Inter for UI, Playfair for headings]

## 3. Micro-Animations (Layer 3)
Define the motion design that makes it feel alive.
- `execution/gen_animations.js`: Controls hover and entrance effects.
- `execution/optimize_assets.py`: Ensures fast loading of high-vibe assets.

## 4. Visual Verification
- [ ] Correct shadow depths (Glassmorphism)
- [ ] Responsive breakout points valid
- [ ] Hover states provide clear feedback

## 5. Vibe Drift Check
Define what constitutes a "low-vibe" result and how to self-anneal.
