<template>
  <h2>Give me a bell</h2>

  <form action="" method="post">
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
      <textarea name="message" id="message" required></textarea>
    </div>
    <div>
      <button type="submit">Send</button>
    </div>
  </form>
</template>

<style lang="scss" scoped></style>
