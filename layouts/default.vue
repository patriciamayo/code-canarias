<template>
  <div vs-theme="dark">
    <TheNavBar />
    <div id="padding-scroll-content">
      <Nuxt />
    </div>
  </div>
</template>

<style>
html {
  font-family: 'Source Sans Pro', -apple-system, BlinkMacSystemFont, 'Segoe UI',
    Roboto, 'Helvetica Neue', Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
}

:root {
  --vs-success: 0, 245, 233;
  --vs-warn: 255, 255, 0;
}

body {
  background-color: #151518;
}

#padding-scroll-content {
  height: 100vh;
  overflow-x: auto;
}
</style>
