Mission Master PWA — files and setup

IMPORTANT: mm.html is copied byte-for-byte from the original uploaded file. Its code was not edited.

Files:
- index.html: PWA wrapper. It opens mm.html inside a full-screen iframe so the original HTML remains unchanged.
- mm.html: your original application code, unchanged.
- manifest.webmanifest: install name, display mode, colors, and icon declarations.
- service-worker.js: caches the app shell for offline reopening.
- icons/: PWA icons at 192x192 and 512x512.

To install as a PWA:
1. Upload all files and the icons folder together to the SAME folder on an HTTPS host (or test on localhost).
2. Open the hosted index.html in Chrome on Android.
3. Use Chrome menu > Install app / Add to Home screen.

Opening the files directly with file:// will not enable PWA installation; service workers require HTTPS or localhost.

Offline note: the app shell and mm.html are cached. The original page loads Font Awesome and the Cairo font from external CDNs, so those external fonts/icons may not be available offline unless they were already cached by the browser. The original code has intentionally not been modified.
