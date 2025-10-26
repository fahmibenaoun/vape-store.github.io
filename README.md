<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Vape Store Shop</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>

  <header>
    <div class="logo">
      <img src="images/logo-vape-store.jpg.png" alt="Logo Vape Store Shop">
      Vape Store Shop
    </div>

    <div class="phone">
      📞 <a href="tel:+21653509481">+216 53 509 481</a>
    </div>

    <nav>
      <ul>
        <li><a href="#hero">Accueil</a></li>
        <li><a href="#products">Produits</a></li>
        <li><a href="#about">À propos</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </nav>
  </header>

  <section class="hero reveal" id="hero">
    <h1>Bienvenue sur Vape Store Shop</h1>
    <p>Découvrez nos produits modernes et innovants.</p>
    <a href="#products" class="btn">Voir les produits</a>
  </section>

  <section class="products reveal" id="products">
    <h2>Nos Produits</h2>
    <div class="product-list">

      <div class="product-card reveal">
        <img src="images/puff-falcon.jpg" alt="Puff Falcon JNR Rechargeable">
        <h3>Puff Falcon JNR Rechargeable</h3>
        <p>Un goût unique et une vapeur douce pour une expérience inoubliable.</p>
        <span>65 dt</span>
      </div>

      <div class="product-card reveal">
        <img src="images/vape-produit2.jpg" alt="Vape Pro Max">
        <h3>Vape Pro Max</h3>
        <p>Design élégant et puissance optimale pour les amateurs exigeants.</p>
        <span>80 dt</span>
      </div>

      <div class="product-card reveal">
        <img src="images/NEXPOD-RECHARGABLE.jpg" alt="NEXPOD Rechargeable">
        <h3>NEXPOD Rechargeable</h3>
        <p>Une cigarette électronique rechargeable, élégante et performante.</p>
        <span>45 dt</span>
      </div>

      <div class="product-card reveal">
        <img src="images/OXBAR-30K.jpg" alt="OXBAR 30K">
        <h3>OXBAR 30K</h3>
        <p>Un modèle compact et puissant pour une expérience durable.</p>
        <span>60 dt</span>
      </div>

      <div class="product-card reveal">
        <img src="images/OXBAR-30K-2.jpg" alt="OXBAR 30K-2">
        <h3>OXBAR 30K-2</h3>
        <p>Version améliorée du OXBAR 30K avec design optimisé.</p>
        <span>60 dt</span>
      </div>

      <div class="product-card reveal">
        <img src="images/OXBAR-30K-3.jpg" alt="OXBAR 30K-3">
        <h3>OXBAR 30K-3</h3>
        <p>Modèle dernier cri OXBAR, performance et autonomie maximales.</p>
        <span>60 dt</span>
      </div>

      <div class="product-card reveal">
        <img src="images/Vozol-25k-Shisha.jpg" alt="Vozol 25k Shisha">
        <h3>Vozol 25k Shisha</h3>
        <p>Saveurs inspirées du Shisha pour une expérience originale et douce.</p>
        <span>55 dt</span>
      </div>

      <div class="product-card reveal">
        <img src="images/Vozol-40k.jpg" alt="Vozol 40k">
        <h3>Vozol 40k</h3>
        <p>Haute capacité, vapeur dense et autonomie exceptionnelle.</p>
        <span>60 dt</span>
      </div>

    </div>
  </section>

  <section class="about reveal" id="about">
    <h2>À propos</h2>
    <p>Nous sommes une boutique passionnée par les produits de qualité et le service client. 
    Vape Store Shop s’engage à offrir le meilleur de la vape moderne.</p>
  </section>

  <section class="contact reveal" id="contact">
    <h2>Contactez-nous</h2>
    <p>Pour toute question, appelez-nous au : <a href="tel:+21653509481">53 509 481</a></p>
  </section>

  <footer>
    &copy; 2025 Vape Store Shop - Tous droits réservés.<br>
    📞 <a href="tel:+21653509481">53 509 481</a>
  </footer>

  <script>
    function reveal() {
      const reveals = document.querySelectorAll('.reveal');
      for (let i = 0; i < reveals.length; i++) {
        const windowHeight = window.innerHeight;
        const elementTop = reveals[i].getBoundingClientRect().top;
        const elementVisible = 150;
        if (elementTop < windowHeight - elementVisible) {
          reveals[i].classList.add('active');
        } else {
          reveals[i].classList.remove('active');
        }
      }
    }

    window.addEventListener('scroll', reveal);
    window.addEventListener('load', reveal);
  </script>

</body>
</html>


/* --- Style de base --- */
body {
  font-family: Arial, sans-serif;
  margin: 0;
  background-color: #f5f5f5;
  color: #333;
}

header {
  background-color: #111;
  color: white;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 10px 30px;
  position: sticky;
  top: 0;
  z-index: 1000;
  flex-wrap: wrap;
}

/* --- Logo --- */
.logo {
  display: flex;
  align-items: center;
  gap: 10px;
  font-size: 1.6em;
  font-weight: bold;
}

.logo img {
  width: 85px;
  height: 85px;
  border-radius: 50%;
  object-fit: cover;
}

/* --- Téléphone dans le header --- */
.phone {
  font-size: 1em;
  color: #ff6600;
  font-weight: bold;
}

.phone a {
  color: #ff6600;
  text-decoration: none;
  font-weight: bold;
}

.phone a:hover {
  text-decoration: underline;
}

nav ul {
  list-style: none;
  margin: 0;
  padding: 0;
  display: flex;
  gap: 20px;
}

nav a {
  color: white;
  text-decoration: none;
  font-weight: 500;
  transition: color 0.3s;
}

nav a:hover {
  color: #ff6600;
}

/* --- Section d'accueil (Hero) --- */
.hero {
  background: url('images/COUVERTURE.JPG.png') center/cover no-repeat;
  color: white;
  text-align: center;
  padding: 100px 20px;
  position: relative;
}

/* --- Titre animé --- */
.hero h1 {
  font-size: 3em;
  margin: 0;
  background: linear-gradient(90deg, #ff6600, #ffcc00, #ff6600);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-size: 200% auto;
  animation: gradientMove 4s linear infinite;
}

@keyframes gradientMove {
  0% { background-position: 0% center; }
  100% { background-position: 200% center; }
}

.btn {
  background-color: #ff6600;
  color: white;
  padding: 12px 25px;
  text-decoration: none;
  border-radius: 5px;
  display: inline-block;
  margin-top: 20px;
  transition: background-color 0.3s, transform 0.3s;
}

.btn:hover {
  background-color: #e55b00;
  transform: scale(1.05);
}

.products, .about, .contact {
  padding: 50px 20px;
  text-align: center;
}

.product-list {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 20px;
  margin-top: 30px;
}

.product-card {
  background: white;
  border-radius: 10px;
  box-shadow: 0 4px 10px rgba(0,0,0,0.1);
  width: 250px;
  padding: 15px;
  transition: transform 0.3s, box-shadow 0.3s;
}

.product-card:hover {
  transform: scale(1.05);
  box-shadow: 0 8px 20px rgba(0,0,0,0.2);
}

.product-card img {
  width: 100%;
  border-radius: 10px;
  object-fit: cover;
}

.product-card h3 {
  margin: 10px 0 5px;
}

.product-card span {
  color: #ff6600;
  font-weight: bold;
}

.contact a {
  color: #ff6600;
  text-decoration: none;
  font-weight: bold;
}

.contact a:hover {
  text-decoration: underline;
}

footer {
  background-color: #111;
  color: rgb(198, 192, 192);
  text-align: center;
  padding: 20px;
  margin-top: 30px;
}

/* --- Scroll reveal animations --- */
.reveal {
  opacity: 0;
  transform: translateY(30px);
  transition: all 0.8s ease;
}

.reveal.active {
  opacity: 1;
  transform: translateY(0);
}

/* --- Responsive (téléphone) --- */
@media (max-width: 768px) {
  header {
    flex-direction: column;
    align-items: center;
    text-align: center;
  }

  .phone {
    margin-top: 10px;
  }

  .logo img {
    width: 70px;
    height: 70px;
  }

  .product-list {
    flex-direction: column;
    gap: 15px;
  }
}
