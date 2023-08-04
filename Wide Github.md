## Wide Github
###Makes most of Github fill your whole screen!

#### Add CSS and JS to your boost

CSS:
```
@-moz-document regexp("^https://(?:gist\\.)?github\\.com/.*") {

  body:not(.wgh-disabled) .application-main .container {
    width: auto !important;
    padding-left: 16px !important;
    padding-right: 16px !important;
    margin-left: 0px !important;
    min-width: 980px;
  }
  body:not(.wgh-disabled) .application-main .container-lg,
  body:not(.wgh-disabled) .footer.container-lg {
    max-width: none !important;
    margin-left: 0px !important;
  }

  /* New github design */
  body:not(.wgh-disabled) .application-main .container-xl {
    max-width: none !important;
  }

  /* Floating PR toolbar */
  body:not(.wgh-disabled) .pr-toolbar {
    margin-left: -16px !important;
    margin-right: -16px !important;
    padding-left: 16px !important;
    padding-right: 16px !important;
  }

  /* Repository Issues */
  body:not(.wgh-disabled) #js-repo-pjax-container .discussion-timeline {  /* Issue body */
    width: 100% !important;
  }
  body:not(.wgh-disabled) #js-repo-pjax-container .timeline-new-comment { /* New Issue / issue comment form */
    max-width: 100% !important;
  }
  body:not(.wgh-disabled) #js-repo-pjax-container .new-discussion-timeline .files-bucket > div { /* New PR code diff */
    width: inherit !important;
    left: auto !important;
    right: auto !important;
    margin-left: 0px !important;
    margin-right: 0px !important;
    padding-left: 0px !important;
    padding-right: 0px !important;
  }
  body:not(.wgh-disabled) #js-repo-pjax-container .inline-comments .comment-holder, /* Diff / code comments */
  body:not(.wgh-disabled) #js-repo-pjax-container .inline-comments .inline-comment-form-container,
  body:not(.wgh-disabled) #js-repo-pjax-container .inline-comments .inline-comment-form,
  body:not(.wgh-disabled) #js-repo-pjax-container #all_commit_comments .commit-comments-heading,
  body:not(.wgh-disabled) #js-repo-pjax-container #all_commit_comments .comment-holder {
    max-width: inherit !important;
  }
  body:not(.wgh-disabled) #js-repo-pjax-container .js-issue-row .text-right { /* Issue list Assignee alignment */
    max-width: 303px !important;
  }

  /* Repository graph page */
  body:not(.wgh-disabled) #js-repo-pjax-container .capped-card-content { /* Graph cards on contributors / graph list */
    width: 100% !important;
  }

  /* New gist input field height */
  body:not(.wgh-disabled) .gist-content .commit-create .CodeMirror {
    min-height: 250px;
    height: calc(100vh - 500px) !important;
  }

}
```

JS:
```
"use strict";
var styleSheet = "" +
"body:not(.wgh-disabled) .application-main .container {" +
  "width: auto !important;" +
  "padding-left: 16px !important;" +
  "padding-right: 16px !important;" +
  "margin-left: 0px !important;" +
  "min-width: 980px;" +
"}" +
"body:not(.wgh-disabled) .application-main .container-lg," +
"body:not(.wgh-disabled) .footer.container-lg {" +
  "max-width: none !important;" +
  "margin-left: 0px !important;" +
"}" +

// New github design
"body:not(.wgh-disabled) .application-main .container-xl {" +
  "max-width: none !important;" +
"}" +

// Floating PR toolbar
"body:not(.wgh-disabled) .pr-toolbar {" +
  "margin-left: -16px !important;" +
  "margin-right: -16px !important;" +
  "padding-left: 16px !important;" +
  "padding-right: 16px !important;" +
"}" +

// Repository Issues
"body:not(.wgh-disabled) #js-repo-pjax-container .discussion-timeline {" +  // Issue body
  "width: 100% !important;" +
"}" +
"body:not(.wgh-disabled) #js-repo-pjax-container .timeline-new-comment {" + // New Issue / issue comment form
  "max-width: 100% !important;" +
"}" +
"body:not(.wgh-disabled) #js-repo-pjax-container .new-discussion-timeline .files-bucket > div {" + // New PR code diff
  "width: inherit !important;" +
  "left: auto !important;" +
  "right: auto !important;" +
  "margin-left: 0px !important;" +
  "margin-right: 0px !important;" +
  "padding-left: 0px !important;" +
  "padding-right: 0px !important;" +
"}" +
"body:not(.wgh-disabled) #js-repo-pjax-container .inline-comments .comment-holder," + // Diff / code comments
"body:not(.wgh-disabled) #js-repo-pjax-container .inline-comments .inline-comment-form-container," +
"body:not(.wgh-disabled) #js-repo-pjax-container .inline-comments .inline-comment-form," +
"body:not(.wgh-disabled) #js-repo-pjax-container #all_commit_comments .commit-comments-heading," +
"body:not(.wgh-disabled) #js-repo-pjax-container #all_commit_comments .comment-holder {" +
  "max-width: inherit !important;" +
"}" +
"body:not(.wgh-disabled) #js-repo-pjax-container .js-issue-row .text-right {" + // Issue list Assignee alignment
  "max-width: 303px !important;" +
"}" +

// Repository graph page
"body:not(.wgh-disabled) #js-repo-pjax-container .capped-card-content {" + // Graph cards on contributors / graph list
  "width: 100% !important;" +
"}" +

// New gist input field height
"body:not(.wgh-disabled) .gist-content .commit-create .CodeMirror {" +
  "min-height: 250px;" +
  "height: calc(100vh - 500px) !important;" +
"}" +

"";

(function () {
  var s = document.createElement('style');
  s.type = "text/css";
  s.innerHTML = styleSheet;
  (document.head || document.documentElement).appendChild(s);
})();

```
