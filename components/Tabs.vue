<template>
  <div class="tabs">
    <div
      class="tabs__tabs"
      role="tablist"
      aria-label="Tabs"
      @keydown.left="selectPreviousTab"
      @keydown.right="selectNextTab"
    >
      <button
        v-for="(tab, index) in tabs"
        :key="index"
        role="tab"
        class="tabs__tab"
        :aria-selected="activeTab === tab.id"
        :aria-controls="tab.id"
        @click="activeTab = tab.id"
        :tabindex="activeTab === tab.id ? 0 : -1"
        ref="tabsRefs"
      >
        {{ tab.label }}
      </button>
    </div>

    <div class="tabs__contents">
      <TabPanel
        label="Essentials"
        id="essentials"
        :active="activeTab === 'essentials'"
      >
        <h2>What you need to know</h2>
        <p>
          I’m a full-stack web developer with 20 years of experience behind me.
          I love using PHP, JavaScript, CSS, Laravel, Vue, Craft CMS, and other
          LAMP stack and front end
          <a href="#" @click.prevent="activeTab = 'tools'">technologies</a>.
          Having worked in-house and agency-side, I’m now looking for a future
          where I can make a positive impact - not just to turnover but to
          people’s lives. I’m passionate about the
          <a
            href="https://www.tbtmarketing.com/blog/reducing-your-offices-carbon-footprint-from-home"
            target="_blank"
            >environment</a
          >
          (because that’s where I live), I occasionally dream in code, and I
          love a good cup of tea.
        </p>

        <h3>Current employment</h3>
        <ul class="cards">
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
        </ul>

        <h3>Previous employment</h3>
        <ul class="cards">
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
            logo="/images/diocese-of-chelmsford-logo.webp"
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
        </ul>

        <h3>Education</h3>
        <ul class="cards">
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
            <p>
              GCSEs: lots, almost all A and A* (but let's face it, these are
              pretty redundant at this point)
            </p>
          </Card>
        </ul>
      </TabPanel>

      <TabPanel
        label="Tools and technologies"
        id="tools"
        :active="activeTab === 'tools'"
      >
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
              For projects that depend on back-end functionality, Laravel is
              hard to beat. It’s powerful, flexible, widely supported, and a joy
              to use. I’ve used Laravel to create APIs, landing pages, portals,
              back-end management tools, and more. It’s perhaps overkill for a
              single landing page, but really shines when the project calls for
              a complex database structure or user authentication.
            </p>
            <p><a href="https://laravel.com" target="_blank">laravel.com</a></p>
          </Card>
          <Card
            title="Vue"
            style="--accent: var(--orange)"
            logo="/images/vue.svg"
          >
            <p>
              When it comes to front-end frameworks, I’ve landed on Vue for many
              projects. It’s easy to use, expressive (I love that components
              include CSS as well JS and HTML), fast, easily extendable with a
              variety of third-party libraries, and can be put onto existing web
              pages.
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
              Inertia allows me to connect Laravel and Vue together seamlessly,
              so I can take advantage of the best of both worlds, without the
              overhead of manually creating an API. I’ve used it particularly
              successfully where the front-end experience is most important but
              some database integration is required.
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
              allows me to create dynamic front-end experiences without stepping
              too far out of the back-end development world. For websites that
              rely on Laravel but benefit from a dynamic-feeling front-end,
              Livewire is a great option.
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
              Vue is great. Nuxt takes it to the next level. There are some
              great shortcuts included to speed up development (such as
              automatic imports), and its ability to generate static sites makes
              deployment effortless. If I need to create a Vue project, I
              generally start by creating a Nuxt project (in fact, this CV was
              made with Nuxt).
            </p>
            <p><a href="https://nuxtjs.org" target="_blank">nuxtjs.org</a></p>
          </Card>
          <Card
            title="Craft CMS"
            style="--accent: var(--orange)"
            logo="/images/craft.png"
          >
            <p>
              This is my CMS of choice. I’ve used WordPress (who hasn’t?), but
              I’ve found Craft CMS to be a more professional platform, with far
              less bloat, more customisability out of the box, a better
              experience for content editors, finer control over the generated
              output, and better security. And I’m especially fond of the way
              the database structure (but not the content) is defined in config
              files that can be tracked in Git, which enables more robust
              deployment.
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
              Sure, CSS is awesome. But sometimes it needs a helping hand.
              That’s why I love using Sass, and typically install it by default
              in most projects. As a result, my CSS code is cleaner and more
              powerful.
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
              defining different server requirements. Docker is great for this,
              but creating Docker files manually is a pain. Lando takes the
              stress out of containerised development environments.
            </p>
            <p><a href="https://lando.dev" target="_blank">lando.dev</a></p>
          </Card>
          <Card
            title="Netlify"
            style="--accent: var(--orange)"
            logo="/images/netlify.webp"
          >
            <p>
              For static sites, I love hosting with Netlify. The deployment
              process is a doddle, with Continuous Deployment built in - code,
              commit, push, and BOOM it’s live.
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
              For more PHP sites, I prefer automating the deployment process to
              ensure nothing gets missed. Deployer is a PHP-based tool that
              handles all that for me, SSHing into the server, pulling the code
              from the repo, running any migrations or setup required, and all
              with zero downtime.
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
              When it comes to actually writing code, nothing beats Visual
              Studio Code. I can easily set mine up exactly the way I want, with
              a plethora of extensions available (I’m particularly enjoying the
              Codeium extension at the moment which uses AI to autocomplete my
              code for me). I love the integrated terminal, and that I get all
              of that goodness for free.
            </p>
            <p>
              <a href="https://code.visualstudio.com" target="_blank"
                >code.visualstudio.com</a
              >
            </p>
          </Card>
        </ul>
      </TabPanel>

      <TabPanel
        label="Other interests"
        id="beyond"
        :active="activeTab === 'beyond'"
      >
        <h2>When I'm not at work</h2>
        <p>All work and no play makes Jack a dull boy. I'm not Jack.</p>

        <ul class="cards">
          <Card title="Theatre" style="--accent: var(--red)">
            <p>
              I’ve been involved in a number of local amateur groups in Frome
              and Castle Cary over the past few years, taking both ensemble and
              lead parts. If it involves any combination of acting, singing or
              dancing, I’m up for it. 2024 will also see my debut as a Musical
              Director.
            </p>
          </Card>
          <Card title="Music" style="--accent: var(--red)">
            <p>
              I primarily enjoy listening to jazz and contemporary Christian
              worship, but also occasionally classical music. I play guitar,
              bass, cello, piano, and can have a fair bash at clarinet,
              saxophone, drums, and melodica. Oh, and I also write music too.
            </p>
          </Card>
          <Card title="Model railways" style="--accent: var(--red)">
            <p>
              I’m now two years into my rebuild project, constructing a OO scale
              fictitious GWR branch line terminus set in the late 1930s,
              affectionately called “Frontington and Backwoods”. I have
              documented my progress through
              <a
                href="https://www.youtube.com/@FrontingtonandBackwoodsRailway"
                target="_blank"
                >YouTube</a
              >,
              <a
                href="https://www.facebook.com/FrontingtonBackwoods"
                target="_blank"
                >Facebook</a
              >
              and
              <a href="https://instagram.com/frontington" target="_blank"
                >Instagram</a
              >.
            </p>
          </Card>
          <Card title="Church" style="--accent: var(--red)">
            <p>
              I’m a licensed Reader in the Church of England, ministering to my
              local church and community. I also lead worship at a local
              ecumenical gathering called The Filling Station.
            </p>
          </Card>
        </ul>
      </TabPanel>

      <TabPanel
        label="Contact me"
        id="contact"
        :active="activeTab === 'contact'"
      >
        <h2>Give me a bell</h2>
      </TabPanel>
    </div>
  </div>
</template>

<script setup>
const activeTab = ref("essentials");
const tabs = [
  { id: "essentials", label: "Essentials" },
  { id: "tools", label: "Tools and technologies" },
  { id: "beyond", label: "Beyond the desk" },
  { id: "contact", label: "Contact me" },
];
const tabsRefs = ref([]);

/**
 * Get the index of the currently selected tab
 *
 * @return  {number}
 */
function getCurrentTabIndex() {
  return tabs.findIndex((tab) => tab.id === activeTab.value);
}

/**
 * Focus on the currently selected tab
 *
 * @return  {void}
 */
function selectCurrentTab() {
  tabsRefs.value[getCurrentTabIndex()].focus();
}

/**
 * Focus on the previous tab
 *
 * @return  {void}
 */
function selectPreviousTab() {
  activeTab.value =
    tabs[getCurrentTabIndex() - 1]?.id || tabs[tabs.length - 1].id;
  selectCurrentTab();
}

/**
 * Focus on the next tab
 *
 * @return  {void}
 */
function selectNextTab() {
  activeTab.value = tabs[getCurrentTabIndex() + 1]?.id || tabs[0].id;
  selectCurrentTab();
}
</script>

<style lang="scss" scoped>
.tabs {
  &__tabs {
    display: flex;
    flex-wrap: wrap;
    border-bottom: 1px solid var(--purple);

    @media print {
      display: none;
    }
  }

  &__tab {
    padding: 0.5rem 1rem;
    font: inherit;
    font-weight: bold;
    cursor: pointer;
    background: linear-gradient(to bottom, transparent, transparent);
    text-decoration: none;
    border: 0;

    &[aria-selected="true"] {
      background: linear-gradient(45deg, var(--yellow), var(--orange));
      color: black;
    }

    &:not(&[aria-selected="true"]):hover {
      background: linear-gradient(to bottom, transparent, var(--purple));
    }
  }
}

.cards {
  padding: 0;
  margin: 0;
  list-style: none;
}

@media print {
  a {
    color: inherit;
    text-decoration: none;
  }
}
</style>
