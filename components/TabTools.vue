<template>
  <div>
    <h2>A few of my favourite things</h2>

    <p>
      I'm a full-stack developer. That means I love front-end and back-end
      equally. While not exhaustive, these are the tools I enjoy using most:
    </p>

    <ul class="cards">
      <Card
        title="Laravel"
        style="--accent: var(--orange)"
        logo="/images/laravel.svg"
      >
        <p>
          For projects that depend on back-end functionality, Laravel is hard to
          beat. It’s powerful, flexible, widely supported, and a joy to use.
          I’ve used Laravel to create APIs, landing pages, portals, back-end
          management tools, and more. It’s perhaps overkill for a single landing
          page, but really shines when the project calls for a complex database
          structure or user authentication.
        </p>
        <p><a href="https://laravel.com" target="_blank">laravel.com</a></p>
      </Card>
      <Card title="Vue" style="--accent: var(--orange)" logo="/images/vue.svg">
        <p>
          When it comes to front-end frameworks, I’ve landed on Vue for many
          projects. It’s easy to use, expressive (I love that components include
          CSS as well JS and HTML), fast, easily extendable with a variety of
          third-party libraries, and can be put onto existing web pages.
        </p>
        <p><a href="https://vuejs.org" target="_blank">vuejs.org</a></p>
      </Card>
      <Card
        title="Inertia"
        style="--accent: var(--orange)"
        logo="/images/inertia.png"
      >
        <p>
          When a project needs a mix of front-end and back-end capability,
          Inertia allows me to connect Laravel and Vue together seamlessly, so I
          can take advantage of the best of both worlds, without the overhead of
          manually creating an API. I’ve used it particularly successfully where
          the front-end experience is most important but some database
          integration is required.
        </p>
        <p>
          <a href="https://inertiajs.com" target="_blank">inertiajs.com</a>
        </p>
      </Card>
      <Card
        title="Livewire"
        style="--accent: var(--orange)"
        logo="/images/livewire.webp"
      >
        <p>
          A bit like Inertia, except with less JavaScript involved, Livewire
          allows me to create dynamic front-end experiences without stepping too
          far out of the back-end development world. For websites that rely on
          Laravel but benefit from a dynamic-feeling front-end, Livewire is a
          great option.
        </p>
        <p>
          <a href="https://livewire.dev" target="_blank">livewire.dev</a>
        </p>
      </Card>
      <Card
        title="Nuxt"
        style="--accent: var(--orange)"
        logo="/images/nuxt.webp"
      >
        <p>
          Vue is great. Nuxt takes it to the next level. There are some great
          shortcuts included to speed up development (such as automatic
          imports), and its ability to generate static sites makes deployment
          effortless. If I need to create a Vue project, I generally start by
          creating a Nuxt project (in fact, <a href="https://github.com/mafu-d/cv2023" target="_blank">this CV</a> was made with Nuxt).
        </p>
        <p><a href="https://nuxtjs.org" target="_blank">nuxtjs.org</a></p>
      </Card>
      <Card
        title="Craft CMS"
        style="--accent: var(--orange)"
        logo="/images/craft.png"
      >
        <p>
          This is my CMS of choice. I’ve used WordPress (who hasn’t?), but I’ve
          found Craft CMS to be a more professional platform, with far less
          bloat, more customisability out of the box, a better experience for
          content editors, finer control over the generated output, and better
          security. And I’m especially fond of the way the database structure
          (but not the content) is defined in config files that can be tracked
          in Git, which enables more robust deployment.
        </p>
        <p>
          <a href="https://craftcms.com" target="_blank">craftcms.com</a>
        </p>
      </Card>
      <Card
        title="Sass"
        style="--accent: var(--orange)"
        logo="/images/sass.png"
      >
        <p>
          Sure, CSS is awesome. But sometimes it needs a helping hand. That’s
          why I love using Sass, and typically install it by default in most
          projects. As a result, my CSS code is cleaner and more powerful.
        </p>
        <p>
          <a href="https://sass-lang.com" target="_blank">sass-lang.com</a>
        </p>
      </Card>
      <Card
        title="Lando"
        style="--accent: var(--orange)"
        logo="/images/lando.webp"
      >
        <p>
          Working on multiple projects for different clients often means
          defining different server requirements. Docker is great for this, but
          creating Docker files manually is a pain. Lando takes the stress out
          of containerised development environments.
        </p>
        <p><a href="https://lando.dev" target="_blank">lando.dev</a></p>
      </Card>
      <Card
        title="Netlify"
        style="--accent: var(--orange)"
        logo="/images/netlify.webp"
      >
        <p>
          For static sites, I love hosting with Netlify. The deployment process
          is a doddle, with Continuous Deployment built in - code, commit, push,
          and BOOM it’s live.
        </p>
        <p>
          <a href="https://www.netlify.com" target="_blank">netlify.com</a>
        </p>
      </Card>
      <Card
        title="Deployer"
        style="--accent: var(--orange)"
        logo="/images/deployer.svg"
      >
        <p>
          For PHP sites, I prefer automating the deployment process to
          ensure nothing gets missed. Deployer is a PHP-based tool that handles
          all that for me, SSHing into the server, pulling the code from the
          repo, running any migrations or setup required, and all with zero
          downtime.
        </p>
        <p>
          <a href="https://deployer.org" target="_blank">deployer.org</a>
        </p>
      </Card>
      <Card
        title="VSCode"
        style="--accent: var(--orange)"
        logo="/images/vscode.webp"
      >
        <p>
          When it comes to actually writing code, nothing beats Visual Studio
          Code. I can easily set mine up exactly the way I want, with a plethora
          of extensions available (I’m particularly enjoying the Codeium
          extension at the moment which uses AI to autocomplete my code for me).
          I love the integrated terminal, and that I get all of that goodness
          for free.
        </p>
        <p>
          <a href="https://code.visualstudio.com" target="_blank"
            >code.visualstudio.com</a
          >
        </p>
      </Card>
    </ul>
  </div>
</template>
