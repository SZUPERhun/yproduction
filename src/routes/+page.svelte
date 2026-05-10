<script lang="ts">
  import { asset } from '$app/paths';

  const bgImage1 = asset('/IG-11.JPG');
  const bgImage2 = asset('/IG-2.jpg');
  const bgImage3 = asset('/IG-13.JPG');


  let firstName = '';
  let lastName = '';
  let subject = '';
  let senderEmail = '';
  let message = '';

  const recipientEmail = 'info@yproduction.hu';

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

  .text-content {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    width: 100%;
    max-width: 60%;
    margin-left: 20%;
    margin-top: 3%;
  }

  @media (max-width: 767.98px) {
    .text-content {
      display: flex;
      flex-direction: column;
      align-items: flex-start;
      width: 100%;
      margin-left: 1%;
      margin-top: 3%;
    }
  }

  .text-content h2 {
    width: 100%;
    margin: 0 0 1rem 0;
    text-align: left;
  }

  #about .service-group {
    margin: 0.5rem 0;
    font-size: 30px;
    color: white;
    font-family: 'Poppins', sans-serif;
    font-weight: 600;
    padding-left: 20%;
  }

  .yellow-text {
    color: #facc15;
  }

  #about p {
    margin: 0.25rem 0;
  }

  p {
    text-align: justify;
  }

  .yellow {
    background: #facc15;
  }

  #contact {
    min-height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .form-container {
    width: 100%;
    height: 100vh;
    background-image: linear-gradient(rgba(0,0,0,0.7), rgba(0,0,0,0.7)), var(--bg-image2);
    background-size: cover;
    background-position: center;
    color: white;
  }

  .form-div {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    width: 100%;
    min-height: 100%;
    padding: 2rem 0;
  }

  .col-md-6 {
    min-height: 100vh;
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

  .title-text-container {
    width: min(66.66%, 760px);
    background: rgba(0, 0, 0, 0.5);
    padding: 2.5rem 2rem;
    display: flex;
    flex-direction: column;
    gap: 1rem;
    box-shadow: 0 16px 45px rgba(0, 0, 0, 0.18);
  }

  .title-text-container h1,
  .title-text-container p {
    width: 100%;
    text-align: left;
    margin: 0;
  }

  .title-text-container p {
    margin-top: 0.5rem;
    max-width: 100%;
  }

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

  .title-div {
    position: relative;
    height: 500px;
    color: white;
    background-image: var(--bg-image1);
    background-size: cover;
    background-position: center;
  }

  .top-div {
    position: absolute;
    max-width: 60%;
    max-height: 60%;
    left: 40%;
    top: 40%;
    z-index: 2;
  }

  .responsive-image {
    max-width: 100%;
		max-height: 100%;
		object-fit: contain;
  }

  .logo-div {
		height: 100vh;
		display: flex;
		align-items: center;
		justify-content: center;
	}

  @media (max-width: 900px) {
    .top-div {
      left: 10%;
      top: 30%;
    }

    .top-div h1 {
      font-size: 22px;
    }

    h2.header {
      font-size: 32px;
    }

    .top-div p {
      font-size: 18px;
    }

    .service-group {
      padding-left: 5%;
    }
  }

  .hero {
    width: 100%;
    height: 100vh;
    background-image: var(--bg-image3);
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
    position: relative;
    image-rendering: auto;
  }

  /* dark overlay for contrast */
  .overlay {
    position: absolute;
    inset: 0;
    background: rgba(0, 0, 0, 0.55);
    backdrop-filter: blur(2px);
  }

  /* ensures content is above overlay */
  .container {
    position: relative;
    z-index: 2;
  }

  /* makes video feel like a real UI element */
  .video-card {
    border-radius: 16px;
    overflow: hidden;
    background: rgba(0, 0, 0, 0.3);
    border: 1px solid rgba(255, 255, 255, 0.1);
  }

  iframe {
    width: 100%;
    height: 100%;
  }
</style>

<div class="nav-container">
  <nav>
    <a href="#home">Rólunk</a>
    <a href="#about">Szolgáltatások</a>
    <a href="#contact">Kontakt</a>
  </nav>
</div>

<div class="row justify-content-center">
  <div class="title-div col-12" style={`--bg-image1: url('${bgImage1}')`}>
    <div class="top-div title-text-container">
      <h1 class="header">Y PRODUCTION</h1>
      <p>Hangot adunk a történetnek.</p>
    </div>
  </div>
</div>

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

    <div class="col-md-6 logo-div">
      <img src={asset("/y_production_logo_RGB.svg")} alt="Y Production logo" class="responsive-image" />
    </div>
  </div>
</section>

<section class="hero d-flex align-items-center justify-content-center" style={`--bg-image3: url('${bgImage3}')`}>
	<div class="overlay"></div>

	<div class="container position-relative">
		<div class="row justify-content-center">
			<div class="col-12 col-md-9 col-lg-7">
				
				<div class="video-card shadow-lg">
					<div class="ratio ratio-16x9 rounded overflow-hidden">
						<iframe
							src="https://www.youtube.com/embed/dQw4w9WgXcQ"
							title="YouTube video"
							allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
							allowfullscreen
						></iframe>
					</div>
				</div>

			</div>
		</div>
	</div>
</section>

<section id="about">
  <div class="row">
    <div class="col-md-6">
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
  <div class="row form-container" style={`--bg-image2: url('${bgImage2}')`}>
    <div class="col-md-12 form-div">
      <h1 class="header">KÉRDÉSED VAN?</h1>
      <p>Keress minket bátran:</p>

      <form onsubmit={handleSubmit}>
        <div class="form-row">
          <input
            class="form-control"
            type="text"
            placeholder="Vezetéknév"
            bind:value={lastName}
            required
          />
          <input
            class="form-control"
            type="text"
            placeholder="Keresztnév"
            bind:value={firstName}
            required
          />
        </div>

        <input
          class="form-control"
          type="email"
          placeholder="E-mail cím"
          bind:value={senderEmail}
          required
        />

        <input
          class="form-control"
          type="text"
          placeholder="Tárgy"
          bind:value={subject}
          required
        />

        <textarea
          class="form-control"
          rows="6"
          placeholder="Üzenet"
          bind:value={message}
          required
        ></textarea>

        <button class="btn btn-primary" type="submit">Üzenet küldése</button>
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
      <p>Budapest, Magyarország</p>
    </div>
  </div>

  <div class="footer-bottom">
    <p>© 2026 Y Production. Minden jog fenntartva.</p>
  </div>
</section>