### A very simple Arc boost that simply redirects all youtube links to piped.video.

#### Insert this JS into the boost:

```
// ==UserScript==
// @name         YouTube to piped.video Redirector
// @version      0.1
// @description  Redirect YouTube links to piped.video
// @author       Pasithea0
// @match        https://www.youtube.com/*
// @grant        none
// ==/UserScript==

(function() {
    'use strict';

    // Check if the current URL is a YouTube video
    if (window.location.hostname === "www.youtube.com" && window.location.pathname === "/watch") {
        // Get the video ID from the URL
        const videoID = new URLSearchParams(window.location.search).get("v");
        
        // Redirect to piped.video with the same video ID
        const pipedVideoURL = "https://piped.video/v/" + videoID;
        window.location.href = pipedVideoURL;
    }
})();
```
