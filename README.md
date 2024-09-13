# camada1

## 1. Informações e Relações  
- <b> O que é: </b> Organize os elementos da tela para que suas relações e informações sejam claras tanto para quem vê quanto para quem ouve. 
- <b> Por que é importante: </b>Isso garante que tanto pessoas que veem quanto aquelas que utilizam leitores de tela compreendam o conteúdo da mesma maneira.

## 2. Sequência com Significado  
- <b> O que é: </b> Garanta que a sequência do conteúdo faça sentido lógico e seja preservada em diferentes tamanhos de tela, garantindo também que os elementos focáveis na tela sigam uma ordem sequencial e lógica que preserve o significado do conteúdo, assegurando uma experiência de navegação previsível.  
- <b> Por que é importante: </b> Mantém a experiência de navegação previsível, facilitando o uso por todos, especialmente aqueles que dependem de navegação pelo teclado ou tecnologias assistivas.  

## 3. Página com Título  
- <b> O que é: </b> Certifique-se de que cada página tenha um título claro e descritivo que indique sua finalidade.  
- <b> Por que é importante: </b> Isso ajuda os usuários, especialmente aqueles que usam leitores de tela, a identificar rapidamente o propósito da página.  

## 4. Utilização de Características Sensoriais  
- <b> O que é: </b> Forneça instruções que não dependam apenas de características sensoriais como formato, cor ou posição, tais como “clique no botão abaixo”.  
- <b> Por que é importante: </b> Isso permite que usuários com deficiência visual ou daltonismo entendam as instruções sem dificuldades.  

## 5. Nome, Função e Valor Programático  
- <b> O que é: </b> Certifique-se de que todos os componentes da interface do usuário, como formulários, links e elementos gerados por scripts, possam ser identificados e entendidos por tecnologias assistivas usando nome, função e valor programaticamente.  
- <b> Por que é importante: </b> Isso permite que tecnologias assistivas interpretem corretamente o conteúdo e sua função, tornando a navegação acessível.  

## 6. Conteúdo Não Textual  
- <b> O que é: </b> Forneça descrições textuais para todas as imagens, ícones e CAPTCHAs relevantes, garantindo que suas funções e conteúdos sejam compreensíveis por leitores de tela.  
- <b> Por que é importante: </b> Descrições textuais garantem que usuários de leitores de tela compreendam o propósito e o conteúdo visual.  

## 7. Transcrições e Legendas  
- <b> O que é: </b> Forneça transcrições textuais para todo conteúdo de áudio e forneça legendas e/ou audiodescrições para todo conteúdo de vídeo.  
- <b> Por que é importante: </b> Isso garante o acesso de pessoas com deficiência auditiva ou visual ao conteúdo multimídia.  

## 8. Consistência em Formulários  
- <b> O que é: </b> Evite alterar o contexto do usuário ao interagir com campos de entrada de dados e cabeçalhos, a menos que haja confirmação explícita, de forma a manter a consistência e previsibilidade para os usuários ao preencher formulários, garantindo também que todos os rótulos descrevam claramente a finalidade dos campos, inclusive com instruções, se necessário.  
- <b> Por que é importante: </b> Ajuda o usuário a entender melhor o que é necessário preencher e evita confusões durante o processo de envio de formulários.  

## 9. Entrada Redundante  
- <b> O que é: </b> Evite pedir informações repetidas durante o preenchimento de um formulário em etapas, a menos que seja essencial (como para confirmação de senha).  
- <b> Por que é importante: </b> Simplifica o preenchimento de formulários, economizando tempo e esforço dos usuários.  

## 10. Identificação e Correção de Erros  
- <b> O que é: </b> Certifique-se de que os erros sejam claramente identificados visual e auditivamente, usando, por exemplo, mudança de cor, ícone e som de alerta e uma mensagem de texto. Garantir também que exista uma sugestão clara de onde o erro ocorre e como pode ser solucionado.  
- <b> Por que é importante: </b> Facilita a correção de erros por usuários com diferentes habilidades, melhorando a experiência e eficiência.  

Aqui está a versão revisada do texto sobre acessibilidade, com exemplos de código corretos e incorretos para cada tópico. Os exemplos ilustram práticas de acessibilidade, mostrando como implementar corretamente e os problemas de práticas inadequadas.

---

## 11. Finalidade do Link  
- **O que é:** Cada link deve ter um texto descritivo ou estar inserido em um contexto que indique claramente sua finalidade.  
- **Por que é importante:** Evita confusões para todos os usuários, especialmente aqueles que utilizam tecnologias assistivas.

### Exemplo incorreto:
```html
<a href="acessibilidade.html">Clique aqui</a>
```
Este exemplo não indica claramente a finalidade do link, o que pode confundir usuários de leitores de tela.

### Exemplo correto:
```html
<a href="acessibilidade.html" aria-label="Saiba mais sobre acessibilidade digital">Saiba mais sobre acessibilidade digital</a>
```
Aqui, o texto do link e o atributo `aria-label` tornam a finalidade do link clara.

---

## 12. Cancelamento de Acionamento  
- **O que é:** Permite cancelar um clique ou toque acidental antes de liberar o botão, além de evitar que ações dependam de movimentos do dispositivo.  
- **Por que é importante:** Isso previne erros em dispositivos móveis, onde toques acidentais são comuns.

### Exemplo incorreto:
```html
<button onclick="deleteItem()">Excluir</button>
```
Este exemplo não permite ao usuário confirmar ou cancelar a ação.

### Exemplo correto:
```html
<button onclick="confirmDelete()">Excluir</button>

<div id="confirmDialog" style="display:none;">
  Tem certeza que deseja excluir? 
  <button onclick="deleteItem()">Sim</button>
  <button onclick="cancelDelete()">Não</button>
</div>

<script>
  function confirmDelete() {
    document.getElementById('confirmDialog').style.display = 'block';
  }
  
  function deleteItem() {
    alert('Item excluído!');
  }
  
  function cancelDelete() {
    document.getElementById('confirmDialog').style.display = 'none';
  }
</script>
```
Este código oferece ao usuário a opção de confirmar ou cancelar a exclusão.

---

## 13. Gestos Táteis  
- **O que é:** Funções que requerem gestos táteis devem ter uma alternativa de interação por um único ponto.  
- **Por que é importante:** Garante que pessoas com mobilidade reduzida possam interagir com a interface.

### Exemplo incorreto:
```html
<div id="map"></div>
<script>
  document.getElementById('map').addEventListener('pinch', function() {
    // Zoom com gesto
  });
</script>
```
Este exemplo só permite o uso do gesto de pinçar para ampliar o mapa.

### Exemplo correto:
```html
<div id="map"></div>
<button onclick="zoomIn()">+</button>
<button onclick="zoomOut()">-</button>

<script>
  function zoomIn() {
    alert('Zoom in');
  }
  
  function zoomOut() {
    alert('Zoom out');
  }
</script>
```
Aqui, os botões fornecem uma alternativa ao gesto de pinçar.

---

## 14. Navegação por Teclado  
- **O que é:** Todas as funcionalidades devem ser operáveis por teclado, permitindo navegação por todos os elementos interativos.  
- **Por que é importante:** Facilita a navegação para pessoas que não utilizam o mouse, como usuários de leitores de tela.

### Exemplo incorreto:
```html
<button onclick="showDetails()">Ver detalhes</button>
```
Este botão não está configurado para navegação por teclado.

### Exemplo correto:
```html
<button onclick="showDetails()" tabindex="0">Ver detalhes</button>

<script>
  function showDetails() {
    alert('Detalhes mostrados');
  }
</script>
```
O atributo `tabindex="0"` permite que o botão seja acessível por teclado.

---

## 15. Ignorar Blocos Repetitivos  
- **O que é:** Fornece um meio para os usuários de teclado ignorarem conteúdos repetitivos, como menus de navegação.  
- **Por que é importante:** Melhora a eficiência da navegação para usuários de leitores de tela e teclados.

### Exemplo incorreto:
```html
<nav>
  <!-- Menu longo aqui -->
</nav>
```
Este exemplo não oferece uma maneira de ignorar o menu para chegar ao conteúdo principal.

### Exemplo correto:
```html
<a href="#mainContent" class="skip-link">Pular para o conteúdo principal</a>

<nav>
  <!-- Menu aqui -->
</nav>

<div id="mainContent">
  <h1>Conteúdo principal</h1>
</div>

<style>
  .skip-link {
    position: absolute;
    top: -40px;
    left: 0;
  }
  .skip-link:focus {
    top: 0;
  }
</style>
```
Este link de pular oferece uma maneira de ignorar o menu e ir diretamente ao conteúdo principal.

---

## 16. Controle de Tempo e Movimentos Automáticos  
- **O que é:** Permite que os usuários controlem movimentos automáticos e ajustem limites de tempo definidos no site.  
- **Por que é importante:** Garante que o usuário tenha controle sobre a navegação e evita frustrações.

### Exemplo incorreto:
```html
<div id="banner">
  <img src="banner1.jpg">
</div>

<script>
  setInterval(() => {
    // Muda automaticamente os banners
  }, 3000);
</script>
```
Este banner rotaciona automaticamente sem permitir controle.

### Exemplo correto:
```html
<div id="banner">
  <img src="banner1.jpg">
</div>
<button onclick="pauseRotation()">Pausar</button>

<script>
  let bannerInterval = setInterval(() => {
    // Muda os banners
  }, 3000);

  function pauseRotation() {
    clearInterval(bannerInterval);
  }
</script>
```
O botão permite que o usuário pause a rotação automática.

---

## 17. Rótulo no Nome Acessível  
- **O que é:** O nome dos controles deve coincidir com seus rótulos visíveis para facilitar a interação por voz.  
- **Por que é importante:** Facilita a navegação por comando de voz e com tecnologias assistivas.

### Exemplo incorreto:
```html
<button aria-label="Enviar formulário">Submit</button>
```
Aqui, o rótulo visível "Submit" não coincide com o nome acessível "Enviar formulário".

### Exemplo correto:
```html
<button aria-label="Enviar formulário">Enviar formulário</button>
```
O rótulo visível e o nome acessível são idênticos.

---

## 18. Ajuda Consistente  
- **O que é:** O formato da ajuda deve ser consistente em todas as páginas e incluir opções de contato humano e automatizado.  
- **Por que é importante:** Facilita ao usuário encontrar e usar a ajuda quando necessário.

### Exemplo incorreto:
```html
<a href="suporte.html">Ajuda</a>
<a href="contact.html">Fale conosco</a>
```
Links de ajuda inconsistentes podem confundir o usuário.

### Exemplo correto:
```html
<a href="suporte.html" aria-label="Ajuda e suporte técnico">Ajuda</a>
```
Um único link claro e consistente para todas as páginas de suporte.

---

## 19. Audiodescrição para Vídeos  
- **O que é:** Fornece audiodescrição para todo conteúdo de vídeo pré-gravado.  
- **Por que é importante:** Torna o conteúdo acessível para pessoas com deficiência visual.

### Exemplo incorreto:
```html
<video controls>
  <source src="video.mp4" type="video/mp4">
</video>
```
Este vídeo não oferece audiodescrição.

### Exemplo correto:
```html
<video controls>
  <source src="video.mp4" type="video/mp4">
  <track kind="descriptions" src="audiodescricao.vtt" srclang="pt" label="Português">
</video>
```
O vídeo inclui uma faixa de audiodescrição para ajudar usuários com deficiência visual.

---

## 20. Contraste de Texto e Imagens  
- **O que é:** Garante que o texto e as imagens tenham contraste suficiente em relação ao fundo.  
- **Por que é importante:** Melhora a legibilidade para usuários com baixa visão.

### Exemplo incorreto:
```html
<p style="color: gray; background-color: white;">Texto de baixa legibilidade</p>
```
Aqui, o contraste entre o texto e o fundo é insuficiente.

### Exemplo correto:
```html
<p style="color: black; background-color: white;">Texto de alto contraste</p>
```
Este exemplo garante um contraste suficiente para melhorar a legibilidade.

---

Esses exemplos de código demonstram como implementar corretamente as diretrizes de acessibilidade em sites, melhorando a experiência de navegação para todos os usuários.
