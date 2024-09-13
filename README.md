# Camada 1

[link para o arquivo em Markdown](https://vitorfleonardo.github.io/camada1/)

## 1. Informações e Relações
- **O que é:** Organize os elementos da tela de forma que as relações entre eles fiquem claras tanto para quem vê quanto para quem utiliza leitores de tela.
- **Por que é importante:** Garante que tanto usuários visuais quanto aqueles que utilizam tecnologias assistivas compreendam o conteúdo da mesma forma.

### Exemplo incorreto:
```html
<div>
  <h2>Título</h2>
  <p>Texto descritivo</p>
  <input type="text">
</div>
<div>
  <button>Enviar</button>
</div>
```
Neste exemplo, o botão de envio está fora do contexto visual e lógico do formulário.

### Exemplo correto:
```html
<form>
  <h2>Título</h2>
  <p>Texto descritivo</p>
  <input type="text">
  <button type="submit">Enviar</button>
</form>
```
Aqui, o botão está relacionado ao campo de texto dentro do formulário, garantindo clareza para todos os usuários.

---

## 2. Sequência com Significado
- **O que é:** Garanta que a sequência do conteúdo faça sentido lógico e seja preservada em diferentes tamanhos de tela, com foco em uma ordem sequencial e lógica dos elementos focáveis.
- **Por que é importante:** Facilita a navegação por teclado e o uso de tecnologias assistivas, mantendo a experiência de navegação previsível.

### Exemplo incorreto:
```html
<div tabindex="3">Texto 3</div>
<div tabindex="1">Texto 1</div>
<div tabindex="2">Texto 2</div>
```
A ordem do `tabindex` está fora de sequência, confundindo a navegação.

### Exemplo correto:
```html
<div tabindex="1">Texto 1</div>
<div tabindex="2">Texto 2</div>
<div tabindex="3">Texto 3</div>
```
A sequência do `tabindex` é lógica e segue a ordem visual.

---

## 3. Página com Título
- **O que é:** Certifique-se de que cada página tenha um título claro e descritivo.
- **Por que é importante:** Isso ajuda os usuários, especialmente aqueles que usam leitores de tela, a identificar rapidamente o propósito da página.

### Exemplo incorreto:
```html
<title>Página 1</title>
```
O título da página não fornece informações claras sobre o conteúdo.

### Exemplo correto:
```html
<title>Artigo sobre Acessibilidade Digital</title>
```
O título é descritivo e informa o propósito da página.

---

## 4. Utilização de Características Sensoriais
- **O que é:** Evite depender apenas de características sensoriais como cor ou posição para fornecer instruções.
- **Por que é importante:** Pessoas com deficiência visual ou daltonismo podem não perceber características sensoriais.

### Exemplo incorreto:
```html
<p>Clique no botão verde abaixo.</p>
<button style="background-color: green;">Enviar</button>
```
Esse exemplo depende da cor para instrução.

### Exemplo correto:
```html
<p>Clique no botão abaixo com o texto "Enviar".</p>
<button style="background-color: green;">Enviar</button>
```
Aqui, o texto "Enviar" serve como referência, não a cor.

---

## 5. Nome, Função e Valor Programático
- **O que é:** Certifique-se de que componentes da interface como formulários e links sejam identificados e compreendidos por tecnologias assistivas.
- **Por que é importante:** Facilita a interação de tecnologias assistivas com o conteúdo.

### Exemplo incorreto:
```html
<input type="text">
```
Este campo de entrada não tem rótulo programático.

### Exemplo correto:
```html
<label for="nome">Nome</label>
<input id="nome" type="text">
```
O campo tem um rótulo (`label`), facilitando a compreensão por leitores de tela.

---

## 6. Conteúdo Não Textual
- **O que é:** Forneça descrições textuais para imagens e ícones.
- **Por que é importante:** Ajuda leitores de tela a interpretar o conteúdo visual.

### Exemplo incorreto:
```html
<img src="imagem.jpg">
```
A imagem não tem descrição.

### Exemplo correto:
```html
<img src="imagem.jpg" alt="Descrição da imagem">
```
A `alt` fornece uma descrição textual da imagem.

---

## 7. Transcrições e Legendas
- **O que é:** Forneça transcrições para áudio e legendas para vídeos.
- **Por que é importante:** Isso garante acesso ao conteúdo multimídia para pessoas com deficiência auditiva ou visual.

### Exemplo incorreto:
```html
<video src="video.mp4" controls></video>
```
O vídeo não tem legendas.

### Exemplo correto:
```html
<video src="video.mp4" controls>
  <track kind="captions" src="legendas.vtt" srclang="pt" label="Português">
</video>
```
O vídeo inclui legendas para acessibilidade.

---

## 8. Consistência em Formulários
- **O que é:** Mantenha consistência em formulários e certifique-se de que os rótulos descrevem claramente a finalidade dos campos.
- **Por que é importante:** Facilita o preenchimento de formulários e evita confusões.

### Exemplo incorreto:
```html
<input type="text">
```
O campo não tem rótulo.

### Exemplo correto:
```html
<label for="email">Email</label>
<input id="email" type="text" placeholder="Digite seu email">
```
O campo tem rótulo e instruções claras.

---

## 9. Entrada Redundante
- **O que é:** Evite solicitar informações redundantes, a menos que seja necessário.
- **Por que é importante:** Simplifica o preenchimento de formulários, economizando tempo e esforço.

### Exemplo incorreto:
```html
<input type="email" placeholder="Digite seu email">
<input type="email" placeholder="Confirme seu email">
```
Requer confirmação redundante do email.

### Exemplo correto:
```html
<input type="email" placeholder="Digite seu email">
```
O campo de email é solicitado apenas uma vez.

---

## 10. Identificação e Correção de Erros
- **O que é:** Certifique-se de que os erros sejam claramente identificados e acompanhados de mensagens descritivas.
- **Por que é importante:** Facilita a correção de erros por usuários com diferentes habilidades.

### Exemplo incorreto:
```html
<input type="text">
<div class="error" style="color: red;">Erro</div>
```
A mensagem de erro é vaga e depende apenas da cor.

### Exemplo correto:
```html
<input type="text" aria-describedby="erro-nome">
<div id="erro-nome" class="error">Por favor, insira seu nome.</div>
```
A mensagem de erro é clara e programaticamente vinculada ao campo.

---

Esses exemplos de código demonstram como aplicar práticas corretas de acessibilidade, melhorando a experiência de navegação para todos os usuários.

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
