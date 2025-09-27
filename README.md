# organizacao.3d
<!DOCTYPE html>
<html lang = "pt-pt">
    <head>
        <meta charset="UTF-8">
        <title>teste para impressora 3d</title>
        <link rel="stylesheet" href="style.css">
    </head> 
<body>
    <textarea id="caixa1" rows="80" cols="100" placeholder="Escreve algo aqui (notas)..."></textarea>
  
 <h1> Impressão para catos</h1>
    <ul>
        <li> Ver o stock e os ficheiros já adquiridos</li> <input type="checkbox" />
        <li> fazer uploud dos ficheiros para a impressora</li> <input type="checkbox" />
        <li> fazer a impressão dos ficheiros descarregados</li> <input type="checkbox" />
        <li> corrigir eventuais erros</li> <input type="checkbox" />
        <li> tirar foto do produto final</li> <input type="checkbox" />
        <li> com a foto fazer publicidade</li> <input type="checkbox" />
        <li> fazer converção para a precentagem de lucro</li> <input type="checkbox" />
    </ul>
    <h1> Impressão para suportes</h1>
    <ul>
        <li> Á data de hoje, 22/9/2025, temos varios suportes mas temos de melhorar para menos gastos</li>
        <li> Ver o stock e os ficheiros já adquiridos</li> <input type="checkbox" />
        <li> fazer uploud dos ficheiros para a impressora</li> <input type="checkbox" />
        <li> fazer a impressão dos ficheiros descarregados</li> <input type="checkbox" />
        <li> corrigir eventuais erros</li> <input type="checkbox" />
        <li> tirar foto do produto final</li> <input type="checkbox" />
        <li> com a foto fazer publicidade</li> <input type="checkbox" />
        <li> fazer converção para a precentagem de lucro</li> <input type="checkbox" />
    </ul>
    <h1> Pedidos aleatorios/expecificos</h1>
    <ul> 
        <li> Ver se o cliente tem preferencia na cor</li>
        <li> Ver se temos essa cor</li> <input type="checkbox" />
        <li> Ver se o cliente tem foto do produto</li> <input type="checkbox" />
        <li> Se o cliente tiver foto, fazer um ficheiro com ela ou pesquisar algo do genero</li> <input type="checkbox" />
        <li> Se não tiver foto, encontrar algo que seja o produto que o cliente quer</li> <input type="checkbox" />
        <li> Fazer uploud dos ficheiros para a impressora</li> <input type="checkbox" />
        <li> fazer a impressão dos ficheiros descarregados</li> <input type="checkbox" />
        <li> corrigir eventuais erros</li> <input type="checkbox" />
        <li> tirar foto do produto final</li> <input type="checkbox" />
        <li> com a foto fazer publicidade</li> <input type="checkbox" />
        <li> fazer converção para a precentagem de lucro</li> <input type="checkbox" />
    </ul>
        <h1> Stock existente </h1>
    <ul>
        <li> Impressora para catos </li> <input type="tel" /> <input type="number" />
        <li> Impressora para suportes</li> <input type="tel" /> <input type="number" />
    </ul>
    <h1> Encomendas </h1>
    <ul>
        <li>Impressão para catos </li> <input type="tel" /> <input type="number" /> <input type="text" placeholder="Escreve algo aqui">
        <li>Impressão para suportes</li> <input type="tel" /> <input type="number" /> <input type="text" placeholder="Escreve algo aqui">

</ul>
<textarea id="caixa2" rows="80" cols="100" placeholder="Escreve algo aqui (especifidades das encomendas)..."></textarea>

<script>
  const caixa1 = document.getElementById("caixa1");
  const caixa2 = document.getElementById("caixa2");

  // Recuperar texto guardado para cada caixa
  caixa1.value = localStorage.getItem("textoGuardado1") || "";
  caixa2.value = localStorage.getItem("textoGuardado2") || "";

  // Guardar automaticamente quando o utilizador escreve
  caixa1.addEventListener("input", () => {
    localStorage.setItem("textoGuardado1", caixa1.value);
  });

  caixa2.addEventListener("input", () => {
    localStorage.setItem("textoGuardado2", caixa2.value);
  });
</script>

<h1> Data de entrega das encomendas</h1>
<textarea id="caixa3" rows="1" cols="100" placeholder="Escreve algo aqui (encomenda de quem)..."></textarea> <input type="date" id="data1"/>
<script>
  const caixa3 = document.getElementById("caixa3");
    // Recuperar texto guardado para a caixa3
    caixa3.value = localStorage.getItem("textoGuardado3") || "";
    // Guardar automaticamente quando o utilizador escreve
    caixa3.addEventListener("input", () => {
     localStorage.setItem("textoGuardado3", caixa3.value);
      });
</script>
<script>
  // Guardar e restaurar todas as caixas de texto
  document.querySelectorAll("textarea").forEach(textarea => {
    const id = textarea.id;
    if (!id) return; // ignora se não tiver id
    textarea.value = localStorage.getItem(id) || "";
    textarea.addEventListener("input", () => {
      localStorage.setItem(id, textarea.value);
    });
  });

  // Guardar e restaurar todos os inputs de data
  document.querySelectorAll('input[type="date"]').forEach(dateInput => {
    const id = dateInput.id;
    if (!id) return; // ignora se não tiver id
    dateInput.value = localStorage.getItem(id) || "";
    dateInput.addEventListener("input", () => {
      localStorage.setItem(id, dateInput.value);
    });
  });
</script>
<!-- 10 novas caixas de texto + calendários -->
<div id="bloco-extra">
  <textarea id="caixa4" rows="1" cols="100"  placeholder="Escreve algo aqui (encomenda de quem)..."></textarea>
  <input type="date" id="data4">

  <textarea id="caixa5" rows="1" cols="100"  placeholder="Escreve algo aqui (encomenda de quem)..."></textarea>
  <input type="date" id="data5">

  <textarea id="caixa6" rows="1" cols="100"  placeholder="Escreve algo aqui (encomenda de quem)..."></textarea>
  <input type="date" id="data6">

  <textarea id="caixa7" rows="1" cols="100" placeholder="Escreve algo aqui (encomenda de quem)..."></textarea>
  <input type="date" id="data7">

  <textarea id="caixa8" rows="1" cols="100" placeholder="Escreve algo aqui (encomenda de quem)..."></textarea>
  <input type="date" id="data8">

  <textarea id="caixa9" rows="1" cols="100" placeholder="Escreve algo aqui (encomenda de quem)..."></textarea>
  <input type="date" id="data9">

  <textarea id="caixa10" rows="1" cols="100" placeholder="Escreve algo aqui (encomenda de quem)..."></textarea>
  <input type="date" id="data10">

  <textarea id="caixa11" rows="1" cols="100" placeholder="Escreve algo aqui (encomenda de quem)..."></textarea>
  <input type="date" id="data11">

  <textarea id="caixa12" rows="1" cols="100" placeholder="Escreve algo aqui (encomenda de quem)..."></textarea>
  <input type="date" id="data12">

  <textarea id="caixa13" rows="1" cols="100" placeholder="Escreve algo aqui (encomenda de quem)..."></textarea>
  <input type="date" id="data13">
</div>
<script>
  // --- Guardar e restaurar TODAS as caixas de texto ---
  document.querySelectorAll("textarea").forEach(textarea => {
    const id = textarea.id;
    if (!id) return; // ignora se não tiver id
    textarea.value = localStorage.getItem(id) || "";
    textarea.addEventListener("input", () => {
      localStorage.setItem(id, textarea.value);
    });
  });

  // --- Guardar e restaurar TODOS os inputs de data ---
  document.querySelectorAll('input[type="date"]').forEach(dateInput => {
    const id = dateInput.id;
    if (!id) return;
    dateInput.value = localStorage.getItem(id) || "";
    dateInput.addEventListener("input", () => {
      localStorage.setItem(id, dateInput.value);
    });
  });
</script>




</body>


</html>
