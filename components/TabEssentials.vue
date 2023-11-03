<template>
  <div>
    <h2>What you need to know</h2>
    <p>
      I’m a full-stack web developer with 20 years of experience behind me. I
      love using PHP, JavaScript, CSS, Laravel, Vue, Craft CMS, and other LAMP
      stack and front end
      <a href="#" @click.prevent="$emit('selectTab', 'tools')">technologies</a>.
      Having worked in-house and agency-side, I’m now looking for a future where
      I can make a positive impact - not just to turnover but to people’s lives.
      I’m passionate about the
      <a
        href="https://www.tbtmarketing.com/blog/reducing-your-offices-carbon-footprint-from-home"
        target="_blank"
        >environment</a
      >
      (because that’s where I live), I occasionally dream in code, and I love a
      good cup of tea.
    </p>
    <h3>Current employment</h3>
    <ul class="cards">
      <Card
        title="Senior Web Developer, TBT Marketing, August 2017 - Present"
        logo="/images/tbt_logo.svg"
      >
        <p>
          Leading a small team of developers in creating B2B marketing solutions
          for clients in the IT sector.
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
          GCSEs: lots, almost all A and A* (but let's face it, these are pretty
          redundant at this point)
        </p>
      </Card>
    </ul>
  </div>
</template>
