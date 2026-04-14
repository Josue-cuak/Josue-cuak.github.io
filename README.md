<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
  <title>🌿 Herbario Elegante · Plantas y Árboles</title>
  <!-- Fuentes elegantes -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,500;0,600;1,400&family=Quicksand:wght@300;400;500&display=swap" rel="stylesheet">
  <!-- AOS (Animate On Scroll) -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/aos/2.3.4/aos.css">
  <!-- Font Awesome -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      background-color: #0a2f1f;
      background-image: radial-gradient(circle at 20% 30%, #1a4a2e 0%, #052010 100%);
      color: #f0f2e9;
      font-family: 'Quicksand', sans-serif;
      line-height: 1.6;
      padding: 2rem 1.5rem;
      min-height: 100vh;
    }

    .wrapper {
      max-width: 1600px;
      margin: 0 auto;
    }

    .hero {
      text-align: center;
      margin-bottom: 4rem;
      position: relative;
    }

    .hero h1 {
      font-family: 'Playfair Display', serif;
      font-size: 4rem;
      font-weight: 600;
      letter-spacing: 4px;
      text-transform: uppercase;
      background: linear-gradient(135deg, #f3e9c0, #d4d9b2);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
      text-shadow: 0 8px 20px rgba(0,0,0,0.5);
      margin-bottom: 0.5rem;
    }

    .hero p {
      font-size: 1.3rem;
      font-weight: 300;
      color: #c0cfb2;
      border-bottom: 1px solid #5b8c5c;
      display: inline-block;
      padding-bottom: 8px;
      backdrop-filter: blur(2px);
    }

    .hero i {
      color: #bc9b5a;
      margin: 0 10px;
    }

    .plant-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(360px, 1fr));
      gap: 2.2rem;
    }

    .plant-card {
      background: rgba(20, 45, 30, 0.55);
      backdrop-filter: blur(12px);
      -webkit-backdrop-filter: blur(12px);
      border: 1px solid rgba(180, 210, 150, 0.2);
      border-radius: 42px;
      padding: 1.8rem 1.5rem 2rem;
      box-shadow: 0 30px 40px -20px rgba(0,0,0,0.7), 0 0 0 1px rgba(120, 160, 90, 0.1) inset;
      transition: transform 0.25s ease, box-shadow 0.4s;
      display: flex;
      flex-direction: column;
    }

    .plant-card:hover {
      transform: translateY(-10px);
      box-shadow: 0 40px 50px -15px #00000080, 0 0 0 2px #7faa6b33 inset;
      border-color: #a6c89b55;
    }

    .card-title {
      font-family: 'Playfair Display', serif;
      font-size: 2.1rem;
      font-weight: 600;
      color: #f3efda;
      margin-bottom: 0.25rem;
      line-height: 1.2;
      border-left: 6px solid #b89b5b;
      padding-left: 18px;
      text-shadow: 0 2px 5px #00000040;
    }

    .scientific-name {
      font-style: italic;
      font-weight: 400;
      color: #bfd8b6;
      margin-bottom: 1.2rem;
      font-size: 1.1rem;
      letter-spacing: 0.5px;
      padding-left: 24px;
    }

    .leaf-section {
      display: flex;
      gap: 16px;
      margin: 15px 0 20px;
      align-items: flex-start;
    }

    .leaf-info {
      flex: 2;
    }

    .leaf-info h3, .fruit-section h3, .desc-section h3 {
      font-family: 'Playfair Display', serif;
      font-size: 1.3rem;
      font-weight: 500;
      color: #d4c9a6;
      margin-bottom: 6px;
      letter-spacing: 0.5px;
      border-bottom: 1px dashed #7e9a6e;
      display: inline-block;
    }

    .leaf-img {
      flex: 1;
      min-width: 100px;
      border-radius: 24px;
      overflow: hidden;
      box-shadow: 0 10px 20px -5px #00000060;
      border: 1px solid #9bb88966;
      background: #1f3e28;
      aspect-ratio: 1/1;
    }

    .leaf-img img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      display: block;
      transition: transform 0.5s;
    }

    .leaf-img img:hover {
      transform: scale(1.08);
    }

    .tree-img {
      margin: 20px 0 16px;
      border-radius: 32px;
      overflow: hidden;
      box-shadow: 0 18px 25px -8px black;
      border: 1px solid #a7bb9466;
      background: #1f3e28;
    }

    .tree-img img {
      width: 100%;
      height: 200px;
      object-fit: cover;
      display: block;
      transition: transform 0.7s;
    }

    .tree-img img:hover {
      transform: scale(1.03);
    }

    .fruit-section, .desc-section {
      margin-top: 10px;
    }

    .desc-section p, .fruit-section p {
      color: #e0e6d4;
      font-weight: 400;
      font-size: 1rem;
    }

    .footer-note {
      margin-top: 5rem;
      text-align: center;
      color: #96a78b;
      font-size: 0.95rem;
    }

    [data-aos] {
      transition-timing-function: cubic-bezier(0.25, 0.46, 0.45, 0.94);
    }

    .img-caption {
      font-size: 0.7rem;
      text-align: right;
      color: #b0bb9a;
      margin-top: 4px;
    }

    i {
      margin-right: 6px;
      color: #c6b27c;
    }

    @media (max-width: 600px) {
      body { padding: 1.2rem 0.8rem; }
      .hero h1 { font-size: 2.5rem; }
      .plant-card { padding: 1.5rem 1rem; }
    }
  </style>
</head>
<body>
<div class="wrapper">
  <div class="hero" data-aos="fade-down" data-aos-duration="1000">
    <h1><i class="fas fa-leaf"></i> BOTÁNICA VIVA <i class="fas fa-seedling"></i></h1>
    <p>· elegancia natural · herbario ilustrado ·</p>
  </div>

  <!-- GRID DE PLANTAS -->
  <div class="plant-grid">
    
    <!-- 1. PATA DE VACA -->
    <div class="plant-card" data-aos="fade-up">
      <div class="card-title">Pata de Vaca</div>
      <div class="scientific-name"><i class="fas fa-tag"></i> Bauhinia variegata</div>
      <div class="leaf-section">
        <div class="leaf-info">
          <h3><i class="fas fa-leaf"></i> Hoja</h3>
          <p><strong>Forma:</strong> Bilobulada, hendidura central.<br><strong>Razón:</strong> Reduce resistencia al viento.</p>
        </div>
        <div class="leaf-img">
          <img src="https://images.pexels.com/photos/1323550/pexels-photo-1323550.jpeg?auto=compress&cs=tinysrgb&w=200" alt="Hoja genérica">
        </div>
      </div>
      <div class="desc-section">
        <h3><i class="fas fa-tree"></i> Descripción</h3>
        <p>Árbol caducifolio de copa extendida, flores grandes similares a orquídeas, en tonos rosa, púrpura o blanco. Muy ornamental.</p>
      </div>
      <div class="fruit-section">
        <h3><i class="fas fa-apple-alt"></i> Fruto</h3>
        <p>Legumbre alargada, aplanada, de color marrón, con varias semillas. No es comestible.</p>
      </div>
      <div class="tree-img">
        <img src="https://images.pexels.com/photos/164024/pexels-photo-164024.jpeg?auto=compress&cs=tinysrgb&w=400" alt="Árbol genérico">
        <div class="img-caption"><i class="fas fa-camera"></i> Árbol tropical</div>
      </div>
    </div>

    <!-- 2. CORALILLO -->
    <div class="plant-card" data-aos="fade-up">
      <div class="card-title">Coralillo</div>
      <div class="scientific-name"><i class="fas fa-tag"></i> Hamelia patens</div>
      <div class="leaf-section">
        <div class="leaf-info">
          <h3><i class="fas fa-leaf"></i> Hoja</h3>
          <p><strong>Forma:</strong> Elíptica a ovada, nervaduras rojizas.<br><strong>Razón:</strong> Coloración por antocianinas.</p>
        </div>
        <div class="leaf-img">
          <img src="https://images.pexels.com/photos/130576/pexels-photo-130576.jpeg?auto=compress&cs=tinysrgb&w=200" alt="Hoja verde">
        </div>
      </div>
      <div class="desc-section">
        <h3><i class="fas fa-tree"></i> Descripción</h3>
        <p>Arbusto perenne de rápido crecimiento, flores tubulares rojo-anaranjadas que atraen colibríes. Ideal para setos.</p>
      </div>
      <div class="fruit-section">
        <h3><i class="fas fa-apple-alt"></i> Fruto</h3>
        <p>Bayas pequeñas que pasan de rojo a negro, jugosas, alimento de aves.</p>
      </div>
      <div class="tree-img">
        <img src="https://images.pexels.com/photos/2132171/pexels-photo-2132171.jpeg?auto=compress&cs=tinysrgb&w=400" alt="Arbusto genérico">
      </div>
    </div>

    <!-- 3. ENREDADERA CORALINA -->
    <div class="plant-card" data-aos="fade-up">
      <div class="card-title">Enredadera Coralina</div>
      <div class="scientific-name"><i class="fas fa-tag"></i> Antigonon leptopus</div>
      <div class="leaf-section">
        <div class="leaf-info">
          <h3><i class="fas fa-leaf"></i> Hoja</h3>
          <p><strong>Forma:</strong> Acorazonada, margen ondulado.<br><strong>Razón:</strong> Optimiza captación de luz.</p>
        </div>
        <div class="leaf-img">
          <img src="https://images.pexels.com/photos/1074646/pexels-photo-1074646.jpeg?auto=compress&cs=tinysrgb&w=200" alt="Hoja corazón">
        </div>
      </div>
      <div class="desc-section">
        <h3><i class="fas fa-tree"></i> Descripción</h3>
        <p>Enredadera vigorosa con zarcillos, produce racimos de flores rosadas o blancas. Cubre pérgolas rápidamente.</p>
      </div>
      <div class="fruit-section">
        <h3><i class="fas fa-apple-alt"></i> Fruto</h3>
        <p>Aquenio pequeño, envuelto en el cáliz persistente. No es de interés culinario.</p>
      </div>
      <div class="tree-img">
        <img src="https://images.pexels.com/photos/212324/pexels-photo-212324.jpeg?auto=compress&cs=tinysrgb&w=400" alt="Enredadera">
      </div>
    </div>

    <!-- 4. ALMENDRO TROPICAL -->
    <div class="plant-card" data-aos="fade-up">
      <div class="card-title">Almendro Tropical</div>
      <div class="scientific-name"><i class="fas fa-tag"></i> Terminalia catappa</div>
      <div class="leaf-section">
        <div class="leaf-info">
          <h3><i class="fas fa-leaf"></i> Hoja</h3>
          <p><strong>Forma:</strong> Obovada, grande, coriácea.<br><strong>Razón:</strong> Hojas grandes para sombra.</p>
        </div>
        <div class="leaf-img">
          <img src="https://images.pexels.com/photos/109316/pexels-photo-109316.jpeg?auto=compress&cs=tinysrgb&w=200" alt="Hoja ancha">
        </div>
      </div>
      <div class="desc-section">
        <h3><i class="fas fa-tree"></i> Descripción</h3>
        <p>Árbol de copa estratificada, caducifolio, muy usado en zonas costeras. Las hojas se usan en acuarios.</p>
      </div>
      <div class="fruit-section">
        <h3><i class="fas fa-apple-alt"></i> Fruto</h3>
        <p>Drupa elipsoide con mesocarpio fibroso, almendra comestible de sabor similar a la nuez.</p>
      </div>
      <div class="tree-img">
        <img src="https://images.pexels.com/photos/159807/pexels-photo-159807.jpeg?auto=compress&cs=tinysrgb&w=400" alt="Árbol grande">
      </div>
    </div>

    <!-- 5. MURALLA / JAZMÍN NARANJA -->
    <div class="plant-card" data-aos="fade-up">
      <div class="card-title">Muralla / Jazmín Naranja</div>
      <div class="scientific-name"><i class="fas fa-tag"></i> Murraya paniculata</div>
      <div class="leaf-section">
        <div class="leaf-info">
          <h3><i class="fas fa-leaf"></i> Hoja</h3>
          <p><strong>Forma:</strong> Compuesta, pinnada, folíolos ovados brillantes.<br><strong>Razón:</strong> Maximiza luz en setos densos.</p>
        </div>
        <div class="leaf-img">
          <img src="https://images.pexels.com/photos/1322302/pexels-photo-1322302.jpeg?auto=compress&cs=tinysrgb&w=200" alt="Hojas brillantes">
        </div>
      </div>
      <div class="desc-section">
        <h3><i class="fas fa-tree"></i> Descripción</h3>
        <p>Arbusto perenne, muy aromático. Flores blancas con perfume a azahar. Ideal para cercos vivos.</p>
      </div>
      <div class="fruit-section">
        <h3><i class="fas fa-apple-alt"></i> Fruto</h3>
        <p>Baya ovoide rojo-anaranjada, atractiva para aves, aunque no es comestible para humanos.</p>
      </div>
      <div class="tree-img">
        <img src="https://images.pexels.com/photos/1007657/pexels-photo-1007657.jpeg?auto=compress&cs=tinysrgb&w=400" alt="Seto verde">
      </div>
    </div>

    <!-- 6. FICUS BENJAMINA -->
    <div class="plant-card" data-aos="fade-up">
      <div class="card-title">Ficus Benjamina</div>
      <div class="scientific-name"><i class="fas fa-tag"></i> Ficus benjamina</div>
      <div class="leaf-section">
        <div class="leaf-info">
          <h3><i class="fas fa-leaf"></i> Hoja</h3>
          <p><strong>Forma:</strong> Ovado-elíptica, ápice acuminado.<br><strong>Razón:</strong> Punta alargada para escurrir agua.</p>
        </div>
        <div class="leaf-img">
          <img src="https://images.pexels.com/photos/459225/pexels-photo-459225.jpeg?auto=compress&cs=tinysrgb&w=200" alt="Hoja ficus">
        </div>
      </div>
      <div class="desc-section">
        <h3><i class="fas fa-tree"></i> Descripción</h3>
        <p>Árbol perenne de copa llorona, muy usado en interiores y paisajismo. Raíces aéreas en climas húmedos.</p>
      </div>
      <div class="fruit-section">
        <h3><i class="fas fa-apple-alt"></i> Fruto</h3>
        <p>Sicono (higo) pequeño, rojizo, en pares. No comestible, pero importante para fauna.</p>
      </div>
      <div class="tree-img">
        <img src="https://images.pexels.com/photos/161860/pexels-photo-161860.jpeg?auto=compress&cs=tinysrgb&w=400" alt="Ficus">
      </div>
    </div>

    <!-- 7. ÁRBOL DE GUAYABA -->
    <div class="plant-card" data-aos="fade-up">
      <div class="card-title">Guayabo</div>
      <div class="scientific-name"><i class="fas fa-tag"></i> Psidium guajava</div>
      <div class="leaf-section">
        <div class="leaf-info">
          <h3><i class="fas fa-leaf"></i> Hoja</h3>
          <p><strong>Forma:</strong> Elíptica, opuesta, aromática.<br><strong>Razón:</strong> Aceites esenciales como defensa.</p>
        </div>
        <div class="leaf-img">
          <img src="https://images.pexels.com/photos/594608/pexels-photo-594608.jpeg?auto=compress&cs=tinysrgb&w=200" alt="Hoja aromática">
        </div>
      </div>
      <div class="desc-section">
        <h3><i class="fas fa-tree"></i> Descripción</h3>
        <p>Árbol pequeño, corteza lisa que se desprende. Flores blancas con estambres vistosos.</p>
      </div>
      <div class="fruit-section">
        <h3><i class="fas fa-apple-alt"></i> Fruto</h3>
        <p>Baya globosa, cáscara verde-amarilla, pulpa dulce con muchas semillas. Alto contenido de vitamina C.</p>
      </div>
      <div class="tree-img">
        <img src="https://images.pexels.com/photos/1676432/pexels-photo-1676432.jpeg?auto=compress&cs=tinysrgb&w=400" alt="Guayabo">
      </div>
    </div>

    <!-- 8. CORDYLINE FRUTICOSA -->
    <div class="plant-card" data-aos="fade-up">
      <div class="card-title">Cordyline / Ti</div>
      <div class="scientific-name"><i class="fas fa-tag"></i> Cordyline fruticosa</div>
      <div class="leaf-section">
        <div class="leaf-info">
          <h3><i class="fas fa-leaf"></i> Hoja</h3>
          <p><strong>Forma:</strong> Lanceolada, larga, color rojizo/variegado.<br><strong>Razón:</strong> Pigmentación por antocianinas.</p>
        </div>
        <div class="leaf-img">
          <img src="https://images.pexels.com/photos/1363876/pexels-photo-1363876.jpeg?auto=compress&cs=tinysrgb&w=200" alt="Hoja rojiza">
        </div>
      </div>
      <div class="desc-section">
        <h3><i class="fas fa-tree"></i> Descripción</h3>
        <p>Arbusto tropical de tallos delgados, hojas agrupadas en el ápice. Muy ornamental por su follaje.</p>
      </div>
      <div class="fruit-section">
        <h3><i class="fas fa-apple-alt"></i> Fruto</h3>
        <p>Bayas rojas esféricas, raramente producidas en cultivo; atractivas para aves.</p>
      </div>
      <div class="tree-img">
        <img src="https://images.pexels.com/photos/1458434/pexels-photo-1458434.jpeg?auto=compress&cs=tinysrgb&w=400" alt="Cordyline">
      </div>
    </div>

    <!-- 9. CASUARINA -->
    <div class="plant-card" data-aos="fade-up">
      <div class="card-title">Casuarina</div>
      <div class="scientific-name"><i class="fas fa-tag"></i> Casuarina equisetifolia</div>
      <div class="leaf-section">
        <div class="leaf-info">
          <h3><i class="fas fa-leaf"></i> Hoja</h3>
          <p><strong>Forma:</strong> Escamas diminutas; ramillas como agujas.<br><strong>Razón:</strong> Reducción foliar para evitar pérdida de agua.</p>
        </div>
        <div class="leaf-img">
          <img src="https://images.pexels.com/photos/884549/pexels-photo-884549.jpeg?auto=compress&cs=tinysrgb&w=200" alt="Agujas de pino">
        </div>
      </div>
      <div class="desc-section">
        <h3><i class="fas fa-tree"></i> Descripción</h3>
        <p>Árbol perennifolio de porte columnar, resistente a vientos salinos. Fija nitrógeno por simbiosis.</p>
      </div>
      <div class="fruit-section">
        <h3><i class="fas fa-apple-alt"></i> Fruto</h3>
        <p>Cono leñoso globoso, con pequeñas sámaras aladas.</p>
      </div>
      <div class="tree-img">
        <img src="https://images.pexels.com/photos/159398/pexels-photo-159398.jpeg?auto=compress&cs=tinysrgb&w=400" alt="Árbol alto">
      </div>
    </div>

    <!-- 10. FALSA ASHOKA / PINO HINDÚ -->
    <div class="plant-card" data-aos="fade-up">
      <div class="card-title">Falsa Ashoka</div>
      <div class="scientific-name"><i class="fas fa-tag"></i> Polyalthia longifolia</div>
      <div class="leaf-section">
        <div class="leaf-info">
          <h3><i class="fas fa-leaf"></i> Hoja</h3>
          <p><strong>Forma:</strong> Largas, lanceoladas, borde ondulado.<br><strong>Razón:</strong> Forma colgante para reducir calor.</p>
        </div>
        <div class="leaf-img">
          <img src="https://images.pexels.com/photos/115082/pexels-photo-115082.jpeg?auto=compress&cs=tinysrgb&w=200" alt="Hoja larga">
        </div>
      </div>
      <div class="desc-section">
        <h3><i class="fas fa-tree"></i> Descripción</h3>
        <p>Árbol columnar, de rápido crecimiento, muy usado en alineaciones. Copa piramidal estrecha.</p>
      </div>
      <div class="fruit-section">
        <h3><i class="fas fa-apple-alt"></i> Fruto</h3>
        <p>Bayas ovoides verdes a púrpura oscuro, dispuestas en racimos.</p>
      </div>
      <div class="tree-img">
        <img src="https://images.pexels.com/photos/164024/pexels-photo-164024.jpeg?auto=compress&cs=tinysrgb&w=400" alt="Árbol columnar">
      </div>
    </div>

    <!-- 11. ZACATE MORADO -->
    <div class="plant-card" data-aos="fade-up">
      <div class="card-title">Zacate Morado</div>
      <div class="scientific-name"><i class="fas fa-tag"></i> Pennisetum setaceum 'Rubrum'</div>
      <div class="leaf-section">
        <div class="leaf-info">
          <h3><i class="fas fa-leaf"></i> Hoja</h3>
          <p><strong>Forma:</strong> Lineal, estrecha, púrpura intenso.<br><strong>Razón:</strong> Pigmentación para protección UV.</p>
        </div>
        <div class="leaf-img">
          <img src="https://images.pexels.com/photos/145933/pexels-photo-145933.jpeg?auto=compress&cs=tinysrgb&w=200" alt="Hierba morada">
        </div>
      </div>
      <div class="desc-section">
        <h3><i class="fas fa-tree"></i> Descripción</h3>
        <p>Gramínea ornamental, forma macollas densas. Inflorescencias en espigas suaves color rosado-púrpura.</p>
      </div>
      <div class="fruit-section">
        <h3><i class="fas fa-apple-alt"></i> Fruto</h3>
        <p>Cariópside (semilla) en la espiga, poco vistosa; se propaga por división.</p>
      </div>
      <div class="tree-img">
        <img src="https://images.pexels.com/photos/220131/pexels-photo-220131.jpeg?auto=compress&cs=tinysrgb&w=400" alt="Zacate ornamental">
      </div>
    </div>

    <!-- 12. PLANTA VERANERA -->
    <div class="plant-card" data-aos="fade-up">
      <div class="card-title">Veranera / Buganvilia</div>
      <div class="scientific-name"><i class="fas fa-tag"></i> Bougainvillea glabra</div>
      <div class="leaf-section">
        <div class="leaf-info">
          <h3><i class="fas fa-leaf"></i> Hoja</h3>
          <p><strong>Forma:</strong> Ovada, ápice agudo, verde brillante.<br><strong>Razón:</strong> Hojas pequeñas en zonas secas.</p>
        </div>
        <div class="leaf-img">
          <img src="https://images.pexels.com/photos/459282/pexels-photo-459282.jpeg?auto=compress&cs=tinysrgb&w=200" alt="Hoja buganvilia">
        </div>
      </div>
      <div class="desc-section">
        <h3><i class="fas fa-tree"></i> Descripción</h3>
        <p>Arbusto trepador espinoso, famoso por sus brácteas magenta, naranja o blancas. Muy resistente a sequía.</p>
      </div>
      <div class="fruit-section">
        <h3><i class="fas fa-apple-alt"></i> Fruto</h3>
        <p>Aquenio alargado, seco, rodeado por el perianto persistente.</p>
      </div>
      <div class="tree-img">
        <img src="https://images.pexels.com/photos/931177/pexels-photo-931177.jpeg?auto=compress&cs=tinysrgb&w=400" alt="Buganvilia">
      </div>
    </div>

    <!-- 13. PINO -->
    <div class="plant-card" data-aos="fade-up">
      <div class="card-title">Pino</div>
      <div class="scientific-name"><i class="fas fa-tag"></i> Pinus spp.</div>
      <div class="leaf-section">
        <div class="leaf-info">
          <h3><i class="fas fa-leaf"></i> Hoja (acícula)</h3>
          <p><strong>Forma:</strong> Acicular, en fascículos.<br><strong>Razón:</strong> Reduce superficie transpirante.</p>
        </div>
        <div class="leaf-img">
          <img src="https://images.pexels.com/photos/376464/pexels-photo-376464.jpeg?auto=compress&cs=tinysrgb&w=200" alt="Acículas de pino">
        </div>
      </div>
      <div class="desc-section">
        <h3><i class="fas fa-tree"></i> Descripción</h3>
        <p>Árbol perennifolio, resinoso, de gran longevidad. Madera valiosa, forma bosques.</p>
      </div>
      <div class="fruit-section">
        <h3><i class="fas fa-apple-alt"></i> Fruto (cono)</h3>
        <p>Estróbilo leñoso (piña), con semillas aladas (piñones) en algunas especies.</p>
      </div>
      <div class="tree-img">
        <img src="https://images.pexels.com/photos/1061623/pexels-photo-1061623.jpeg?auto=compress&cs=tinysrgb&w=400" alt="Pino">
      </div>
    </div>
  </div>
  
  <div class="footer-note" data-aos="fade">
    <i class="fas fa-feather-alt"></i> Herbario digital · elegancia botánica · imágenes representativas <i class="fas fa-feather-alt"></i>
  </div>
</div>

<script src="https://cdnjs.cloudflare.com/ajax/libs/aos/2.3.4/aos.js"></script>
<script>
  AOS.init({ duration: 900, once: false, offset: 40, easing: 'ease-out-cubic' });
</script>
</body>
</html>
