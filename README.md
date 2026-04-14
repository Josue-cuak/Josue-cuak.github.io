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
          <p><strong>Forma:</strong> Bilobulada. <br><strong>Razón:</strong> Reduce resistencia al viento.</p>
        </div>
        <div class="leaf-img">
          <img src="https://upload.wikimedia.org/wikipedia/commons/3/3b/Bauhinia_variegata_leaf.jpg" alt="Hoja pata de vaca" onerror="this.src='https://images.pexels.com/photos/1323550/pexels-photo-1323550.jpeg?auto=compress&cs=tinysrgb&w=200'">
        </div>
      </div>
      <div class="desc-section">
        <h3><i class="fas fa-tree"></i> Descripción</h3>
        <p>Árbol caducifolio, flores grandes similares a orquídeas, en tonos rosa o púrpura.</p>
      </div>
      <div class="fruit-section">
        <h3><i class="fas fa-apple-alt"></i> Fruto</h3>
        <p>Legumbre alargada y aplanada, color marrón.</p>
      </div>
      <div class="tree-img">
        <img src="https://upload.wikimedia.org/wikipedia/commons/4/4b/Bauhinia_variegata_tree.jpg" alt="Árbol orquídea" onerror="this.src='https://images.pexels.com/photos/164024/pexels-photo-164024.jpeg?auto=compress&cs=tinysrgb&w=400'">
        <div class="img-caption"><i class="fas fa-camera"></i> Bauhinia variegata</div>
      </div>
    </div>

    <!-- 2. CORALILLO -->
    <div class="plant-card" data-aos="fade-up">
      <div class="card-title">Coralillo</div>
      <div class="scientific-name"><i class="fas fa-tag"></i> Hamelia patens</div>
      <div class="leaf-section">
        <div class="leaf-info">
          <h3><i class="fas fa-leaf"></i> Hoja</h3>
          <p><strong>Forma:</strong> Elíptica, nervaduras rojizas.</p>
        </div>
        <div class="leaf-img">
          <img src="https://upload.wikimedia.org/wikipedia/commons/5/5a/Hamelia_patens_leaf.jpg" alt="Hoja coralillo" onerror="this.src='https://images.pexels.com/photos/130576/pexels-photo-130576.jpeg?auto=compress&cs=tinysrgb&w=200'">
        </div>
      </div>
      <div class="desc-section">
        <h3><i class="fas fa-tree"></i> Descripción</h3>
        <p>Arbusto perenne, flores tubulares rojo-anaranjadas que atraen colibríes.</p>
      </div>
      <div class="fruit-section">
        <h3><i class="fas fa-apple-alt"></i> Fruto</h3>
        <p>Bayas pequeñas de rojo a negro.</p>
      </div>
      <div class="tree-img">
        <img src="https://upload.wikimedia.org/wikipedia/commons/3/3e/Hamelia_patens_plant.jpg" alt="Coralillo arbusto" onerror="this.src='https://images.pexels.com/photos/2132171/pexels-photo-2132171.jpeg?auto=compress&cs=tinysrgb&w=400'">
      </div>
    </div>

    <!-- 3. ENREDADERA CORALINA -->
    <div class="plant-card" data-aos="fade-up">
      <div class="card-title">Enredadera Coralina</div>
      <div class="scientific-name"><i class="fas fa-tag"></i> Antigonon leptopus</div>
      <div class="leaf-section">
        <div class="leaf-info">
          <h3><i class="fas fa-leaf"></i> Hoja</h3>
          <p><strong>Forma:</strong> Acorazonada, margen ondulado.</p>
        </div>
        <div class="leaf-img">
          <img src="https://upload.wikimedia.org/wikipedia/commons/3/33/Antigonon_leptopus1.JPG" alt="Hoja coralina" onerror="this.src='https://images.pexels.com/photos/1074646/pexels-photo-1074646.jpeg?auto=compress&cs=tinysrgb&w=200'">
        </div>
      </div>
      <div class="desc-section">
        <h3><i class="fas fa-tree"></i> Descripción</h3>
        <p>Enredadera vigorosa, flores rosadas. Cubre pérgolas.</p>
      </div>
      <div class="fruit-section">
        <h3><i class="fas fa-apple-alt"></i> Fruto</h3>
        <p>Aquenio pequeño no comestible.</p>
      </div>
      <div class="tree-img">
        <img src="https://upload.wikimedia.org/wikipedia/commons/2/27/Antigonon_leptopus_vine.jpg" alt="Enredadera coralina" onerror="this.src='https://images.pexels.com/photos/212324/pexels-photo-212324.jpeg?auto=compress&cs=tinysrgb&w=400'">
      </div>
    </div>

    <!-- 4. ALMENDRO TROPICAL -->
    <div class="plant-card" data-aos="fade-up">
      <div class="card-title">Almendro Tropical</div>
      <div class="scientific-name"><i class="fas fa-tag"></i> Terminalia catappa</div>
      <div class="leaf-section">
        <div class="leaf-info">
          <h3><i class="fas fa-leaf"></i> Hoja</h3>
          <p><strong>Forma:</strong> Obovada, grande, coriácea.</p>
        </div>
        <div class="leaf-img">
          <img src="https://upload.wikimedia.org/wikipedia/commons/9/9a/Terminalia_catappa_leaf.jpg" alt="Hoja almendro" onerror="this.src='https://images.pexels.com/photos/109316/pexels-photo-109316.jpeg?auto=compress&cs=tinysrgb&w=200'">
        </div>
      </div>
      <div class="desc-section">
        <h3><i class="fas fa-tree"></i> Descripción</h3>
        <p>Árbol de copa estratificada, hojas caducas rojizas.</p>
      </div>
      <div class="fruit-section">
        <h3><i class="fas fa-apple-alt"></i> Fruto</h3>
        <p>Drupa con almendra comestible.</p>
      </div>
      <div class="tree-img">
        <img src="https://upload.wikimedia.org/wikipedia/commons/a/a1/Terminalia_catappa_tree.jpg" alt="Almendro tropical" onerror="this.src='https://images.pexels.com/photos/159807/pexels-photo-159807.jpeg?auto=compress&cs=tinysrgb&w=400'">
      </div>
    </div>

    <!-- 5. MURALLA / JAZMÍN NARANJA -->
    <div class="plant-card" data-aos="fade-up">
      <div class="card-title">Muralla</div>
      <div class="scientific-name"><i class="fas fa-tag"></i> Murraya paniculata</div>
      <div class="leaf-section">
        <div class="leaf-info">
          <h3><i class="fas fa-leaf"></i> Hoja</h3>
          <p><strong>Forma:</strong> Compuesta pinnada, folíolos ovados.</p>
        </div>
        <div class="leaf-img">
          <img src="https://upload.wikimedia.org/wikipedia/commons/4/4b/Murraya_paniculata_leaf.jpg" alt="Hoja muralla" onerror="this.src='https://images.pexels.com/photos/1322302/pexels-photo-1322302.jpeg?auto=compress&cs=tinysrgb&w=200'">
        </div>
      </div>
      <div class="desc-section">
        <h3><i class="fas fa-tree"></i> Descripción</h3>
        <p>Arbusto aromático, flores blancas con perfume a azahar.</p>
      </div>
      <div class="fruit-section">
        <h3><i class="fas fa-apple-alt"></i> Fruto</h3>
        <p>Baya rojo-anaranjada, atractiva para aves.</p>
      </div>
      <div class="tree-img">
        <img src="https://upload.wikimedia.org/wikipedia/commons/9/9f/Murraya_paniculata_tree.jpg" alt="Jazmín naranja" onerror="this.src='https://images.pexels.com/photos/1007657/pexels-photo-1007657.jpeg?auto=compress&cs=tinysrgb&w=400'">
      </div>
    </div>

    <!-- 6. FICUS BENJAMINA -->
    <div class="plant-card" data-aos="fade-up">
      <div class="card-title">Ficus Benjamina</div>
      <div class="scientific-name"><i class="fas fa-tag"></i> Ficus benjamina</div>
      <div class="leaf-section">
        <div class="leaf-info">
          <h3><i class="fas fa-leaf"></i> Hoja</h3>
          <p><strong>Forma:</strong> Ovado-elíptica, ápice acuminado.</p>
        </div>
        <div class="leaf-img">
          <img src="https://upload.wikimedia.org/wikipedia/commons/7/7f/Ficus_benjamina_leaf.jpg" alt="Hoja ficus" onerror="this.src='https://images.pexels.com/photos/459225/pexels-photo-459225.jpeg?auto=compress&cs=tinysrgb&w=200'">
        </div>
      </div>
      <div class="desc-section">
        <h3><i class="fas fa-tree"></i> Descripción</h3>
        <p>Árbol perenne de copa llorona, raíces aéreas.</p>
      </div>
      <div class="fruit-section">
        <h3><i class="fas fa-apple-alt"></i> Fruto</h3>
        <p>Sicono rojizo, no comestible.</p>
      </div>
      <div class="tree-img">
        <img src="https://upload.wikimedia.org/wikipedia/commons/b/bf/Ficus_benjamina_tree.jpg" alt="Ficus benjamina" onerror="this.src='https://images.pexels.com/photos/161860/pexels-photo-161860.jpeg?auto=compress&cs=tinysrgb&w=400'">
      </div>
    </div>

    <!-- 7. GUAYABO -->
    <div class="plant-card" data-aos="fade-up">
      <div class="card-title">Guayabo</div>
      <div class="scientific-name"><i class="fas fa-tag"></i> Psidium guajava</div>
      <div class="leaf-section">
        <div class="leaf-info">
          <h3><i class="fas fa-leaf"></i> Hoja</h3>
          <p><strong>Forma:</strong> Elíptica, aromática, nervaduras marcadas.</p>
        </div>
        <div class="leaf-img">
          <img src="https://upload.wikimedia.org/wikipedia/commons/4/45/Psidium_guajava_leaves_LR.jpg" alt="Hoja guayaba" onerror="this.src='https://images.pexels.com/photos/594608/pexels-photo-594608.jpeg?auto=compress&cs=tinysrgb&w=200'">
        </div>
      </div>
      <div class="desc-section">
        <h3><i class="fas fa-tree"></i> Descripción</h3>
        <p>Árbol pequeño, corteza lisa, flores blancas.</p>
      </div>
      <div class="fruit-section">
        <h3><i class="fas fa-apple-alt"></i> Fruto</h3>
        <p>Baya globosa dulce, rica en vitamina C.</p>
      </div>
      <div class="tree-img">
        <img src="https://upload.wikimedia.org/wikipedia/commons/e/eb/Psidium_guajava_tree.jpg" alt="Árbol de guayaba" onerror="this.src='https://images.pexels.com/photos/1676432/pexels-photo-1676432.jpeg?auto=compress&cs=tinysrgb&w=400'">
      </div>
    </div>

    <!-- 8. CORDYLINE FRUTICOSA -->
    <div class="plant-card" data-aos="fade-up">
      <div class="card-title">Cordyline</div>
      <div class="scientific-name"><i class="fas fa-tag"></i> Cordyline fruticosa</div>
      <div class="leaf-section">
        <div class="leaf-info">
          <h3><i class="fas fa-leaf"></i> Hoja</h3>
          <p><strong>Forma:</strong> Lanceolada, color rojizo/variegado.</p>
        </div>
        <div class="leaf-img">
          <img src="https://upload.wikimedia.org/wikipedia/commons/2/2f/Cordyline_fruticosa_leaf.jpg" alt="Hoja cordyline" onerror="this.src='https://images.pexels.com/photos/1363876/pexels-photo-1363876.jpeg?auto=compress&cs=tinysrgb&w=200'">
        </div>
      </div>
      <div class="desc-section">
        <h3><i class="fas fa-tree"></i> Descripción</h3>
        <p>Arbusto tropical de follaje ornamental muy vistoso.</p>
      </div>
      <div class="fruit-section">
        <h3><i class="fas fa-apple-alt"></i> Fruto</h3>
        <p>Bayas rojas esféricas, raras en cultivo.</p>
      </div>
      <div class="tree-img">
        <img src="https://upload.wikimedia.org/wikipedia/commons/9/94/Cordyline_fruticosa_plant.jpg" alt="Cordyline fruticosa" onerror="this.src='https://images.pexels.com/photos/1458434/pexels-photo-1458434.jpeg?auto=compress&cs=tinysrgb&w=400'">
      </div>
    </div>

    <!-- 9. CASUARINA -->
    <div class="plant-card" data-aos="fade-up">
      <div class="card-title">Casuarina</div>
      <div class="scientific-name"><i class="fas fa-tag"></i> Casuarina equisetifolia</div>
      <div class="leaf-section">
        <div class="leaf-info">
          <h3><i class="fas fa-leaf"></i> Hoja</h3>
          <p><strong>Forma:</strong> Escamas diminutas, ramillas como agujas.</p>
        </div>
        <div class="leaf-img">
          <img src="https://upload.wikimedia.org/wikipedia/commons/5/5a/Casuarina_equisetifolia_branchlets.jpg" alt="Ramillas casuarina" onerror="this.src='https://images.pexels.com/photos/884549/pexels-photo-884549.jpeg?auto=compress&cs=tinysrgb&w=200'">
        </div>
      </div>
      <div class="desc-section">
        <h3><i class="fas fa-tree"></i> Descripción</h3>
        <p>Árbol columnar resistente a vientos salinos.</p>
      </div>
      <div class="fruit-section">
        <h3><i class="fas fa-apple-alt"></i> Fruto</h3>
        <p>Cono leñoso globoso con sámaras.</p>
      </div>
      <div class="tree-img">
        <img src="https://upload.wikimedia.org/wikipedia/commons/0/0e/Casuarina_equisetifolia_tree.jpg" alt="Casuarina" onerror="this.src='https://images.pexels.com/photos/159398/pexels-photo-159398.jpeg?auto=compress&cs=tinysrgb&w=400'">
      </div>
    </div>

    <!-- 10. FALSA ASHOKA -->
    <div class="plant-card" data-aos="fade-up">
      <div class="card-title">Falsa Ashoka</div>
      <div class="scientific-name"><i class="fas fa-tag"></i> Polyalthia longifolia</div>
      <div class="leaf-section">
        <div class="leaf-info">
          <h3><i class="fas fa-leaf"></i> Hoja</h3>
          <p><strong>Forma:</strong> Largas, lanceoladas, borde ondulado.</p>
        </div>
        <div class="leaf-img">
          <img src="https://upload.wikimedia.org/wikipedia/commons/4/4e/Polyalthia_longifolia_leaf.jpg" alt="Hoja falsa ashoka" onerror="this.src='https://images.pexels.com/photos/115082/pexels-photo-115082.jpeg?auto=compress&cs=tinysrgb&w=200'">
        </div>
      </div>
      <div class="desc-section">
        <h3><i class="fas fa-tree"></i> Descripción</h3>
        <p>Árbol columnar, copa piramidal estrecha.</p>
      </div>
      <div class="fruit-section">
        <h3><i class="fas fa-apple-alt"></i> Fruto</h3>
        <p>Bayas ovoides verdes a púrpura.</p>
      </div>
      <div class="tree-img">
        <img src="https://upload.wikimedia.org/wikipedia/commons/7/79/Polyalthia_longifolia_tree.jpg" alt="Pino hindú" onerror="this.src='https://images.pexels.com/photos/164024/pexels-photo-164024.jpeg?auto=compress&cs=tinysrgb&w=400'">
      </div>
    </div>

    <!-- 11. ZACATE MORADO -->
    <div class="plant-card" data-aos="fade-up">
      <div class="card-title">Zacate Morado</div>
      <div class="scientific-name"><i class="fas fa-tag"></i> Pennisetum setaceum 'Rubrum'</div>
      <div class="leaf-section">
        <div class="leaf-info">
          <h3><i class="fas fa-leaf"></i> Hoja</h3>
          <p><strong>Forma:</strong> Lineal, púrpura intenso.</p>
        </div>
        <div class="leaf-img">
          <img src="https://upload.wikimedia.org/wikipedia/commons/b/b1/Pennisetum_setaceum_Rubrum_leaf.jpg" alt="Zacate morado" onerror="this.src='https://images.pexels.com/photos/145933/pexels-photo-145933.jpeg?auto=compress&cs=tinysrgb&w=200'">
        </div>
      </div>
      <div class="desc-section">
        <h3><i class="fas fa-tree"></i> Descripción</h3>
        <p>Gramínea ornamental, espigas rosado-púrpura.</p>
      </div>
      <div class="fruit-section">
        <h3><i class="fas fa-apple-alt"></i> Fruto</h3>
        <p>Cariópside, se propaga por división.</p>
      </div>
      <div class="tree-img">
        <img src="https://upload.wikimedia.org/wikipedia/commons/0/04/Pennisetum_setaceum_Rubrum_plant.jpg" alt="Pennisetum morado" onerror="this.src='https://images.pexels.com/photos/220131/pexels-photo-220131.jpeg?auto=compress&cs=tinysrgb&w=400'">
      </div>
    </div>

    <!-- 12. VERANERA -->
    <div class="plant-card" data-aos="fade-up">
      <div class="card-title">Veranera</div>
      <div class="scientific-name"><i class="fas fa-tag"></i> Bougainvillea glabra</div>
      <div class="leaf-section">
        <div class="leaf-info">
          <h3><i class="fas fa-leaf"></i> Hoja</h3>
          <p><strong>Forma:</strong> Ovada, ápice agudo, verde brillante.</p>
        </div>
        <div class="leaf-img">
          <img src="https://upload.wikimedia.org/wikipedia/commons/2/2e/Bougainvillea_glabra_leaf.jpg" alt="Hoja veranera" onerror="this.src='https://images.pexels.com/photos/459282/pexels-photo-459282.jpeg?auto=compress&cs=tinysrgb&w=200'">
        </div>
      </div>
      <div class="desc-section">
        <h3><i class="fas fa-tree"></i> Descripción</h3>
        <p>Arbusto trepador espinoso, brácteas coloridas.</p>
      </div>
      <div class="fruit-section">
        <h3><i class="fas fa-apple-alt"></i> Fruto</h3>
        <p>Aquenio seco.</p>
      </div>
      <div class="tree-img">
        <img src="https://upload.wikimedia.org/wikipedia/commons/a/a5/Bougainvillea_glabra_plant.jpg" alt="Buganvilia" onerror="this.src='https://images.pexels.com/photos/931177/pexels-photo-931177.jpeg?auto=compress&cs=tinysrgb&w=400'">
      </div>
    </div>

    <!-- 13. PINO -->
    <div class="plant-card" data-aos="fade-up">
      <div class="card-title">Pino</div>
      <div class="scientific-name"><i class="fas fa-tag"></i> Pinus spp.</div>
      <div class="leaf-section">
        <div class="leaf-info">
          <h3><i class="fas fa-leaf"></i> Hoja (acícula)</h3>
          <p><strong>Forma:</strong> Acicular, en fascículos.</p>
        </div>
        <div class="leaf-img">
          <img src="https://upload.wikimedia.org/wikipedia/commons/c/c0/Pinus_cembra_leaves.jpg" alt="Acículas de pino" onerror="this.src='https://images.pexels.com/photos/376464/pexels-photo-376464.jpeg?auto=compress&cs=tinysrgb&w=200'">
        </div>
      </div>
      <div class="desc-section">
        <h3><i class="fas fa-tree"></i> Descripción</h3>
        <p>Árbol perennifolio, resinoso, de gran longevidad.</p>
      </div>
      <div class="fruit-section">
        <h3><i class="fas fa-apple-alt"></i> Fruto (cono)</h3>
        <p>Estróbilo leñoso (piña), semillas aladas.</p>
      </div>
      <div class="tree-img">
        <img src="https://upload.wikimedia.org/wikipedia/commons/7/73/Pinus_tree.jpg" alt="Pino" onerror="this.src='https://images.pexels.com/photos/1061623/pexels-photo-1061623.jpeg?auto=compress&cs=tinysrgb&w=400'">
      </div>
    </div>
  </div>
  
  <div class="footer-note" data-aos="fade">
    <i class="fas fa-feather-alt"></i> Herbario digital · elegancia botánica <i class="fas fa-feather-alt"></i>
  </div>
</div>

<script src="https://cdnjs.cloudflare.com/ajax/libs/aos/2.3.4/aos.js"></script>
<script>
  AOS.init({ duration: 900, once: false, offset: 40, easing: 'ease-out-cubic' });
</script>
</body>
</html>
