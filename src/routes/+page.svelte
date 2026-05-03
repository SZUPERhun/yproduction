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
  .nav-container {
    top: 0;
    width: 100%;
    z-index: 10;
  }

  .header {
    font-family: 'Poppins', sans-serif;
    font-weight: 600;
    font-size: 56px;
    text-align: left;
  }

  .avenir-light  {
    font-family: 'Nunito', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, sans-serif;
    font-weight: 200;
  }

  nav {
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
  }

  .row {
    display: flex;
    min-height: 100vh;
    width: 100%;
  }

  .col-md-6 {
    flex: 1;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    padding: 2rem;
    text-align: center;
  }

  /* Text content wrapper for consistent width */
  .text-content {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    width: 100%;
    max-width: 400px;
  }

  .text-content h1,
  .text-content h2 {
    width: 100%;
    margin: 0 0 1rem 0;
    text-align: left;
  }

  .text-content p {
    width: 100%;
    text-align: left;
  }

  /* About section left column specific styling */
  #about .col-md-6.blue {
    justify-content: center;
    align-items: center;
    text-align: left;
  }

  #about .service-group {
    margin: 0.5rem 0;
    font-size: 30px;
    color: white;
    font-family: 'Poppins', sans-serif;
    font-weight: 600;
  }

  .yellow-text {
    color: #facc15;
  }

  #about hr {
    border: none;
    border-top: 1px solid rgba(255, 255, 255, 0.3);
    margin: 0.5rem 0;
  }

  #about p {
    margin: 0.25rem 0;
  }

  p {
    text-align: justify;
  }

  /* Mobile: Stack columns vertically */
  @media (max-width: 767.98px) {
    .row {
      flex-direction: column;
      min-height: auto;
    }

    .col-md-6 {
      min-height: 100vh;
      width: 100%;
    }
  }

  .yellow {
    background: #facc15;
  }

  .blue {
    background: rgb(0, 119, 255);
  }

  .green {
    background: rgb(106, 255, 0);
    height: calc(100vh - 80px);
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
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

  .about-content {
    text-align: left;
  }
</style>

<div class="nav-container">
  <nav>
    <a href="#home">Rólunk</a>
    <a href="#about">Szolgáltatások</a>
    <a href="#contact">Kontakt</a>
  </nav>
</div>


<section class="green">
  <h1>My Product</h1>
  <p>A simple sentence describing what this product does.</p>
</section>

<section id="home">
  <div class="row">
    <div class="col-md-6 yellow">
      <div class="text-content">
        <h2 class="header">RÓLUNK</h2>
        <p>
          Az Y Production 2018 óta a hazai televíziós és filmes hangutómunka egyik kiemelkedő szereplője.
        </p>
        <p>
          Dinamikusan fejlődő cégünk professzionális hangkeveréssel, zenei szerkesztéssel, valamint filmes utómunkákkal foglalkozik.
        </p>
        <p>
          Partnereink között megtalálhatók a vezető televíziós csatornák és streaming platformok:
          RTL, TV2, ViaSat, MTVA, HBO.
        </p>
        <p>
          Tevékenységünk kiterjed podcastok gyártására - többek között az IstenEst és a Ki Mit Tube műsorok felvétele is nálunk készül.
        </p>
        <p>
          Továbbá próbatermek és stúdióhelyiségek bérbeadására, valamint professzionális technikai eszközök biztosítására is.
        </p>
        <p>
        Valamint legújabb szolgáltatásunk az AI tartalmak gyártása, melyre egy egész csapatunk specializálódott. Legyen szó reklámokról, tv műsorokról, social média tartalmakról.
        </p>
      </div>
    </div>

    <div class="col-md-6 blue fullscreen">
      test
    </div>
  </div>
</section>

<section id="about">
  <div class="row">
    <div class="col-md-6 header about-content">
      <div class="service-group">
        <p class="yellow-text">SZOLGÁLTATÁSAINK</p>
        <p>HANGFELVÉTEL</p>
        <p>HANGUTÓMUNKA</p>
        <p>ZENEI SZERKESZTÉS</p>
        <p>SZINKRON</p>
        <br />
        <p class="yellow-text">STÚDIÓ BÉRBEADÁS</p>
        <p>PRÓBATEREM</p>
        <p>TÁNCTEREM</p>
        <p>PODCAST STÚDIÓ</p>
        <br />
        <p class="yellow-text">RENTAL</p>
        <p>KAMERATECHNIKA</p>
        <p>HANGTECHNIKA</p>
        <br />
        <p class="yellow-text">AI TARTALOMGYÁRTÁS</p>
      </div>
    </div>

    <div class="col-md-6 yellow">
      <div class="text-content">
        <h2 class="header">REFERENCIÁK</h2>
        X-Faktor • Csillag születik • Megasztár • Házasság Első Látásra • SztárBox • Next Top Model Hungary • Password • Lego Masters Hungary • Nyerő Páros • Kalandra Fal • Az Erőd • Kincsvadászok • Gáspárék • Mém Over • Kivele • Kapóra • Útközben Elmeséled • Kabát FC • A híd • The Voice • Hal a tortán • Séfek séfe • Survivor • Rich Kids Hungary • Virtuózok V4+ • Farm VIP • Vigyázat, gyerekkel vagyok! • Párharc • Ide süss! • Ninja Warrior Hungary • Pepe’s Beach Bar • Mintaapák • Összezárva Hajdú Péterrel • A Piramis • Álarcos énekes • Bezár a bazár • Kapd el, ha tudsz! • Ázsia Expressz • Fuss család, fuss • Ifjú tudósok • Partyzánok • Hungary’s Got Talent • Kicsi Óriások • Drágám, add az életed! • Extreme Activity • Annyit ésszel, mint erővel • MasterChef Junior • MasterChef VIP 2 • Pumpedék • Észbontók • Feleségek luxuskivitelben • Kicsi Gesztenye Klub • Showder Klub • Activity Ábel Anitával • Legyen Ön is Milliomos • Made in Karantén • Nagy Ő • Pandora szelencéje • Csillag születik • Jobb később, mint soha • Álommeló • Kísértés • Celeb vagyok, ments ki innen! • Nagy Színpad • Való Világ • Love Island • Házasodna a gazda • Sztárban sztár leszek! • Van életünk • Ébredj velünk! • Vacsorakirály • Nagy szám • Dancing with the Stars
      </div>
      
    </div>
  </div>
</section>

<section id="contact blue">
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