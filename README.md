Photos

<img src="https://raw.githubusercontent.com/DanversKara/KarasPage/refs/heads/main/images/screenshots/mobile.png" alt="description" width="100%"/>

<img src="https://raw.githubusercontent.com/DanversKara/KarasPage/refs/heads/main/images/screenshots/desktop.png" alt="description" width="100%"/>

<img src="https://raw.githubusercontent.com/DanversKara/KarasPage/refs/heads/main/images/screenshots/desktop1.png" alt="description" width="100%"/>

if you wanna add backgrounds
Add this to your CSS (around line where you define .bg-glow):
css
/* ─── Custom Background Image ─── */
body {
  background-image: url('https://.com');
  background-size: cover;
  background-position: center;
  background-attachment: fixed;
  background-repeat: no-repeat;
}

/* Optional: Darken overlay to make text more readable */
body::before {
  content: '';
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.5); /* Adjust opacity as needed */
  pointer-events: none;
  z-index: 0;
}

/* Adjust existing bg-glow to work with new background */
.bg-glow {
  display: none; /* Hide the existing gradient glow since we have an image */
}
Alternative approach (keep both image and glow):
css
/* Keep both the image and subtle glow */
body {
  background-image: url('YOUR_IMAGE_URL_HERE');
  background-size: cover;
  background-position: center;
  background-attachment: fixed;
  background-repeat: no-repeat;
  position: relative;
}

.bg-glow {
  opacity: 0.3; /* Reduce opacity so image shows through */
  mix-blend-mode: overlay; /* Blend with the image */
}
Note: Make sure to replace 'YOUR_IMAGE_URL_HERE' with the actual URL you provided. The image will set a beautiful dark forest atmosphere that matches your page's dark theme perfectly!

