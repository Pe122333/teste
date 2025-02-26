<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <title>Super Compras</title>

  <!-- Exemplo: caso as fontes não estejam disponíveis localmente,
       substitua ou importe do Google Fonts ou outro local -->
  <style>
    /* ====== Reset básico ====== */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }
    html, body {
      width: 100%;
      height: 100%;
      overflow: hidden; /* evita scroll */
    }
    body {
      position: relative;
      font-family: sans-serif;
    }

    /* ====== Background (1440x1024) ====== */
    .Background {
      position: absolute;
      width: 1440px;
      height: 1024px;
      left: 0;
      top: 0;
      background: #E9E9E9;
    }

    /* ====== Rectangle 16 (1440x1024 #D9D9D9) ====== */
    .Rectangle16 {
      position: absolute;
      width: 1440px;
      height: 1024px;
      left: 0;
      top: 0;
      background: #D9D9D9;
    }

    /* ====== Subtract1 (mesmo tamanho) ====== */
    .Subtract1 {
      position: absolute;
      width: 1440px;
      height: 1024px;
      left: 0;
      top: 0;
      background: #D9D9D9;
    }

    /* ====== Rectangle 15 (1440x1024 #D9D9D9) ====== */
    .Rectangle15 {
      position: absolute;
      width: 1440px;
      height: 1024px;
      left: 0;
      top: 0;
      background: #D9D9D9;
    }

    /* ====== "$" repetidos (14 vezes), todos iguais ====== */
    .money-sign {
      position: absolute;
      width: 137px;
      height: 75px;
      font-family: 'Akatab', sans-serif;
      font-style: normal;
      font-weight: 800;
      font-size: 256px;
      line-height: 75px;
      display: flex;
      align-items: center;
      justify-content: center;
      text-align: center;
      color: #FFFFFF;
      transform: rotate(-30deg);
      /* Sem left/top definidos no snippet – todos ficarão empilhados 
         Se quiser posicioná-los, adicione .money-sign-1, .money-sign-2 etc. */
    }

    /* ====== Rectangle 14 ====== */
    .Rectangle14 {
      position: absolute;
      width: 1350px;
      height: 772px;
      left: 45px;
      top: 140px;
      background: linear-gradient(180deg, #0F6A89 8%, #FDFDFD 78.03%);
      box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
      border-radius: 50px;
    }

    /* ====== Porquinho (imagem + overlay) ====== */
    .Porquinho {
      position: absolute;
      width: 565px;
      height: 772px;
      left: 45px;
      top: 140px;
      background: 
        linear-gradient(
          180.03deg, 
          rgba(7, 101, 130, 0.85) 0.03%, 
          rgba(15, 49, 61, 0.85) 82.58%
        ),
        url('post_thumbnail-83196d3e51a33a7f92c125e536b12b58.png');
      background-size: cover;
      background-position: center;
      border-radius: 50px 0px 0px 50px;
    }

    /* ====== Group 1 (336x336) ====== */
    .Group1 {
      position: absolute;
      width: 336px;
      height: 336px;
      left: 159px;
      top: 273px;
    }

    /* ====== Logo Simples (também 336x336) ====== */
    .LogoSimples {
      position: absolute;
      width: 336px;
      height: 336px;
      left: 159px;
      top: 273px;
      /* Nada mais definido */
    }

    /* ====== InteriorLogo (grande) ====== */
    .InteriorLogo {
      position: absolute;
      width: 188.26px;
      height: 273.72px;
      left: 232.04px;
      top: 300.59px;
    }

    /* ====== Rectangle1 (dentro do logo) ====== */
    .Rectangle1 {
      box-sizing: border-box;
      position: absolute;
      width: 74.03px;
      height: 22.63px;
      left: 251.01px;
      top: 450.12px;
      background: #FFFFFF;
      border: 1px solid #FFFFFF;
      transform: rotate(-30.46deg);
    }

    /* ====== Rectangle2 (dentro do logo) ====== */
    .Rectangle2 {
      box-sizing: border-box;
      position: absolute;
      width: 74.16px;
      height: 22.63px;
      left: 326.19px;
      top: 443.63px;
      background: #FFFFFF;
      border: 1px solid #FFFFFF;
      transform: rotate(-30.46deg);
    }

    /* ====== Intersect1 ====== */
    .Intersect1 {
      box-sizing: border-box;
      position: absolute;
      width: 172.49px;
      height: 139.78px;
      left: 232.04px;
      top: 300.59px;
      background: #FFFFFF;
      border: 1px solid #FFFFFF;
    }

    /* ====== Rectangle8 ====== */
    .Rectangle8 {
      position: absolute;
      width: 309.26px;
      height: 137.42px;
      left: 121.67px;
      top: 353.49px;
      background: #D9D9D9;
      transform: rotate(-30.46deg);
    }

    /* ====== Subtract2 ====== */
    .Subtract2 {
      position: absolute;
      width: 185.04px;
      height: 185.04px;
      left: 232.04px;
      top: 300.59px;
      background: #D9D9D9;
    }

    /* ====== Ellipse4-1 ====== */
    .Ellipse4-1 {
      position: absolute;
      width: 185.04px;
      height: 185.04px;
      left: 232.04px;
      top: 300.59px;
      background: rgba(217, 217, 217, 0.46);
      border-radius: 50%;
    }

    /* ====== Ellipse5-1 ====== */
    .Ellipse5-1 {
      position: absolute;
      width: 99.01px;
      height: 99.01px;
      left: 275.87px;
      top: 344.42px;
      background: rgba(174, 164, 164, 0.76);
      border-radius: 50%;
    }

    /* ====== Intersect2 ====== */
    .Intersect2 {
      box-sizing: border-box;
      position: absolute;
      width: 172.03px;
      height: 139px;
      left: 248.28px;
      top: 435.32px;
      background: #FFFFFF;
      border: 1px solid #FFFFFF;
    }

    /* ====== Rectangle9 ====== */
    .Rectangle9 {
      position: absolute;
      width: 309.26px;
      height: 137.42px;
      left: 194.68px;
      top: 560.66px;
      background: #D9D9D9;
      transform: rotate(-30.46deg);
    }

    /* ====== Subtract3 ====== */
    .Subtract3 {
      position: absolute;
      width: 185.04px;
      height: 185.04px;
      left: 235.26px;
      top: 389.27px;
      background: #D9D9D9;
    }

    /* ====== Ellipse4-2 ====== */
    .Ellipse4-2 {
      position: absolute;
      width: 185.04px;
      height: 185.04px;
      left: 235.26px;
      top: 389.27px;
      background: rgba(217, 217, 217, 0.46);
      border-radius: 50%;
    }

    /* ====== Ellipse5-2 ====== */
    .Ellipse5-2 {
      position: absolute;
      width: 99.01px;
      height: 99.01px;
      left: 279.08px;
      top: 433.1px;
      background: rgba(174, 164, 164, 0.76);
      border-radius: 50%;
    }

    /* ====== Ellipse3 (contorno do logo) ====== */
    .Ellipse3 {
      box-sizing: border-box;
      position: absolute;
      width: 336px;
      height: 336px;
      left: 159px;
      top: 273px;
      border: 6px solid #FFFFFF;
      border-radius: 50%;
    }

    /* ====== SUPER COMPRAS (Texto) ====== */
    .SUPERCOMPRAS {
      position: absolute;
      width: 316px;
      height: 142px;
      left: 176px;
      top: 636px;
      font-family: 'Akatab', sans-serif;
      font-style: normal;
      font-weight: 800;
      font-size: 64px;
      line-height: 75px;
      display: flex;
      align-items: center;
      justify-content: center;
      text-align: center;
      color: #FFFFFF;
    }

    /* ====== "Clique no botão abaixo..." (Texto) ====== */
    .CliqueNoBotao {
      position: absolute;
      width: 539px;
      height: 76px;
      left: 739px;
      top: 482px;
      font-family: 'Alegreya Sans', sans-serif;
      font-style: normal;
      font-weight: 700;
      font-size: 42px;
      line-height: 45px;
      display: flex;
      align-items: center;
      justify-content: center;
      text-align: center;
      color: #16485A;
    }

    /* ====== Group 2 (botão) ====== */
    .Group2 {
      position: absolute;
      width: 517px;
      height: 87px;
      left: 746px;
      top: 698px;
    }

    /* ====== Rectangle17 (fundo do botão) ====== */
    .Rectangle17 {
      position: absolute;
      width: 517px;
      height: 87px;
      left: 746px;
      top: 698px;
      background: #056482;
      box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
      border-radius: 64px;
    }

    /* ====== "Verifique agora" (texto do botão) ====== */
    .VerifiqueAgora {
      position: absolute;
      width: 477px;
      height: 86px;
      left: 769px;
      top: 699px;
      font-family: 'Afacad', sans-serif;
      font-style: normal;
      font-weight: 700;
      font-size: 52px;
      line-height: 75px;
      display: flex;
      align-items: center;
      justify-content: center;
      text-align: center;
      color: #FFFFFF;
    }

    /* ====== Interior Logo2 (a 2ª instância) ====== */
    .InteriorLogo2 {
      position: absolute;
      width: 94.06px;
      height: 136.76px;
      left: 958px;
      top: 240px;
    }

    /* ====== Rectangle1-2 ====== */
    .Rectangle1-2 {
      position: absolute;
      width: 36.99px;
      height: 11.31px;
      left: 967.48px;
      top: 314.71px;
      background: #FFFFFF;
      transform: rotate(-30.46deg);
    }

    /* ====== Rectangle2-2 ====== */
    .Rectangle2-2 {
      position: absolute;
      width: 37.05px;
      height: 11.31px;
      left: 1005.04px;
      top: 311.47px;
      background: #FFFFFF;
      transform: rotate(-30.46deg);
    }

    /* ====== Intersect3 ====== */
    .Intersect3 {
      position: absolute;
      width: 86.18px;
      height: 69.84px;
      left: 958px;
      top: 240px;
      background: #FFFFFF;
    }

    /* ====== Rectangle8-2 ====== */
    .Rectangle8-2 {
      position: absolute;
      width: 154.52px;
      height: 68.66px;
      left: 902.85px;
      top: 266.43px;
      background: #D9D9D9;
      transform: rotate(-30.46deg);
    }

    /* ====== Subtract4 ====== */
    .Subtract4 {
      position: absolute;
      width: 92.45px;
      height: 92.45px;
      left: 958px;
      top: 240px;
      background: #D9D9D9;
    }

    /* ====== Ellipse4-3 ====== */
    .Ellipse4-3 {
      position: absolute;
      width: 92.45px;
      height: 92.45px;
      left: 958px;
      top: 240px;
      background: rgba(217, 217, 217, 0.46);
      border-radius: 50%;
    }

    /* ====== Ellipse5-3 ====== */
    .Ellipse5-3 {
      position: absolute;
      width: 49.47px;
      height: 49.47px;
      left: 979.9px;
      top: 261.9px;
      background: rgba(174, 164, 164, 0.76);
      border-radius: 50%;
    }

    /* ====== Intersect4 ====== */
    .Intersect4 {
      position: absolute;
      width: 85.95px;
      height: 69.45px;
      left: 966.11px;
      top: 307.31px;
      background: #FFFFFF;
    }

    /* ====== Rectangle9-2 ====== */
    .Rectangle9-2 {
      position: absolute;
      width: 154.52px;
      height: 68.66px;
      left: 939.33px;
      top: 369.94px;
      background: #D9D9D9;
      transform: rotate(-30.46deg);
    }

    /* ====== Subtract5 ====== */
    .Subtract5 {
      position: absolute;
      width: 92.45px;
      height: 92.45px;
      left: 959.61px;
      top: 284.31px;
      background: #D9D9D9;
    }

    /* ====== Ellipse4-4 ====== */
    .Ellipse4-4 {
      position: absolute;
      width: 92.45px;
      height: 92.45px;
      left: 959.61px;
      top: 284.31px;
      background: rgba(217, 217, 217, 0.46);
      border-radius: 50%;
    }

    /* ====== Ellipse5-4 ====== */
    .Ellipse5-4 {
      position: absolute;
      width: 49.47px;
      height: 49.47px;
      left: 981.5px;
      top: 306.2px;
      background: rgba(174, 164, 164, 0.76);
      border-radius: 50%;
    }

    /* ====== Ellipse3-2 (não tem estilo distinto no snippet, 
         mas foi listado no final) ====== */
    .Ellipse3-2 {
      position: absolute;
      width: 336px;
      height: 336px;
      left: 159px;
      top: 273px;
      border: 6px solid #FFFFFF;
      border-radius: 50%;
      /* Se for o mesmo contorno do primeiro logo, é duplicado */
    }
  </style>
</head>
<body>

  <!-- Camadas de fundo -->
  <div class="Background"></div>
  <div class="Rectangle16"></div>
  <div class="Subtract1"></div>
  <div class="Rectangle15"></div>

  <!-- Vários "$" sobrepostos (14 vezes) -->
  <div class="money-sign">$</div>
  <div class="money-sign">$</div>
  <div class="money-sign">$</div>
  <div class="money-sign">$</div>
  <div class="money-sign">$</div>
  <div class="money-sign">$</div>
  <div class="money-sign">$</div>
  <div class="money-sign">$</div>
  <div class="money-sign">$</div>
  <div class="money-sign">$</div>
  <div class="money-sign">$</div>
  <div class="money-sign">$</div>
  <div class="money-sign">$</div>
  <div class="money-sign">$</div>

  <!-- Cartão principal e imagem -->
  <div class="Rectangle14"></div>
  <div class="Porquinho"></div>

  <!-- Grupo do Logo grande (esquerda) -->
  <div class="Group1"></div>
  <div class="LogoSimples"></div>
  <div class="InteriorLogo"></div>
  <div class="Rectangle1"></div>
  <div class="Rectangle2"></div>
  <div class="Intersect1"></div>
  <div class="Rectangle8"></div>
  <div class="Subtract2"></div>
  <div class="Ellipse4-1"></div>
  <div class="Ellipse5-1"></div>
  <div class="Intersect2"></div>
  <div class="Rectangle9"></div>
  <div class="Subtract3"></div>
  <div class="Ellipse4-2"></div>
  <div class="Ellipse5-2"></div>
  <div class="Ellipse3"></div>

  <!-- Texto "SUPER COMPRAS" -->
  <div class="SUPERCOMPRAS">SUPER COMPRAS</div>

  <!-- Texto "Clique no botão abaixo..." -->
  <div class="CliqueNoBotao">Clique no botão abaixo para evitar problemas no caixa</div>

  <!-- Botão -->
  <div class="Group2"></div>
  <div class="Rectangle17"></div>
  <div class="VerifiqueAgora">🔎 Verifique agora</div>

  <!-- Segundo logo / interior? (direita?) -->
  <div class="InteriorLogo2"></div>
  <div class="Rectangle1-2"></div>
  <div class="Rectangle2-2"></div>
  <div class="Intersect3"></div>
  <div class="Rectangle8-2"></div>
  <div class="Subtract4"></div>
  <div class="Ellipse4-3"></div>
  <div class="Ellipse5-3"></div>
  <div class="Intersect4"></div>
  <div class="Rectangle9-2"></div>
  <div class="Subtract5"></div>
  <div class="Ellipse4-4"></div>
  <div class="Ellipse5-4"></div>
  <div class="Ellipse3-2"></div>

</body>
</html>
