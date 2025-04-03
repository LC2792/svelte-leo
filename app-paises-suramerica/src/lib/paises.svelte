<script>
    export let pais;
    let p;
  
    // Diccionario con TODOS los países de Sudamérica
    const paises = {
        "argentina": ["Argentina", "Buenos Aires", "45,81 millones", "Peso argentino", "2,78 millones km²", "Flag_of_Argentina.svg"],
        "bolivia": ["Bolivia", "La Paz (sede de gobierno)", "12,08 millones", "Boliviano", "1,1 millones km²", "Flag_of_Bolivia.svg"],
        "brasil": ["Brasil", "Brasilia", "214,3 millones", "Real brasileño", "8,51 millones km²", "Flag_of_Brazil.svg"],
        "chile": ["Chile", "Santiago", "19,49 millones", "Peso chileno", "756.102 km²", "Flag_of_Chile.svg"],
        "colombia": ["Colombia", "Bogotá", "51,52 millones", "Peso colombiano", "1,142 millones km²", "Flag_of_Colombia.svg"],
        "ecuador": ["Ecuador", "Quito", "17,8 millones", "Dólar estadounidense", "256.370 km²", "Flag_of_Ecuador.svg"],
        "guyana": ["Guyana", "Georgetown", "800.000", "Dólar guyanés", "214.970 km²", "Flag_of_Guyana.svg"],
        "paraguay": ["Paraguay", "Asunción", "7,1 millones", "Guaraní paraguayo", "406.752 km²", "Flag_of_Paraguay.svg"],
        "peru": ["Perú", "Lima", "33,72 millones", "Sol peruano", "1.285.215 km²", "Flag_of_Peru.png"],
        "surinam": ["Surinam", "Paramaribo", "590.000", "Dólar surinamés", "163.820 km²", "Flag_of_Suriname.svg"],
        "uruguay": ["Uruguay", "Montevideo", "3,55 millones", "Peso uruguayo", "176.215 km²", "Flag_of_Uruguay.svg"],
        "venezuela": ["Venezuela", "Caracas", "28,2 millones", "Bolívar", "916.445 km²", "Flag_of_Venezuela.svg"]
    };
  
    
    p = paises[pais];

  </script>
  
  <div class="main">
      <div class="col1">
        <img src={"/src/assets/" + p[5]} alt={"Bandera " + p[0]} width="300" height="200">
      </div>
      <div class="col2">
          <div class="linea"><strong>País:</strong> {p[0]}</div>
          <div class="linea"><strong>Capital:</strong> {p[1]}</div>
          <div class="linea"><strong>Población:</strong> {p[2]}</div>
          <div class="linea"><strong>Moneda:</strong> {p[3]}</div>
          <div class="linea"><strong>Extensión:</strong> {p[4]}</div>
      </div>
  </div>

<style>
    .main {
        display: grid;
        grid-template-columns: repeat(4, 1fr);
        grid-gap: 5px;
        grid-auto-rows: minmax(100px, auto);
        border-radius: 10px;
        border-style: solid;
        border-color: rgb(186, 190, 182);
        border-width: 2px;
        margin-left: auto;
        width: 600px;
        box-shadow: 5px 5px 5px black;
        margin-right: 5px;
        margin-bottom: 10px;
    }

    .col1 {
        grid-column: 1;
        grid-row: 1;
        margin: 5px;
        padding: 5px;
    }

    .col2 {
        grid-column: 2;
        grid-row: 1;
        margin: 5px;
        padding: 5px;
        border-color: black;
        width: max-content;
    }
    strong {
        color: blue;
        font-weight: bolder;
    }

    .linea {
        font-size: 20px;
        margin-bottom: 18px;
    }
</style>
