
To integrate PWA functionality into your site:
1. Upload manifest.json and service-worker.js to your web root.
2. Add these lines in the <head> of your HTML pages:
   <link rel="manifest" href="/manifest.json">
   <script>
     if ('serviceWorker' in navigator) {
       window.addEventListener('load', () => {
         navigator.serviceWorker.register('/service-worker.js');
       });
     }
   </script>
3. Provide icons in /icons (192x192 and 512x512 PNG).
4. Your site will now be installable as "VibeCheck" on Android and supported browsers.
