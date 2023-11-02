<template>
  <div class="tabs">
    <ul class="tabs__tabs">
      <li
        class="tabs__tab"
        :class="{ 'tabs__tab--active': activeTab === 'essentials' }"
        @click="activeTab = 'essentials'"
      >
        Essentials
      </li>
      <li
        class="tabs__tab"
        :class="{ 'tabs__tab--active': activeTab === 'tools' }"
        @click="activeTab = 'tools'"
      >
        Tools and technologies
      </li>
      <li
        class="tabs__tab"
        :class="{ 'tabs__tab--active': activeTab === 'beyond' }"
        @click="activeTab = 'beyond'"
      >
        Beyond the desk
      </li>
      <li
        class="tabs__tab"
        :class="{ 'tabs__tab--active': activeTab === 'contact' }"
        @click="activeTab = 'contact'"
      >
        Contact me
      </li>
    </ul>
    <div class="tabs__contents">
      <div class="tabs__content" v-show="activeTab === 'essentials'">
        <h2>Essentials</h2>
        <p>
          I’m a full-stack web developer with 20 years of experience behind me.
          I love using PHP, JavaScript, CSS, Laravel, Vue, Craft CMS, and other
          LAMP stack technologies. Having worked in-house and agency-side, I’m
          now looking for a future where I can make a positive impact - not just
          to turnover but to people’s lives. I’m passionate about the
          environment (because that’s where I live), I occasionally dream in
          code, and I love a good cup of tea.
        </p>

        <h3>Current employment</h3>
        <Card
          title="Senior Web Developer, TBT Marketing, August 2017 - Present"
          logo="/images/tbt_logo.svg"
        >
          <p>
            Leading a small team of developers in creating B2B marketing
            solutions for clients in the IT sector.
          </p>
          <p>
            <a href="https://tbtmarketing.com" target="_blank"
              >tbtmarketing.com</a
            >
          </p>
        </Card>

        <h3>Previous employment</h3>
        <Card
          title="Web Developer, Crown Pet Foods, 2010-2017"
          logo="/images/cpf_logos.webp"
          style="--accent: var(--red)"
        >
          <p>
            Created and managed corporate websites, user portals, a voucher
            scanning app, internal tools, and a bespoke CRM platform.
          </p>
        </Card>
        <Card
          title="Freelance Web Developer, 2005-2011"
          logo="/images/c9-logo-colour.png"
          style="--accent: var(--red)"
        >
          <p>
            Providing web design and development services for churches and
            Christian organisations across the UK.
          </p>
        </Card>
        <Card
          title="Webmaster, Diocese of Chelmsford, 2005-2010"
          logo="/images/diocese-of-chelmsford-logo.png"
          style="--accent: var(--red)"
        >
          <p>
            Created and managed the website and provided support to content
            editors.
          </p>
        </Card>
        <Card
          title="Chaplaincy Assistant, University of Essex, 2004-2005"
          logo="/images/essex_logo.gif"
          style="--accent: var(--red)"
        >
          <p>
            Helped run the Chaplaincy Centre, leading services, running Bible
            study groups, providing pastoral support, coordinating outreach
            events, comms.
          </p>
        </Card>

        <h3>Education</h3>
        <Card
          title="University of Essex, 2001-2004"
          logo="/images/essex_logo.gif"
          style="--accent: var(--blue)"
        >
          <p>BSc. Computer Science (2:1)</p>
        </Card>
        <Card
          title="Torquay Boys Grammar School, 1994-2001"
          logo="/images/tbgs_crest.png"
          style="--accent: var(--blue)"
        >
          <p>A levels: Music (A), Computing (C), Maths (C)</p>
          <p>GCSEs: lots, mostly A and A*</p>
        </Card>
      </div>
      <div class="tabs__content" v-show="activeTab === 'tools'">
        <h2>Tools and technologies</h2>

        <h3>Laravel</h3>
        <p>
          For projects that depend on back-end functionality, Laravel is hard to
          beat. It’s powerful, flexible, widely supported, and a joy to use.
          I’ve used Laravel to create APIs, landing pages, portals, back-end
          management tools, and more. It’s perhaps overkill for a single landing
          page, but really shines when the project calls for a complex database
          structure or user authentication.
        </p>
        <h3>Vue</h3>
        <p>
          When it comes to front-end frameworks, I’ve landed on Vue for many
          projects. It’s easy to use, expressive (I love that components include
          CSS as well JS and HTML), fast, easily extendable with a variety of
          third-party libraries, and can be put onto existing web pages.
        </p>
        <h3>Inertia</h3>
        <p>
          When a project needs a mix of front-end and back-end capability,
          Inertia allows me to connect Laravel and Vue together seamlessly, so I
          can take advantage of the best of both worlds, without the overhead of
          manually creating an API. I’ve used it particularly successfully where
          the front-end experience is most important but some database
          integration is required.
        </p>
        <h3>Livewire</h3>
        <p>
          A bit like Inertia, except with less JavaScript involved, Livewire
          allows me to create dynamic front-end experiences without stepping too
          far out of the back-end development world. For websites that rely on
          Laravel but benefit from a dynamic-feeling front-end, Livewire is a
          great option.
        </p>
        <h3>Nuxt</h3>
        <p>
          Vue is great. Nuxt takes it to the next level. There are some great
          shortcuts included to speed up development (such as automatic
          imports), and its ability to generate static sites makes deployment
          effortless. If I need to create a Vue project, I generally start by
          creating a Nuxt project.
        </p>
        <h3>Craft CMS</h3>
        <p>
          This is my CMS of choice. I’ve used WordPress (who hasn’t?), but I’ve
          found Craft CMS to be a more professional platform, with far less
          bloat, more customisability out of the box, a better experience for
          content editors, finer control over the generated output, and better
          security. And I’m especially fond of the way the database structure
          (but not the content) is defined in config files that can be tracked
          in Git, which enables more robust deployment.
        </p>
        <h3>Sass</h3>
        <p>
          Sure, CSS is awesome. But sometimes it needs a helping hand. That’s
          why I love using Sass, and typically install it by default in most
          projects. As a result, my CSS code is cleaner and more powerful.
        </p>
        <h3>Lando</h3>
        <p>
          Working on multiple projects for different clients often means
          defining different server requirements. Docker is great for this, but
          creating Docker files manually is a pain. Lando takes the stress out
          of containerised development environments.
        </p>
        <h3>Netlify</h3>
        <p>
          For static sites, I love hosting with Netlify. The deployment process
          is a doddle, with Continuous Deployment built in - code, commit, push,
          and BOOM it’s live.
        </p>
        <h3>Deployer</h3>
        <p>
          For more PHP sites, I prefer automating the deployment process to
          ensure nothing gets missed. Deployer is a PHP-based tool that handles
          all that for me, SSHing into the server, pulling the code from the
          repo, running any migrations or setup required, and all with zero
          downtime.
        </p>
        <h3>VSCode</h3>
        <p>
          When it comes to actually writing code, nothing beats Visual Studio
          Code. I can easily set mine up exactly the way I want, with a plethora
          of extensions available (I’m particularly enjoying the Codeium
          extension at the moment which uses AI to autocomplete my code for me).
          I love the integrated terminal, and that I get all of that goodness
          for free.
        </p>
      </div>
      <div class="tabs__content" v-show="activeTab === 'beyond'">
        <h2>Beyond the desk</h2>
        <h3>Theatre</h3>
        <p>
          I’ve been involved in a number of local amateur groups in Frome and
          Castle Cary over the past few years, taking both ensemble and lead
          parts. If it involves any combination of acting, singing or dancing,
          I’m up for it. 2024 will also see my debut as a Musical Director.
        </p>
        <h3>Music</h3>
        <p>
          I primarily enjoy listening to jazz and contemporary Christian
          worship, but also occasionally classical music. I play guitar, bass,
          cello, piano, and can have a fair bash at clarinet, saxophone, drums,
          and melodica. Oh, and I also write music too.
        </p>
        <h3>Model railways</h3>
        <p>
          I’m now two years into my rebuild project, constructing a OO scale
          fictitious GWR branch line terminus set in the late 1930s,
          affectionately called “Frontington and Backwoods”. I have documented
          my progress through YouTube, Facebook and Instagram.
        </p>
        <h3>Church</h3>
        <p>
          I’m a licensed Reader in the Church of England, ministering to my
          local church and community. I also lead worship at a local ecumenical
          gathering called The Filling Station.
        </p>
      </div>
      <div class="tabs__content" v-show="activeTab === 'contact'">
        <h2>Contact me</h2>
      </div>
    </div>
  </div>
</template>

<script setup>
const activeTab = ref("essentials");
</script>

<style lang="scss" scoped>
.tabs {
  &__tabs {
    display: flex;
    list-style: none;
    padding: 0;
    margin: 0;
    border-bottom: 1px solid var(--purple);
  }
  &__tab {
    padding: 0.5rem 1rem;
    font-weight: bold;
    font-size: 1.2rem;
    cursor: pointer;
    background: linear-gradient(to bottom, transparent, transparent);

    &--active {
      background: linear-gradient(45deg, var(--yellow), var(--orange));
      color: black;
    }

    &:not(&--active):hover {
      background: linear-gradient(to bottom, transparent, var(--purple));
    }
  }
}
</style>
