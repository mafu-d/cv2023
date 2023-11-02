<template>
  <div>
    <Head>
      <Title>CV - Matthew Dawkins</Title>
      <Link rel="preconnect" href="https://fonts.googleapis.com" />
      <Link rel="preconnect" href="https://fonts.gstatic.com" />
      <Link
        href="https://fonts.googleapis.com/css2?family=Raleway:wght@100;400;600;900&display=swap"
        rel="stylesheet"
      />
      <Link
        href="https://fonts.googleapis.com/css2?family=Pacifico&family=Quicksand:wght@300;400;600;700&family=Raleway:wght@100;400;900&display=swap"
        rel="stylesheet"
      />
    </Head>
    <MainTitle />
    <main>
      <Tabs />
    </main>
    <footer class="footer">
      &copy; 2023 Matthew Dawkins. All rights reserved.
    </footer>
  </div>
</template>

<style lang="scss">
:root {
  --yellow: #ffbe0b;
  --orange: #fb5607;
  --red: #ff006e;
  --purple: #8338ec;
  --blue: #3a86ff;
  @media screen {
    font-size: 18px;
    color-scheme: dark;
  }
}
body {
  font-family: "Quicksand", sans-serif;
  margin: 0;
}

main {
  max-width: 800px;
  margin: 0 auto;
  padding: 1rem;
}

h2 {
  font-size: 2.8rem;
  line-height: 1.2;
  position: relative;
  display: inline-block;
  letter-spacing: -0.05em;
  color: var(--yellow);
  @media screen {
    background: linear-gradient(to bottom, var(--yellow), var(--orange));
    background-clip: text;
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
  }

  &::before {
    content: "";
    width: 100%;
    height: 0.16em;
    background: var(--orange);
    position: absolute;
    bottom: -0.18em;
    border-radius: 0.08em;
  }

  &::after {
    content: "";
    color: var(--yellow);
    width: 0.2em;
    height: 0.2em;
    border-radius: 50%;
    display: inline-block;
    background: var(--yellow);
    animation: h2-stop-color 1s alternate infinite ease-in-out;
    position: absolute;
    right: -0.3em;
    bottom: -0.2em;
  }
}

@keyframes h2-stop-color {
  0% {
    background: var(--yellow);
  }
  100% {
    background: var(--orange);
  }
}

h3 {
  font-size: 2rem;
  line-height: 1.2;
  letter-spacing: -0.04em;
  color: var(--orange);

  @media screen {
    background: linear-gradient(to bottom, var(--orange), var(--red));
    background-clip: text;
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
  }
  @media print {
    break-after: avoid;
  }
}

.footer {
  font-size: 0.8rem;
  text-align: center;
  padding: 1rem;
}
</style>
