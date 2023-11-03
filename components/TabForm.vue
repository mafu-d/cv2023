<template>
  <div>
    <h2>Give me a bell</h2>
    <div class="print-only">
      <p>Phone: 07443609124</p>
      <p>Email: matthew.dawkins@gmail.com</p>
      <p>Location: Somerset, UK</p>
    </div>
    <form name="contact" method="POST" netlify>
      <div>
        <label for="name">Your name:</label>
        <input type="text" name="name" id="name" required />
      </div>
      <div>
        <label for="email">Your email address:</label>
        <input type="email" name="email" id="email" required />
      </div>
      <div>
        <label for="message">Your message:</label>
        <textarea name="message" id="message" required rows="5"></textarea>
      </div>
      <div>
        <button type="submit">Send</button>
      </div>
    </form>
  </div>
</template>

<style lang="scss" scoped>
.print-only {
  @media screen {
    display: none;
  }
}

form {
  display: grid;
  gap: 1rem;

  @media print {
    display: none;
  }
}

label {
  display: block;
  margin-bottom: 0.5rem;
}

input,
textarea {
  display: block;
  width: 100%;
  padding: 0.5rem;
  font: inherit;
  border: 0;
  margin: 0;
  background: rgba(255, 255, 255, 0.1);
  transition: box-shadow 0.2s ease;

  &:focus {
    outline: 0;
    box-shadow: inset 0 -3px 0 0 var(--purple);
  }
}

button {
  background: linear-gradient(to bottom, var(--blue), var(--purple));
  color: white;
  font: inherit;
  border: 0;
  padding: 0.5rem 1rem;
  border-radius: 0.2rem;
  cursor: pointer;
  transition: box-shadow 0.2s ease;

  &:hover {
    box-shadow: inset 0 0 0 999rem rgba(255, 255, 255, 0.1),
      0 0 0 0.15rem var(--yellow);
  }

  &:active {
    box-shadow: inset 0 0 0 999rem rgba(0, 0, 0, 0.4);
  }
}
</style>
