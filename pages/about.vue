<template>
    <ContentDoc class="content" path="/about" />
</template>

<style>
  .content {
    max-width: 70ch;
    background: red;
    margin: auto;
    padding: 1rem;
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  .content > h1, h2, h3, h4, h5, h6 {
    text-align: center;
    margin: 1rem;
  }

  .content > p {
    margin: 0.5rem;
    text-indent: 3rem;
    text-align: justify;
  }

  .content > p:has(img) {
    text-indent: 0 !important;
    text-align: center;
  }

  .content > p > img {
    max-width: min(80ch, 100vw);
  }
</style>