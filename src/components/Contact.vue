<script></script>

<template>
  <footer id="contact" class="contact">
    <a class="contact-info link" href="https://github.com/archawitch" target="_blank">GitHub</a>
    <a class="contact-info link" href="https://linkedin.com/in/archawitch/" target="_blank"
      >LinkedIn</a
    >
    <a class="contact-info link" href="mailto:parchawitch@gmail.com" target="_blank"
      >parchawitch@gmail.com</a
    >
  </footer>
</template>

<style scoped>
.contact {
  margin-bottom: 1rem;
  padding-top: 2.5rem;
  border-top: 0.06rem solid #444147;
  display: flex;
  align-items: baseline;
  width: 100%;
}

.contact-info:not(:last-child) {
  margin-right: 1.5rem;
}

@media only screen and (max-width: 640px) {
  .contact {
    flex-direction: column;
    row-gap: 1.5rem;
    margin-bottom: 1.5rem;
  }
}
</style>
