<template>
  <footer class="footer">
    <div class="footer-container">
      <p class="footer-love">
        Hecho con ❤️ en las Islas Canarias 🇮🇨 por
        <a href="patriciamayo.com">Patricia</a>
      </p>
      <ul class="footer-links">
        <li class="footer-link">
          <a
            href="https://github.com/patriciamayo/code-canarias"
            target="_blank"
            >Github</a
          >
        </li>
        <li class="footer-link">
          <a href="mailto:abc@example.com" target="_blank">Contact</a>
        </li>
      </ul>
    </div>
  </footer>
</template>

<script>
export default {}
</script>

<style scoped>
.footer {
  padding: 32px;
}
.footer-container {
  color: white;
  display: flex;
  width: 100%;
  justify-content: space-between;
  align-items: center;
}

.footer-links {
  list-style: none;
  display: flex;
  padding-left: 0;
}

.footer-link {
  margin-left: 32px;
}
</style>
