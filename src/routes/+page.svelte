<script lang="ts">
  let firstName = '';
  let lastName = '';
  let subject = '';
  let senderEmail = '';
  let message = '';

  const recipientEmail = 'info@yproduction.hu'; // Replace with the email you want to receive messages

  function handleSubmit(e: Event) {
    e.preventDefault();

    const fullName = `${firstName} ${lastName}`.trim();
    const mailtoSubject = encodeURIComponent(subject);
    const mailtoBody = encodeURIComponent(
      `From: ${fullName} (${senderEmail})\n\n${message}`
    );
    const mailtoLink = `mailto:${recipientEmail}?subject=${mailtoSubject}&body=${mailtoBody}`;

    window.location.href = mailtoLink;
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

  section.footer {
    min-height: auto;
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

  #contact {
    min-height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .form-container {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    width: 100%;
    min-height: 100%;
    padding: 2rem;
  }

  #contact form {
    width: 100%;
    max-width: 560px;
    display: flex;
    flex-direction: column;
    gap: 1rem;
  }

  .form-row {
    display: flex;
    gap: 1rem;
    width: 100%;
    flex-wrap: wrap;
  }

  .form-row input {
    flex: 1;
    min-width: 150px;
  }

  .form-control {
    width: 100%;
    padding: 0.85rem 1rem;
    font-size: 1rem;
    border-radius: 0.35rem;
    border: 1px solid rgba(255, 255, 255, 0.35);
    background: rgba(255, 255, 255, 0.08);
    color: white;
  }

  .form-control::placeholder {
    color: rgba(255, 255, 255, 0.75);
  }

  .btn {
    padding: 0.85rem 1.25rem;
    border: none;
    border-radius: 0.35rem;
    cursor: pointer;
  }

  .btn-primary {
    background: #222;
    color: white;
  }

  .btn-primary:hover {
    background: #111;
  }

  .footer {
    background: #111;
    color: rgba(255, 255, 255, 0.9);
    padding: 3rem 1.5rem;
    text-align: center;
  }

  .footer .footer-content {
    max-width: 1100px;
    margin: 0 auto;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    gap: 1.5rem;
    align-items: flex-start;
  }

  .footer .footer-block {
    flex: 1 1 220px;
    min-width: 220px;
    text-align: left;
  }

  .footer .footer-block h3 {
    margin-bottom: 1rem;
    font-size: 1.15rem;
  }

  .footer .footer-block p,
  .footer .footer-block a {
    color: rgba(255, 255, 255, 0.75);
    text-decoration: none;
    margin: 0.35rem 0;
    display: block;
  }

  .footer .footer-bottom {
    margin-top: 2rem;
    font-size: 0.95rem;
    color: rgba(255, 255, 255, 0.6);
  }

  .green {
    background: rgb(106, 255, 0);
    height: calc(100vh - 80px);
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    padding: 2rem;
  }

  .title-container {
    width: min(66.66%, 760px);
    background: rgba(0, 0, 0, 0.5);
    padding: 2.5rem 2rem;
    display: flex;
    flex-direction: column;
    gap: 1rem;
    box-shadow: 0 16px 45px rgba(0, 0, 0, 0.18);
  }

  .title-container h1,
  .title-container p {
    width: 100%;
    text-align: left;
    margin: 0;
  }

  .title-container p {
    margin-top: 0.5rem;
    max-width: 90%;
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
  <div class="title-container">
    <h1 class="header">Y PRODUCTION</h1>
    <p>Hangot adunk a történetnek.</p>
  </div>
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

    <div class="col-md-6 blue">
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
        <p>X-Faktor • 
          Csillag születik • 
          Megasztár • 
          Házasság Első Látásra • 
          SztárBox • 
          Next Top Model Hungary • 
          Password • 
          Lego Masters Hungary • 
          Nyerő Páros • 
          Kalandra Fal • 
          Az Erőd • 
          Kincsvadászok • 
          Gáspárék • 
          Mém Over • 
          Kivele • 
          Kapóra • 
          Útközben Elmeséled • 
          Kabát FC • 
          A híd • 
          The Voice • 
          Hal a tortán 
          • Séfek séfe • 
          Survivor • 
          Rich Kids Hungary • 
          Virtuózok V4+ • 
          Farm VIP • 
          igyázat, gyerekkel vagyok! • 
          Párharc • 
          Ide süss! • 
          Ninja Warrior Hungary • 
          Pepe’s Beach Bar • 
          Mintaapák • 
          Összezárva Hajdú Péterrel • 
          A Piramis • 
          Álarcos énekes • 
          Bezár a bazár • 
          Kapd el, ha tudsz! • 
          Ázsia Expressz • 
          Fuss család, fuss • 
          Ifjú tudósok • 
          Partyzánok • 
          Hungary’s Got Talent • 
          Kicsi Óriások • 
          Drágám, add az életed! • 
          Extreme Activity • 
          Annyit ésszel, mint erővel • 
          MasterChef Junior • 
          MasterChef VIP 2 • 
          Pumpedék • 
          Észbontók • 
          Feleségek luxuskivitelben • 
          Kicsi Gesztenye Klub • 
          Showder Klub • 
          Activity Ábel Anitával • 
          Legyen Ön is Milliomos • 
          Made in Karantén • 
          Nagy Ő • 
          Pandora szelencéje • 
          Csillag születik • 
          Jobb később, mint soha • 
          Álommeló • 
          Kísértés • 
          Celeb vagyok, ments ki innen! • 
          Nagy Színpad • 
          Való Világ • 
          Love Island • 
          Házasodna a gazda • 
          Sztárban sztár leszek! • 
          Van életünk • Ébredj velünk! • 
          Vacsorakirály • 
          Nagy szám • 
          Dancing with the Stars • 
          IstenEst • 
          Ki Mit Tube
        </p>
      </div>
      
    </div>
  </div>
</section>

<section id="contact">
  <div class="row">
    <div class="col-md-12 blue form-container">
      <h1 class="header">KÉRDÉSED VAN?</h1>
      <p>Keress minket bátran:</p>

      <form onsubmit={handleSubmit}>
        <div class="form-row">
          <input
            class="form-control"
            type="text"
            placeholder="First name"
            bind:value={firstName}
            required
          />
          <input
            class="form-control"
            type="text"
            placeholder="Last name"
            bind:value={lastName}
            required
          />
        </div>

        <input
          class="form-control"
          type="email"
          placeholder="Your email"
          bind:value={senderEmail}
          required
        />

        <input
          class="form-control"
          type="text"
          placeholder="Subject"
          bind:value={subject}
          required
        />

        <textarea
          class="form-control"
          rows="6"
          placeholder="Your message"
          bind:value={message}
          required
        ></textarea>

        <button class="btn btn-primary" type="submit">Send message</button>
      </form>
    </div>
  </div>
</section>

<section class="footer">
  <div class="footer-content">
    <div class="footer-block">
      <h3>Y Production</h3>
      <p>Professzionális hangutómunka, hangfelvétel és AI tartalomgyártás.</p>
    </div>

    <div class="footer-block">
      <h3>Kapcsolat</h3>
      <a href="mailto:info@yproduction.hu">info@yproduction.hu</a>
      <a href="tel:+36123456789">+36 1 234 5678</a>
      <p>Budapest, Magyarország</p>
    </div>

    <div class="footer-block">
      <h3>Nyitvatartás</h3>
      <p>Hétfő–Péntek: 09:00–18:00</p>
      <p>Szombat: 10:00–14:00</p>
      <p>Vasárnap: Zárva</p>
    </div>
  </div>

  <div class="footer-bottom">
    <p>© 2026 Y Production. Minden jog fenntartva.</p>
  </div>
</section>