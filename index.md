Here is a complete, production-ready solution for Assignment 9.2 — Responsive Typography & Images.

This solution uses fluid typography with clamp(), flexible container constraints (max-width), fluid images (max-width: 100%, height: auto), and optimal line length (ch units) for supreme readability across mobile and desktop devices.

HTML Structure (index.html)
HTML
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>The Art of Slow Photography — Responsive Article</title>
  <link rel="stylesheet" href="style.css">
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&family=Merriweather:ital,wght@0,300;0,400;0,700;1,300&display=swap" rel="stylesheet">
</head>
<body>

  <!-- Step 5: Content Container with Optimal Max-Width -->
  <main class="article-container">
    
    <!-- Article Header -->
    <header class="article-header">
      <h1>The Art of Slow Photography in a Fast-Paced Digital World</h1>
      <p class="subtitle">Why stepping back from rapid shutter clicks can transform how you see and capture the world around you.</p>
      <div class="author-meta">
        <span>By Ananya Verma</span>
        <span>•</span>
        <time datetime="2026-06-15">June 15, 2026</time>
      </div>
    </header>

    <!-- Article Body Content -->
    <div class="article-body">
      <p>
        In an era where smartphones are always within arm's reach and millions of images are uploaded every single second, the sheer volume of visual media can feel overwhelming. We capture moments instantly, often before we've even had a chance to truly experience them. But what happens when we slow down?
      </p>

      <h2>The Shift from Quantity to Intention</h2>
      <p>
        Slow photography isn't strictly about using vintage film cameras or heavy mechanical gear. Instead, it represents a mindset—a deliberate choice to pause, observe lighting, study framing, and wait for the right alignment of elements before pressing the shutter button.
      </p>

      <!-- Step 2 & 4: Responsive Figure & Image -->
      <figure class="article-figure">
        <img src="https://images.unsplash.com/photo-1516035069371-29a1b244cc32?auto=format&fit=crop&w=1200&q=80" alt="Vintage film camera resting on a wooden table with soft natural light">
        <figcaption>A deliberate approach to framing shifts focus from speed to substance.</figcaption>
      </figure>

      <p>
        When you limit yourself to just a few frames during an outing, your psychological relationship with the environment changes completely. You begin noticing subtle details you would otherwise miss while scanning through a digital viewfinder on burst mode.
      </p>

      <h2>Practical Steps to Slow Down</h2>
      <p>
        Practicing intentional composition requires discipline. Here are a few simple ways to incorporate this into your routine:
      </p>

      <ul>
        <li><strong>Leave the zoom at home:</strong> Take a single prime lens or walk with your smartphone's native wide lens to force your feet to do the zooming.</li>
        <li><strong>Wait for the light:</strong> Spend ten minutes watching how sunlight shifts across a subject before taking your first shot.</li>
        <li><strong>Put the camera away:</strong> Spend half your walk without looking through a screen at all.</li>
      </ul>

      <!-- Secondary Responsive Image -->
      <figure class="article-figure">
        <img src="https://images.unsplash.com/photo-1500648767791-00dcc994a43e?auto=format&fit=crop&w=1200&q=80" alt="Detailed portrait in natural shadow lighting">
        <figcaption>Patience reveals depth in everyday subjects.</figcaption>
      </figure>

      <p>
        Ultimately, photography is less about the hardware in your hand and more about the presence of your mind. By slowing down, you create images that carry authentic emotional resonance rather than just digital clutter.
      </p>
    </div>

    <!-- Article Footer -->
    <footer class="article-footer">
      <p>&copy; 2026 Ananya Verma. All rights reserved.</p>
    </footer>

  </main>

</body>
</html>
CSS Styles (style.css)
CSS
/* Reset & Base Styles */
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: 'Inter', sans-serif;
  background-color: #fafaf9;
  color: #1c1917;
  line-height: 1.6;
  overflow-x: hidden;
}

/* Step 5: Container with Optimal Max-Width for Readability */
.article-container {
  width: 100%;
  max-width: 740px; /* Ideal line length control */
  margin: 0 auto;
  padding: 2rem 1.25rem;
}

/* Step 3: Fluid Typography using clamp() and rem */
html {
  font-size: 100%; /* Base 16px */
}

.article-header {
  margin-bottom: 2.5rem;
  padding-bottom: 1.5rem;
  border-bottom: 1px solid #e7e5e4;
}

.article-header h1 {
  font-family: 'Merriweather', serif;
  font-size: clamp(1.8rem, 4vw, 2.75rem); /* Fluid responsive heading */
  font-weight: 700;
  line-height: 1.25;
  color: #0c0a09;
  margin-bottom: 1rem;
}

.subtitle {
  font-size: clamp(1rem, 1.5vw, 1.2rem);
  color: #57534e;
  line-height: 1.5;
  margin-bottom: 1rem;
}

.author-meta {
  font-size: 0.875rem;
  color: #78716c;
  display: flex;
  gap: 0.5rem;
  align-items: center;
}

/* Step 6: Typography spacing and line length for body copy */
.article-body {
  font-family: 'Merriweather', serif;
  font-size: 1.05rem;
  color: #292524;
  line-height: 1.8; /* Generous line height for comfortable reading */
}

.article-body p {
  margin-bottom: 1.5rem;
  max-width: 65ch; /* Optimal line length (characters per line) */
}

.article-body h2 {
  font-family: 'Inter', sans-serif;
  font-size: clamp(1.3rem, 2.5vw, 1.65rem);
  font-weight: 600;
  color: #0c0a09;
  margin: 2.5rem 0 1rem 0;
}

.article-body ul {
  margin: 1.5rem 0 1.5rem 1.5rem;
  max-width: 65ch;
}

.article-body li {
  margin-bottom: 0.75rem;
}

/* Step 4: Responsive Images (Prevent Stretching & Overflow) */
.article-figure {
  margin: 2rem 0;
  width: 100%;
}

.article-figure img {
  width: 100%;          /* Forces image to scale down to container width */
  max-width: 100%;      /* Never exceeds container bounds */
  height: auto;         /* Maintains natural aspect ratio without distortion */
  display: block;       /* Removes baseline gaps */
  border-radius: 8px;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
}

.article-figure figcaption {
  font-family: 'Inter', sans-serif;
  font-size: 0.85rem;
  color: #78716c;
  text-align: center;
  margin-top: 0.75rem;
}

/* Article Footer */
.article-footer {
  margin-top: 4rem;
  padding-top: 1.5rem;
  border-top: 1px solid #e7e5e4;
  font-family: 'Inter', sans-serif;
  font-size: 0.85rem;
  color: #78716c;
  text-align: center;
}

/* Responsive adjustments for larger viewports */
@media (min-width: 768px) {
  .article-container {
    padding: 3.5rem 2rem;
  }
}
Step 7: Verification & Testing
No Horizontal Overflow: Shrink your browser window down to iPhone/Mobile size (320px–375px wide); notice that text wraps cleanly within the container and no horizontal scrollbar appears.

No Image Distortion: Inspect the images across mobile and desktop viewports; max-width: 100% and height: auto ensure images scale smoothly without getting squished or stretched.

Typography Scaling: Headings adjust smoothly using clamp() while body paragraphs maintain optimal line lengths (~65ch).

Want me to explain how CSS clamp() works for fluid typography across breakpoints?

Yes