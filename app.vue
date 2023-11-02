<template>
  <div>
    <Head>
      <Title>CV - Matthew Dawkins</Title>
      <Link rel="preconnect" href="https://fonts.googleapis.com" />
      <Link rel="preconnect" href="https://fonts.gstatic.com" />
      <Link
        href="https://fonts.googleapis.com/css2?family=Raleway:wght@100;400;900&display=swap"
        rel="stylesheet"
      />
    </Head>
    <MainTitle />
    <main>
      <Tabs />
    </main>
  </div>
</template>

<style lang="scss">
:root {
  --yellow: #ffbe0b;
  --orange: #fb5607;
  --red: #ff006e;
  --purple: #8338ec;
  --blue: #3a86ff;
  color-scheme: dark;
}
body {
  font-family: "Raleway", sans-serif;
  margin: 0;
}

main {
  max-width: 800px;
  margin: 0 auto;
  padding: 1rem;
}
</style>
