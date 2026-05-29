# Jogo da Forca Inclusivo (Versão Demo)

Um Jogo da Forca clássico projetado sob a filosofia do **Design Universal**. Este projeto não foi feito "para nichos de acessibilidade", mas sim para ser uma ferramenta de entretenimento **inclusiva**, onde qualquer pessoa — utilizando leitor de tela, teclado físico, comandos por toque ou jogando sem áudio — pode competir e se divertir de igual para igual, compartilhando a mesma tela.

O projeto é totalmente autocontido em um **único arquivo HTML** (HTML, CSS e JavaScript), sem dependências externas de imagens ou arquivos de áudio pesados, sendo ideal para hospedagem imediata no **GitHub Pages**.

---

## 🚀 Recursos de Destaque

### 🎮 Dinâmica de Controle Fluida
* **Sem barreiras de interface:** O jogo descarta teclados virtuais poluídos que travam a navegação por leitores de tela. Ele utiliza uma caixa de texto padrão (`<input>`) nativa e acessível.
* **Foco Inteligente Automatizado:** Ao digitar seu palpite e pressionar `Enter`, o foco é transferido via código para o painel de status para anunciar o resultado e, em menos de um segundo, retorna sozinho para o campo de texto. Isso garante agilidade máxima na digitação.
* **Prevenção de Erros Intercalados:** Se um caractere inválido (números, símbolos) ou uma letra repetida for digitada, a interface bloqueia a ação, emite um aviso sonoro/textual dedicado e limpa o campo sem penalizar as vidas do jogador.

### 🔊 Identidade Sonora Dinâmica (Web Audio API)
Todos os bipes do jogo são sintetizados diretamente pelo navegador via código (ondas senoidais, triangulares e dente de serra):
* **Silhueta Sonora da Palavra:** Ao acertar ou iniciar uma rodada, o jogo varre a palavra da esquerda para a direita em bipes rápidos. Letras descobertas emitem um bipe agudo cristalino, e letras ocultas emitem um bipe curto e seco. É possível "ouvir" o desenho da palavra.
* **Escalonamento de Tensão:** A cada erro cometido, o jogo reproduz a sequência de falhas acumuladas em tons progressivos (do mais grave ao mais agudo), sinalizando auditivamente a aproximação do enforcamento.
* **Fanfarras de Estado:** Efeitos melódicos exclusivos para Vitória e Game Over.

### 🎨 Visual Moderno e Semântica Rígida
* **Interface Escura (Dark Mode):** Cores contrastantes e elegantes com foco visual ciano brilhante, garantindo conforto e nitidez para quem joga olhando para a tela.
* **Ilustração em SVG Nativo:** A forca clássica (cabeça, tronco, braços e pernas) é renderizada de forma responsiva via vetores diretos no documento, possuindo transições suaves de exibição.
* **Independência de Áudio:** Caso o jogador esteja jogando no mudo ou em ambientes barulhentos, um painel de status textual descreve em tempo real a parte exata do corpo que foi desenhada.

---

## 🏁 Regras da Demo

* Cada palavra descoberta confere **100 pontos** ao jogador.
* Letras com acento (como `Ã`, `É`, `Ó`) são tratadas automaticamente. Se a palavra secreta contiver acentuação, o palpite da letra limpa (como `A`, `E`, `O`) será aceito perfeitamente.
* **Condição de Vitória:** O jogador precisa somar **500 pontos** (descobrir 5 palavras) para vencer a partida da Demo.
* **Condição de Derrota:** Caso o boneco da forca seja completamente desenhado (6 erros acumulados), a partida é encerrada imediatamente com Game Over e o placar é resetado.

---

## 🛠️ Tecnologias Utilizadas

* **HTML5:** Estrutura semântica com atributos ARIA para acessibilidade nativa.
* **CSS3:** Layout flexível, centralizado e responsivo com variáveis de cores (CSS Variables).
* **JavaScript (Vanilla):** Lógica de estados, gerenciamento de foco e manipulação de strings (normalização de acentos).
* **Web Audio API:** Sintetização de áudio em tempo real por osciladores nativos.

---

## 📦 Como Executar o Projeto

Como o jogo foi construído inteiramente em um único arquivo, o processo de execução é imediato:

1. Baixe o arquivo `index.html` (ou copie o código fonte).
2. Dê um duplo clique no arquivo para abri-lo diretamente em qualquer navegador moderno (Chrome, Edge, Firefox, Safari).
3. **Para Hospedar:** Suba o arquivo para um repositório no seu GitHub e ative o **GitHub Pages** nas configurações do projeto para gerar um link público e jogar direto pelo celular ou PC.

---

## 👤 Autor

* **Anderson Carvalho**
* **Contato:** [euconcego@gmail.com](mailto:euconcego@gmail.com)
