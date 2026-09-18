---
title: "Digital Twin"
draft: false
showTitle: false
showAuthor: false
showDate: false
showReadingTime: false
showWordCount: false
showTableOfContents: false
fullWidth: true
menu:
  main:
    name: "Digital Twin"
    weight: 30
---

<style>
  /* Remove article/header restrictions */
  header.article-header,
  .article-header,
  article > header,
  .mb-12 {
    display: none !important;
  }

  /* Remove Hugo/theme container width restrictions */
  main,
  article,
  .article-content,
  .content,
  .prose,
  div.max-w-prose,
  div.max-w-3xl,
  div.max-w-7xl,
  div.max-w-full,
  .container {
    max-width: none !important;
    width: 100% !important;
  }

  /* Remove padding/margins from the page wrappers */
  main,
  article,
  .article-content,
  .content {
    padding: 0 !important;
    margin: 0 !important;
  }

  /* Chatbot full-width breakout */
  .digital-twin-wrapper {
    width: 100vw !important;
    max-width: 100vw !important;

    margin-left: calc(50% - 50vw) !important;
    margin-right: 0 !important;

    padding: 0 !important;

    height: calc(100vh - 64px);
    min-height: 600px;

    overflow: hidden;
  }

  .digital-twin-wrapper iframe {
    display: block;

    width: 100% !important;
    max-width: none !important;

    height: 100% !important;
    min-height: 600px;

    border: none !important;
    border-radius: 0 !important;

    margin: 0 !important;
    padding: 0 !important;

    background: #07111e;
  }

  /* Mobile */
  @media (max-width: 768px) {
    .digital-twin-wrapper {
      height: calc(100vh - 56px);
      min-height: 500px;
    }

    .digital-twin-wrapper iframe {
      min-height: 500px;
    }
  }
</style>

<div class="digital-twin-wrapper">
  <iframe
    src="https://digital-twin-jodb.onrender.com"
    title="Digital Twin"
    frameborder="0"
    allow="microphone; camera"
    loading="eager">
  </iframe>
</div>