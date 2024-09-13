# camada1

## 1. Informações e Relações  
- <b> O que é: </b> Organize os elementos da tela para que suas relações e informações sejam claras tanto para quem vê quanto para quem ouve. 
- <b> Por que é importante: </b>Isso garante que tanto pessoas que veem quanto aquelas que utilizam leitores de tela compreendam o conteúdo da mesma maneira.

**Exemplo correto de implementação:**
```
<h1>Formulário de Contato</h1>
<p>Preencha as informações abaixo para nos enviar uma mensagem.</p>

<label for="nome">Nome:</label>
<input type="text" id="nome" name="nome">

<label for="email">E-mail:</label>
<input type="email" id="email" name="email">

<label for="mensagem">Mensagem:</label>
<textarea id="mensagem" name="mensagem"></textarea>

<button type="submit">Enviar</button>			
```

**Contraexemplo de implementação:**
```
<h1>Formulário de Contato</h1>

<input type="text" placeholder="Nome">
<input type="email" placeholder="E-mail">
<textarea placeholder="Digite sua mensagem aqui..."></textarea>

<button>Enviar</button>
```

## 2. Sequência com Significado  
- <b> O que é: </b> Garanta que a sequência do conteúdo faça sentido lógico e seja preservada em diferentes tamanhos de tela, garantindo também que os elementos focáveis na tela sigam uma ordem sequencial e lógica que preserve o significado do conteúdo, assegurando uma experiência de navegação previsível.  
- <b> Por que é importante: </b> Mantém a experiência de navegação previsível, facilitando o uso por todos, especialmente aqueles que dependem de navegação pelo teclado ou tecnologias assistivas.  

**Exemplo correto de implementação:**
```
 <header>
        <h1>Bem-vindo ao Site</h1>
        <nav>
            <ul>
                <li><a href="#home">Início</a></li>
                <li><a href="#sobre">Sobre Nós</a></li>
                <li><a href="#contato">Contato</a></li>
            </ul>
        </nav>
    </header>

    <main>
        <section id="home">
            <h2>Página Inicial</h2>
            <p>Conteúdo principal da página inicial.</p>
        </section>

        <section id="sobre">
            <h2>Sobre Nós</h2>
            <p>Informações sobre nossa empresa.</p>
        </section>

        <section id="contato">
            <h2>Contato</h2>
            <p>Formas de entrar em contato conosco.</p>
        </section>
    </main>

    <footer>
        <p>&copy; 2024 Empresa Exemplo</p>
    </footer>
```
**Contraexemplo de implementação:**
```
<section id="contato">
        <h2>Contato</h2>
        <p>Formas de entrar em contato conosco.</p>
    </section>

    <header>
        <h1>Bem-vindo ao Site</h1>
    </header>

    <section id="sobre">
        <h2>Sobre Nós</h2>
        <p>Informações sobre nossa empresa.</p>
    </section>

    <footer>
        <p>&copy; 2024 Empresa Exemplo</p>
    </footer>

    <section id="home">
        <h2>Página Inicial</h2>
        <p>Conteúdo principal da página inicial.</p>
    </section>
```
## 3. Página com Título  
- <b> O que é: </b> Certifique-se de que cada página tenha um título claro e descritivo que indique sua finalidade.  
- <b> Por que é importante: </b> Isso ajuda os usuários, especialmente aqueles que usam leitores de tela, a identificar rapidamente o propósito da página.

**Exemplo correto de implementação:**
```
"Formulário de Contato - Empresa XYZ"
```

**Contraexemplo de implementação:**
```
"Página 1"
```

## 4. Utilização de Características Sensoriais  
- <b> O que é: </b> Forneça instruções que não dependam apenas de características sensoriais como formato, cor ou posição, tais como “clique no botão abaixo”.  
- <b> Por que é importante: </b> Isso permite que usuários com deficiência visual ou daltonismo entendam as instruções sem dificuldades.

**Exemplo correto de implementação:**
```
"Selecione a opção que está à direita do campo de texto e clique no botão 'Enviar' para prosseguir."
```

**Contraexemplo de implementação:**
```
"Selecione a opção verde e clique no botão abaixo para continuar."
```

## 5. Nome, Função e Valor Programático  
- <b> O que é: </b> Certifique-se de que todos os componentes da interface do usuário, como formulários, links e elementos gerados por scripts, possam ser identificados e entendidos por tecnologias assistivas usando nome, função e valor programaticamente.  
- <b> Por que é importante: </b> Isso permite que tecnologias assistivas interpretem corretamente o conteúdo e sua função, tornando a navegação acessível.

**Exemplo correto de implementação:**
```
<form>
    <label for="email">E-mail:</label>
    <input type="email" id="email" name="email" aria-label="Campo para inserir o e-mail" aria-required="true">

    <label for="senha">Senha:</label>
    <input type="password" id="senha" name="senha" aria-label="Campo para inserir a senha" aria-required="true">

    <button type="submit" aria-label="Botão para enviar o formulário">Enviar</button>
</form>
```

**Contraexemplo de implementação:**
```
<form>
    <input type="text" placeholder="Digite seu e-mail">
    <input type="password" placeholder="Digite sua senha">
    <button>OK</button>
</form>
```

## 6. Conteúdo Não Textual  
- <b> O que é: </b> Forneça descrições textuais para todas as imagens, ícones e CAPTCHAs relevantes, garantindo que suas funções e conteúdos sejam compreensíveis por leitores de tela.  
- <b> Por que é importante: </b> Descrições textuais garantem que usuários de leitores de tela compreendam o propósito e o conteúdo visual.

**Exemplo correto de implementação:**
```
<h1>Perfil do Usuário</h1>
<img src="perfil.jpg" alt="Foto de perfil de João Silva sorrindo" />

<p>Clique no ícone abaixo para acessar suas mensagens:</p>
<a href="mensagens.html">
  <img src="icone-mensagem.png" alt="Ícone de envelope que representa mensagens" />
</a>
```

**Contraexemplo de implementação:**
```
<h1>Perfil do Usuário</h1>
<img src="perfil.jpg" alt="" />

<p>Clique no ícone abaixo para acessar suas mensagens:</p>
<a href="mensagens.html">
  <img src="icone-mensagem.png" />
</a>
```

## 7. Transcrições e Legendas  
- <b> O que é: </b> Forneça transcrições textuais para todo conteúdo de áudio e forneça legendas e/ou audiodescrições para todo conteúdo de vídeo.  
- <b> Por que é importante: </b> Isso garante o acesso de pessoas com deficiência auditiva ou visual ao conteúdo multimídia.  

## 8. Consistência em Formulários  
- <b> O que é: </b> Evite alterar o contexto do usuário ao interagir com campos de entrada de dados e cabeçalhos, a menos que haja confirmação explícita, de forma a manter a consistência e previsibilidade para os usuários ao preencher formulários, garantindo também que todos os rótulos descrevam claramente a finalidade dos campos, inclusive com instruções, se necessário.  
- <b> Por que é importante: </b> Ajuda o usuário a entender melhor o que é necessário preencher e evita confusões durante o processo de envio de formulários.  

**Exemplo correto de implementação:**
```
<h1>Inscreva-se no Curso XYZ</h1>
<form action="/submit" method="post">
    <label for="nome">Nome Completo:</label>
    <input type="text" id="nome" name="nome" required>

    <label for="email">E-mail:</label>
    <input type="email" id="email" name="email" required>

    <label for="telefone">Telefone:</label>
    <input type="tel" id="telefone" name="telefone">

    <p>Selecione seu nível de experiência:</p>
    <label for="iniciante">
        <input type="radio" id="iniciante" name="nivel" value="iniciante"> Iniciante
    </label>
    <label for="intermediario">
        <input type="radio" id="intermediario" name="nivel" value="intermediario"> Intermediário
    </label>
    <label for="avancado">
        <input type="radio" id="avancado" name="nivel" value="avancado"> Avançado
    </label>

    <button type="submit">Enviar</button>
</form>
```

**Contraexemplo de implementação:**
```
<h1>Inscrição</h1>
<form action="/submit" method="post">
  <input type="text" name="name" placeholder="Nome Completo">

  <input type="email" name="email" placeholder="E-mail">

  <input type="tel" name="phone" placeholder="Telefone">

  <select name="nivel">
      <option value="iniciante">Iniciante</option>
      <option value="intermediario">Intermediário</option>
      <option value="avancado">Avançado</option>
  </select>

  <!-- Ao clicar no campo de telefone, o formulário é enviado -->
  <input type="submit" value="Enviar">
</form>
```

## 9. Entrada Redundante  
- <b> O que é: </b> Evite pedir informações repetidas durante o preenchimento de um formulário em etapas, a menos que seja essencial (como para confirmação de senha).  
- <b> Por que é importante: </b> Simplifica o preenchimento de formulários, economizando tempo e esforço dos usuários.

**Exemplo correto de implementação:**
```
<h1>Endereço de Entrega</h1>
<form action="/submit" method="post">
    <label for="nome">Nome Completo:</label>
    <input type="text" id="nome" name="nome" required>

    <label for="endereco">Endereço de Entrega:</label>
    <input type="text" id="endereco" name="endereco" required>

    <label for="cidade">Cidade:</label>
    <input type="text" id="cidade" name="cidade" required>

    <label for="estado">Estado:</label>
    <input type="text" id="estado" name="estado" required>

    <label for="cep">CEP:</label>
    <input type="text" id="cep" name="cep" required>

    <p>
        <input type="checkbox" id="mesmo-endereco" name="mesmo-endereco">
        <label for="mesmo-endereco">Usar o mesmo endereço para cobrança</label>
    </p>

    <button type="submit">Prosseguir para Pagamento</button>
</form>
```

**Contraexemplo de implementação:**
```
 <h1>Endereço de Entrega</h1>
<form action="/submit" method="post">
    <label for="nome">Nome Completo:</label>
    <input type="text" id="nome" name="nome" required>

    <label for="endereco">Endereço de Entrega:</label>
    <input type="text" id="endereco" name="endereco" required>

    <label for="cidade">Cidade:</label>
    <input type="text" id="cidade" name="cidade" required>

    <label for="estado">Estado:</label>
    <input type="text" id="estado" name="estado" required>

    <label for="cep">CEP:</label>
    <input type="text" id="cep" name="cep" required>

    <h2>Endereço de Cobrança</h2>
    <label for="nome-cobranca">Nome Completo:</label>
    <input type="text" id="nome-cobranca" name="nome-cobranca" required>

    <label for="endereco-cobranca">Endereço de Cobrança:</label>
    <input type="text" id="endereco-cobranca" name="endereco-cobranca" required>

    <label for="cidade-cobranca">Cidade:</label>
    <input type="text" id="cidade-cobranca" name="cidade-cobranca" required>

    <label for="estado-cobranca">Estado:</label>
    <input type="text" id="estado-cobranca" name="estado-cobranca" required>

    <label for="cep-cobranca">CEP:</label>
    <input type="text" id="cep-cobranca" name="cep-cobranca" required>

    <button type="submit">Prosseguir para Pagamento</button>
</form>
```

## 10. Identificação e Correção de Erros  
- <b> O que é: </b> Certifique-se de que os erros sejam claramente identificados visual e auditivamente, usando, por exemplo, mudança de cor, ícone e som de alerta e uma mensagem de texto. Garantir também que exista uma sugestão clara de onde o erro ocorre e como pode ser solucionado.  
- <b> Por que é importante: </b> Facilita a correção de erros por usuários com diferentes habilidades, melhorando a experiência e eficiência.

**Exemplo correto de implementação:**
```
<h1>Registro</h1>
<form id="formulario" action="/submit" method="post">
    <label for="email">E-mail:</label>
    <input type="email" id="email" name="email" required>
    <span id="email-error" class="error" style="display: none;">Por favor, insira um e-mail válido.</span><br><br>

    <label for="senha">Senha:</label>
    <input type="password" id="senha" name="senha" required>
    <span id="senha-error" class="error" style="display: none;">A senha deve ter pelo menos 8 caracteres.</span><br><br>

    <button type="submit">Registrar</button>
</form>

<script>
    document.getElementById('formulario').addEventListener('submit', function(event) {
        var email = document.getElementById('email');
        var senha = document.getElementById('senha');
        var emailError = document.getElementById('email-error');
        var senhaError = document.getElementById('senha-error');
        
        // Resetando os erros
        emailError.style.display = 'none';
        senhaError.style.display = 'none';
        email.classList.remove('error');
        senha.classList.remove('error');
        
        if (!email.validity.valid) {
            event.preventDefault();
            emailError.style.display = 'inline';
            email.classList.add('error');
        }

        if (senha.value.length < 8) {
            event.preventDefault();
            senhaError.style.display = 'inline';
            senha.classList.add('error');
        }
    });
</script>
```

**Contraexemplo de implementação:**
```
 <h1>Registro</h1>
<form action="/submit" method="post">
  <label for="email">E-mail:</label>
  <input type="email" id="email" name="email" required><br><br>
  
  <label for="senha">Senha:</label>
  <input type="password" id="senha" name="senha" required><br><br>
  
  <button type="submit">Registrar</button>
</form>
```

## 11. Finalidade do Link  
- <b> O que é: </b> Cada link deve ter um texto descritivo ou estar envolvido por contexto que indique claramente sua finalidade.  
- <b> Por que é importante: </b> Evita confusões para todos os usuários, especialmente aqueles que utilizam tecnologias assistivas.  

## 12. Cancelamento de Acionamento  
- <b> O que é: </b> Certifique-se de que é possível cancelar um clique ou toque acidental antes de liberar o botão e evite depender do movimento do dispositivo para controle de conteúdo, permitindo desativação para evitar acionamentos acidentais.  
- <b> Por que é importante: </b> Isso previne erros, especialmente em dispositivos móveis, onde toques acidentais são comuns.  

## 13. Gestos Táteis  
- <b> O que é: </b> Todas as funções que requerem gestos táteis (como arrastar com o dedo em telas sensíveis ao toque) devem ter uma alternativa que permita interação por um único ponto.  
- <b> Por que é importante: </b> Garante que pessoas com mobilidade reduzida possam interagir com a interface sem dificuldades.  

## 14. Navegação por Teclado  
- <b> O que é: </b> Garanta que todas as funcionalidades possam ser operadas apenas com o teclado (exceto quando o controle manual for necessário para a função específica), permitindo que a navegação por todos os elementos “clicáveis” seja ininterrupta ao interagir via teclado.  
- <b> Por que é importante: </b> Isso permite a navegação por pessoas que não utilizam o mouse, como usuários de leitores de tela ou com deficiências motoras.  

## 15. Ignorar Blocos Repetitivos  
- <b> O que é: </b> Forneça um meio para usuários de teclado ignorarem conteúdos repetitivos, como menus de navegação, para facilitar a navegação.  
- <b> Por que é importante: </b> Isso melhora a eficiência da navegação, permitindo que os usuários cheguem diretamente ao conteúdo principal.  

## 16. Controle de Tempo e Movimentos Automáticos  
- <b> O que é: </b> Permita que os usuários desativem, ajustem ou estendam qualquer limite de tempo definido no aplicativo ou site e que controlem qualquer movimento automático, piscar ou rolar na tela, com a opção de pausar, parar ou ocultar.  
- <b> Por que é importante: </b> Isso evita frustrações e garante que o usuário tenha controle total sobre sua experiência de navegação.  

## 17. Rótulo no Nome Acessível  
- <b> O que é: </b> Garanta que o nome dos controles coincida com seus rótulos visíveis para facilitar a interação por voz.  
- <b> Por que é importante: </b> Facilita a navegação por comando de voz, tornando a experiência acessível para pessoas com deficiência motora.  

## 18. Ajuda Consistente  
- <b> O que é: </b> Mantenha o formato da ajuda consistente em todas as telas onde ela é oferecida, incluindo opções de contato humano e sistemas automatizados.  
- <b> Por que é importante: </b> Isso torna mais fácil para o usuário encontrar e utilizar a ajuda quando necessário, melhorando a experiência de suporte.  

## 19. Audiodescrição para Vídeos  
- <b> O que é: </b> Certifique-se de que seja fornecida audiodescrição para todo o conteúdo de vídeo pré-gravado. Qualquer vídeo que foi gravado e está sendo disponibilizado online deve ter uma trilha adicional que descreva o que está acontecendo visualmente no vídeo.  
- <b> Por que é importante: </b> Torna o conteúdo visual acessível para pessoas com deficiência visual, descrevendo o que acontece no vídeo.  

## 20. Contraste de Texto e Imagens  
- <b> O que é: </b> Garanta a legibilidade do texto e das imagens de texto, assegurando que tenham um contraste suficiente em relação ao fundo da página. Também deve-se oferecer a personalização do contraste, permitindo escolhas de fundo e cor de texto.  
- <b> Por que é importante: </b> Um bom contraste garante a legibilidade do conteúdo, beneficiando usuários com baixa visão e outras dificuldades visuais.
