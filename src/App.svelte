<script>
  import Button from "./elements/Button.svelte";
  import ResponsiveContainer from "./elements/ResponsiveContainer.svelte";
  const linkExternally = src => {
    window.open(src);
  };

  const discord = () => {
    linkExternally("https://discord.gg/7UEXYzc");
  };
  const riot = () => {
    linkExternally(
      "https://riot.im/app/#/room/#gantree-community:matrix.org?action=chat"
    );
  };
  const twitter = () => {
    linkExternally("https://twitter.com/gantree_app");
  };
</script>

<style>
  p {
    line-height: 1.5em;
  }
  h1 {
    font-size: 2.8em;
    font-weight: bold;
    text-transform: capitalize;
    line-height: 1.4em;
  }
  h2 {
    font-size: 2em;
    font-weight: bold;
    /* text-transform: capitalize; */
    line-height: 1.4em;
  }

  h3 {
    font-size: 1.5em;
    font-weight: lighter;
    line-height: 1.5em;
  }

  #rotated-crane {
    transform: rotateZ(-12deg);
    mix-blend-mode: multiply;
  }

  .resource {
    font-size: 1.8em;
    margin: 0.25em 0;
    color: black;
    text-decoration: underline;
  }

  .resource:visited {
    color: black;
  }

  .resource:hover::before {
    content: "🏗";
    position: relative;
    left: -1rem;
  }

  .header {
    color: #da5900;
    font-weight: bolder;
    text-decoration: underline;
  }

  quote {
    font-style: italic;
    line-height: 1.5em;
    font-weight: lighter;
  }

  input {
    margin: 1rem 0;
    width: 100%;
    border: none;
    background: none;
    border-bottom: 2px black solid;
  }

  input::placeholder {
    opacity: 0.8;
  }

  .w-responsive {
    width: 90%;
  }

  @media only screen and (min-aspect-ratio: 1/1) {
    .w-responsive {
      width: 50%;
    }
  }
</style>

<svelte:head>
  <link
    href="https://fonts.googleapis.com/css?family=Monda&display=swap"
    rel="stylesheet" />
  <link
    rel="stylesheet"
    href="https://unpkg.com/tachyons@4.10.0/css/tachyons.min.css" />
</svelte:head>

<ResponsiveContainer>
  <div class="w-responsive">
    <h1 class="header">Node Infrastructure Requires Heavy Lifting.</h1>
    <h3>
      Gantree gives you the leverage you need to deploy, manage and monitor your
      own node infrastructure.
    </h3>
  </div>
  <div class="w-responsive pa3" id="rotated-crane">
    <img src="/img/crane-primary.png" alt="sweet pic of crane" />
  </div>
</ResponsiveContainer>

<ResponsiveContainer secondary={true}>
  <div class="w-responsive h-50">
    <h2>Focus less on DevOps, more on building your business.</h2>
    <h3>
      Using Gantree, any organisation can own a piece of the infrastructure that
      powers the global, p2p economy.
    </h3>
  </div>
  <div class="w-responsive flex h-50 justify-end">
    <div class="w-75 flex flex-column ">
      <h2>Gantree Resources:</h2>
      <a
        class="resource"
        target="_new"
        href="https://github.com/flex-dapps/gantree-lib-nodejs">
        gantree-lib
      </a>
      <a
        class="resource"
        target="_new"
        href="https://github.com/flex-dapps/gantree-lib-nodejs/blob/dev/docs/gantree_config/tutorial.md">
        tutorial
      </a>
      <a
        class="resource"
        target="_new"
        href="https://github.com/flex-dapps/gantree-cli">
        gantree-cli
      </a>
      <a
        class="resource"
        target="_new"
        href="https://www.youtube.com/watch?v=fQDwd8lOMqQ">
        demo video
      </a>
    </div>
  </div>
</ResponsiveContainer>

<ResponsiveContainer tall={false}>
  <div class="w-responsive">
    <h3>We take inspiration from the Gantry Crane.</h3>
    <quote>
      Invented in 1959 by the Paceco Corporation, Ship-to-shore Gantree cranes
      are capable of lifting some of the heaviest loads in the world, they help
      pioneering companies minimise time in port and ship faster.
    </quote>
  </div>
  <div class="w-responsive pa5">
    <img src="/img/crane-secondary.png" alt="another banger of a crane" />
  </div>
</ResponsiveContainer>

<ResponsiveContainer secondary={true}>
  <div class="w-responsive pa3">
    <h2>Join our community!</h2>
    <p>
      Interested in using or contributing to Gantree? We're fostering an
      open-source community where anybody can help us to
      <i>
        Empower any organisation to cultivate and grow the peer to peer
        economy".
      </i>
    </p>
    <p>Have a feature idea, bug to report or want to make a pull request?</p>
    <p>
      Join us on Riot Chat and Discord to get involved and share your finest
      memes.
    </p>
    <div class="flex flex-wrap justify-start pa2">
      <Button src="/img/riot.png" text="Riot Chat" click={riot} />
      <Button src="/img/discord.png" text="Discord" click={discord} />
      <Button src="/img/twitter.png" text="Twitter" click={twitter} />
    </div>
  </div>
  <div class="w-responsive pa3">
    <h2>Want to get in touch?</h2>
    <p>
      We'll get back to you as soon as we can, in the meantime check out our
      online communities.
    </p>
    <form action="https://formspree.io/mwkrodrp" method="POST" class="w-100">
      <label>Your name:</label>
      <input type="text" name="name" />
      <label>Your email:</label>
      <input type="text" name="_replyto" />
      <input type="hidden" name="_subject" value="Gantree Form Submission" />
      <label>Your message:</label>
      <input name="message" />
      <div class="w-100 flex justify-end">
        <Button text="Submit" type="submit" src="/img/enter.png" />
      </div>
    </form>
  </div>

</ResponsiveContainer>
