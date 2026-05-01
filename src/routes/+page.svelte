<script lang="ts">
  let name = '';
  let email = '';
  let message = '';

  function handleSubmit(e: Event) {
    e.preventDefault();
    console.log({ name, email, message });
    alert('Form submitted (check console)');
  }
</script>

<style>
  nav {
    position: fixed;
    top: 0;
    width: 100%;
    background: #222;
    padding: 1rem;
    display: flex;
    gap: 1rem;
    z-index: 10;
  }

  nav a {
    color: white;
    text-decoration: none;
  }

  section {
    min-height: 100vh;
    padding: 100px 2rem 2rem;
    scroll-margin-top: 80px;
  }

  /* Layout helpers */
  .two-col {
    display: flex;
    gap: 2rem;
  }

  .col {
    flex: 1;
  }

  .yellow {
    background: #facc15;
  }


  /* Contact form */
  form {
    max-width: 400px;
    display: flex;
    flex-direction: column;
    gap: 1rem;
  }

  input, textarea {
    padding: 0.5rem;
    font-size: 1rem;
  }

  button {
    padding: 0.7rem;
    background: #222;
    color: white;
    border: none;
    cursor: pointer;
  }
</style>

<nav>
  <a href="#home">Rólunk</a>
  <a href="#about">Szolgáltatások</a>
  <a href="#contact">Kontakt</a>
</nav>

<section>
  <h1>My Product</h1>
  <p>A simple sentence describing what this product does.</p>
</section>

<section id="home">
  <div class="two-col">
    <div class="col">
      <h1>Rólunk</h1>
      <p>
        Az Y Production 2018 óta a hazai televíziós és filmes hangutómunka egyik kiemelkedő szereplője.

        Dinamikusan fejlődő cégünk professzionális hangkeveréssel, zenei szerkesztéssel, valamint filmes utómunkákkal foglalkozik.

        Partnereink között megtalálhatók a vezető televíziós csatornák és streaming platformok:
        RTL, TV2, ViaSat, MTVA, HBO.

        Tevékenységünk kiterjed podcastok gyártására - többek között az IstenEst és a Ki Mit Tube műsorok felvétele is nálunk készül.

        Továbbá próbatermek és stúdióhelyiségek bérbeadására, valamint professzionális technikai eszközök biztosítására is.

        Valamint legújabb szolgáltatásunk az AI tartalmak gyártása, melyre egy egész csapatunk specializálódott. Legyen szó reklámokról, tv műsorokról, social média tartalmakról.
      </p>
    </div>

    <div class="col yellow">
      <!-- Placeholder visual -->
    </div>
  </div>
</section>

<section id="about">
  

  <div class="two-col">
    <div class="col">
      <p>SZOLGÁLTATÁSAINK
        HANGFELVÉTEL
        HANGUTÓMUNKA
        ZENEI SZERKESZTÉS
        SZINKRON

        STÚDIÓ BÉRBEADÁS
        PRÓBATEREM
        TÁNCTEREM
        PODCAST STÚDIÓ

        RENTAL
        KAMERATECHNIKA
        HANGTECHNIKA
        AI TARTALOMGYÁRTÁS</p>
    </div>

    <div class="col">
      <h2>About (Right)</h2>
      <p>More supporting information or details.</p>
    </div>
  </div>

  <div class="yellow" style="height: 300px; margin-top: 2rem;">
    <!-- Placeholder for image later -->
  </div>
</section>

<section id="contact">
  <h1>KÉRDÉSED VAN?</h1>
  <div>Keress minket bátran:</div>

  <form onsubmit={handleSubmit}>
    <input
      type="text"
      placeholder="Your name"
      bind:value={name}
      required
    />

    <input
      type="email"
      placeholder="Your email"
      bind:value={email}
      required
    />

    <textarea
      rows="5"
      placeholder="Your message"
      bind:value={message}
      required
    ></textarea>

    <button type="submit">Send</button>
  </form>
</section>