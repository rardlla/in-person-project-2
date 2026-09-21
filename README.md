# Week 4: Modern Layout Portfolio
## Transform Your Portfolio with Flexbox, Grid, and Responsive Design

### 🎯 Learning Objectives
By completing this project, you will:
- Master Flexbox for navigation bars, card layouts, and flexible components
- Command CSS Grid for complex page layouts and image galleries
- Implement responsive design patterns that adapt seamlessly across devices
- Choose the right tool (Flexbox vs Grid) for each layout challenge
- Create fluid layouts without relying heavily on media queries
- Build a professional portfolio that showcases modern CSS mastery

### 📚 Prerequisites
Before starting, you should have:
- Completed Week 4 lecture on Modern CSS Layouts
- Reviewed prep work chapters:
  - Chapter 7: Flexbox
  - Chapter 15: CSS Grid
  - Chapter 8: Responsive Design (optional but helpful)
- (Optional) Your code from the Week 3 project - Personal Profile Page

### 🏗️ Project Overview
You'll transform a basic portfolio website into a modern, responsive masterpiece using Flexbox and Grid. This isn't just about making things look pretty - you're implementing the exact layout techniques used by professional developers at companies like Google, Apple, and Netflix. Focus purely on CSS layouts - no JavaScript needed for this week!

### 🚀 Getting Started

**First:** Fork this template repository on GitHub into your own account (the Fork button, top right; keep it public, name it `in-person-project-2-<your-github-username>`). Your fork carries the Week 4 starter code.

1. **Clone your new repository:**
   ```bash
   git clone [your-fork-url]
   cd [your-repo-name]
   ```

2. **Choose your path:**

#### Option A: Continue from Week 3 (Recommended)
If you completed the Week 3 project and want to build upon it:

1. **Delete the starter files** in your cloned repository (but keep the .git folder)
2. **Copy your Week 3 files** into the cloned repository folder
3. **Replace the content** in your HTML with your personal information
4. We'll focus on transforming `style.css` with modern layout techniques

**Note:** Week 3 was a static HTML/CSS page. This week goes deeper into layout with Flexbox and Grid - no JavaScript needed yet (that starts next week).

#### Option B: Fresh Start
If starting fresh, use the provided starter files in your cloned repository:

1. **Use the existing starter files** (already in your cloned repository)
2. You'll find a complete portfolio with static HTML content
3. **Customize the content** - Replace "Alex Johnson" with your information
4. Focus on implementing the CSS layout enhancements
5. Open `index.html` in your browser to see your starting point

### 📝 Step-by-Step Instructions

#### Part 1: Navigation Bar with Flexbox (10 minutes)
Transform your navigation into a modern, responsive navbar using Flexbox.

**Step 1.1: Basic Flexbox Navigation**
In your `style.css`, update the navigation:

```css
#navbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1rem 2rem;
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    position: sticky;
    top: 0;
    z-index: 1000;
}

.nav-menu {
    display: flex;
    gap: 2rem;
    list-style: none;
    margin: 0;
    padding: 0;
}
```

What's happening here:
- `display: flex` on navbar creates a flex container
- `justify-content: space-between` spreads items horizontally
- `gap` property creates consistent spacing without margins

**Step 1.2: Add Logo/Brand Section**
```css
.nav-brand {
    display: flex;
    align-items: center;
    gap: 1rem;
    font-weight: bold;
    color: white;
}
```

Common mistakes to avoid:
- Forgetting to remove default list styles
- Not using `align-items` for vertical centering
- Using margins instead of gap for spacing

#### Part 2: Hero Section with Flexbox (10 minutes)
Create a stunning hero section that centers content perfectly.

**Step 2.1: Centered Hero Layout**
```css
.hero {
    min-height: 60vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    padding: 4rem 2rem;
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
}

.hero-content {
    max-width: 800px;
}
```

**Step 2.2: Hero Call-to-Action Buttons**
```css
.hero-buttons {
    display: flex;
    gap: 1rem;
    justify-content: center;
    flex-wrap: wrap;
    margin-top: 2rem;
}

.btn {
    padding: 0.75rem 2rem;
    border-radius: 50px;
    text-decoration: none;
    transition: transform 0.3s ease;
}

.btn:hover {
    transform: translateY(-2px);
}
```

What's happening here:
- `flex-wrap: wrap` ensures buttons stack on small screens
- Flexbox handles both horizontal and vertical centering effortlessly

#### Part 3: Skills Grid Layout (10 minutes)
Use CSS Grid to create a responsive skills showcase.

**Step 3.1: Grid Container Setup**
```css
.skills-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 2rem;
    padding: 2rem;
}

.skill-card {
    background: white;
    padding: 1.5rem;
    border-radius: 8px;
    box-shadow: 0 2px 10px rgba(0,0,0,0.1);
    transition: transform 0.3s ease;
}

.skill-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 5px 20px rgba(0,0,0,0.15);
}
```

What's happening here:
- `auto-fit` with `minmax()` creates truly responsive grids
- No media queries needed - the grid adapts automatically!

**Step 3.2: Skill Progress Bars**
```css
.skill-level {
    height: 8px;
    background: #e0e0e0;
    border-radius: 4px;
    overflow: hidden;
    margin-top: 0.5rem;
}

.skill-progress {
    height: 100%;
    background: linear-gradient(90deg, #667eea, #764ba2);
    width: var(--skill-level);
    transition: width 1s ease;
}
```

#### Part 4: Project Gallery with Grid (10 minutes)
Create a stunning project showcase using advanced Grid techniques.

**Step 4.1: Asymmetric Grid Layout**
```css
.projects-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 2rem;
    padding: 2rem;
}

/* Featured project spans multiple cells */
.project-card.featured {
    grid-column: span 2;
    grid-row: span 2;
}

.project-card {
    position: relative;
    overflow: hidden;
    border-radius: 12px;
    background: white;
    box-shadow: 0 4px 6px rgba(0,0,0,0.1);
}
```

**Step 4.2: Project Card with Flexbox Content**
```css
.project-content {
    display: flex;
    flex-direction: column;
    height: 100%;
    padding: 1.5rem;
}

.project-header {
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
    margin-bottom: 1rem;
}

.project-tags {
    display: flex;
    flex-wrap: wrap;
    gap: 0.5rem;
    margin-top: auto; /* Pushes tags to bottom */
}
```

What's happening here:
- Grid handles the overall layout
- Flexbox manages content within each card
- Combining both tools gives maximum flexibility

#### Part 5: Responsive Design Without Media Queries (5 minutes)
Modern CSS can be responsive without traditional breakpoints.

**Step 5.1: Fluid Typography**
```css
:root {
    font-size: clamp(14px, 2vw, 18px);
}

h1 {
    font-size: clamp(2rem, 5vw, 4rem);
}

h2 {
    font-size: clamp(1.5rem, 4vw, 2.5rem);
}
```

**Step 5.2: Container Queries (Bonus - Advanced)**
```css
.card-container {
    container-type: inline-size;
}

@container (min-width: 400px) {
    .card {
        display: grid;
        grid-template-columns: 150px 1fr;
    }
}
```

### 🎨 Customization Ideas
1. **Color Themes**: Create CSS custom properties for easy theme switching
2. **Animation**: Add scroll-triggered animations to sections
3. **Dark Mode**: Implement a dark mode toggle with CSS variables
4. **Grid Art**: Create decorative grid patterns in the background
5. **Flexbox Navigation**: Add a mobile hamburger menu with pure CSS

### 🏆 Challenge Extensions

#### Intermediate: Masonry Layout
Create a Pinterest-style masonry layout for projects:
```css
.masonry {
    columns: 300px auto;
    column-gap: 1rem;
}
```

#### Advanced: CSS Grid Areas
Use named grid areas for complex layouts:
```css
.page-layout {
    display: grid;
    grid-template-areas:
        "header header header"
        "sidebar main aside"
        "footer footer footer";
}
```

#### Graduate (253A): Responsive Without Any Media Queries
Build the entire layout using only modern CSS features:
- Clamp() for fluid sizing
- Grid auto-fit/auto-fill
- Aspect-ratio for images
- Container queries

### 🐛 Troubleshooting Guide

**Issue: Flexbox items not centering**
- Solution: Check that you're using both `justify-content` and `align-items`
- Remember: justify = main axis, align = cross axis

**Issue: Grid items overflowing**
- Solution: Add `min-width: 0` to grid items
- Use `minmax()` in grid-template-columns

**Issue: Sticky navigation not working**
- Solution: Ensure parent containers don't have `overflow: hidden`
- Add appropriate `z-index` to stay above content

**Issue: Gap property not working**
- Solution: Gap works in both Flexbox and Grid (modern browsers)
- Fallback: Use margins for older browser support

### 📖 Resources & References
- [CSS-Tricks Flexbox Guide](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
- [CSS-Tricks Grid Guide](https://css-tricks.com/snippets/css/complete-guide-grid/)
- [MDN Flexbox](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout)
- [MDN CSS Grid](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Grid_Layout)
- [Grid Garden Game](https://cssgridgarden.com/)
- [Flexbox Froggy Game](https://flexboxfroggy.com/)

### ✅ Project Checklist
- [ ] Navigation uses Flexbox for responsive layout
- [ ] Hero section centers content with Flexbox
- [ ] Skills section uses CSS Grid with auto-fit
- [ ] Projects showcase combines Grid and Flexbox
- [ ] At least one section works without media queries
- [ ] Layout is responsive across all screen sizes
- [ ] Code includes helpful comments
- [ ] Visual hierarchy is clear and professional
- [ ] Hover states and transitions enhance UX
- [ ] Layout degrades gracefully on older browsers

### 💡 Final Tips
- Start with mobile layout, enhance for larger screens
- Use Grid for 2D layouts, Flexbox for 1D layouts
- Test in DevTools device mode frequently
- Keep accessibility in mind - layouts should be keyboard navigable
- Performance matters - avoid overly complex nested grids

Remember: Modern CSS layouts aren't just about making things look good - they're about creating maintainable, scalable, and accessible interfaces. Every technique you learn here is used in production at major tech companies!