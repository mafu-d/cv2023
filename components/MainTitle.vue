<template>
  <Head>
    <Link
      href="https://fonts.googleapis.com/css2?family=Pacifico&family=Raleway:wght@100;400;900&display=swap"
      rel="stylesheet"
    />
  </Head>
  <header>
    <h1>CV</h1>
    <div class="subtitle">
      <div class="subtitle__name">Matthew Dawkins</div>
      <div class="subtitle__title">Web Developer</div>
    </div>
  </header>
  <div class="contact-details">
    <p>Phone: 07443609124</p>
    <p>Email: matthew.dawkins@gmail.com</p>
    <p>Location: Somerset, UK</p>
  </div>
</template>

<style lang="scss" scoped>
@use "sass:math";

header {
  text-align: center;
  display: grid;
  grid-template-areas: "title";
  justify-content: center;
  align-items: center;
  overflow-x: hidden;
}

h1 {
  font-size: 20rem;
  line-height: 1;
  margin: 0;
  grid-area: title;
  opacity: 0.2;
  z-index: -1;
  color: var(--blue);
  @media screen {
    animation: dullColours 10s infinite;
  }
}

@keyframes dullColours {
  0% {
    color: var(--yellow);
  }
  20% {
    color: var(--orange);
  }
  40% {
    color: var(--red);
  }
  60% {
    color: var(--purple);
  }
  80% {
    color: var(--blue);
  }
  100% {
    color: var(--yellow);
  }
}

.subtitle {
  font-family: "Pacifico", cursive;
  grid-area: title;
  margin: 0;
  line-height: 1.1;

  &__name {
    font-size: 4rem;
    color: var(--purple);
    @media screen {
      background: linear-gradient(
        to right,
        var(--yellow),
        var(--orange),
        var(--red),
        var(--purple),
        var(--blue)
      );
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
    }
  }

  &__title {
    font-size: 2rem;
    font-family: "Raleway", sans-serif;
    font-weight: 100;
    @media screen {
      color: var(--yellow);
    }
  }
}

.contact-details {
  text-align: center;
  @media screen {
    display: none;
  }
}
</style>
