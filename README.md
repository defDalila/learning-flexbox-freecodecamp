# <p align="center"><font color='#FF79C6'><strong>Learn CSS Flexbox by Building a Photo Galery</strong></font></p>

<p align="center"> <i>Módulo de treinamento para a certificação <a href="https://www.freecodecamp.org/learn/2022/responsive-web-design/"><em>Responsive Web Design Certification</em></a> da plataforma FreeCodeCamp</i>.
<p>

<p align="center">
    <img src="https://skillicons.dev/icons?i=html,css,md,vscode,git,github,figma" height="30px">
</p>


<br>

## :memo: <font color='#8BE9FD'><strong>Notas de Aula</strong></font>

<br>

:ballot_box_with_check: Para centralizar o título no `header` e melhorar o layout, podemos usar o **CSS Flexbox**. Isso nos permitirá alinhar o título tanto horizontal quanto verticalmente. Além disso, vamos adicionar um pouco de estilo para tornar o cabeçalho mais atraente.


<details>

<summary><font color='#50FA7B'><strong>Exibir Exemplo de Código</strong></font></summary>

### :star: <font color='#BD93F9'><strong>Exemplo</strong></font> :star:

```css
.header {
  display: flex;           /* Usa Flexbox para o layout */
  justify-content: center; /* Centraliza horizontalmente */
  align-items: center;     /* Centraliza verticalmente */
  height: 100vh;           /* Ocupa a altura total da tela */
  background-color: #f0f0f0; /* Cor de fundo suave */
  text-align: center;      /* Garante que o texto do h1 seja centralizado */
}

h1 {
  font-size: 3rem;         /* Tamanho de fonte grande */
  color: #333;             /* Cor do texto */
  margin: 0;               /* Remove a margem padrão */
  font-family: 'Arial', sans-serif; /* Fonte limpa e moderna */
}
```

### Explicação:
- **`display: flex;`** → Usamos Flexbox para tornar o layout mais flexível.
- **`justify-content: center;`** → Alinha o conteúdo horizontalmente no centro.
- **`align-items: center;`** → Alinha o conteúdo verticalmente no centro.
- **`height: 100vh;`** → Faz o cabeçalho ocupar 100% da altura da tela.
- **`background-color: #f0f0f0;`** → Adiciona um fundo suave para o cabeçalho.
- **`font-size: 3rem;`** → Aumenta o tamanho da fonte para o título.
- **`color: #333;`** → Define uma cor escura e legível para o texto.


 </details> 

<br>

:ballot_box_with_check: Para corrigir o problema onde a borda da imagem se estende além da borda do contêiner devido ao modelo de caixa padrão do navegador, podemos usar a propriedade `box-sizing`. Definir `box-sizing: content-box;` irá garantir que as bordas e o preenchimento (padding) não afetem o tamanho da largura e altura do elemento.

- Usaremos o seletor global `*` para aplicar essa propriedade a todos os elementos, incluindo as imagens.


<details>

<summary><font color='#50FA7B'><strong>Exibir Exemplo de Código</strong></font></summary>

### :star: <font color='#BD93F9'><strong>Exemplo</strong></font> :star:

```css
/* Aplica box-sizing: content-box a todos os elementos */
* {
  box-sizing: content-box;
}
```


 </details> 

<br>


> [!NOTE]
> - **`box-sizing: content-box;`** → Define que o cálculo de largura e altura de cada elemento não incluirá as bordas nem o preenchimento. Isso significa que qualquer borda e preenchimento será **adicionado** ao tamanho do elemento, fazendo com que o contêiner precise ser maior para acomodar esses valores.
> - Como está usando o valor padrão `content-box`, essa alteração não resultará em mudanças visíveis imediatamente, mas é útil para garantir que o comportamento da caixa seja consistente.


<br>

:ballot_box_with_check: O modelo de dimensionamento **`border-box`** é muito útil, pois faz com que a largura e altura de um elemento incluam as bordas e o preenchimento (padding), o que significa que a dimensão definida para o elemento será a **largura total**, incluindo o conteúdo, a borda e o preenchimento.

- Usar **`box-sizing: border-box;`** ajuda a evitar que o tamanho de um elemento se expanda inesperadamente devido a bordas e preenchimento.


<details>

<summary><font color='#50FA7B'><strong>Exibir Exemplo de Código</strong></font></summary>

### :star: <font color='#BD93F9'><strong>Exemplo</strong></font> :star:

```css
/* Aplica box-sizing: border-box a todos os elementos */
* {
  box-sizing: border-box;
}
```


 </details> 

<br>



> [!IMPORTANT]
> - **`box-sizing: border-box;`** → Com este modelo, a largura e altura de um elemento serão o valor exato definido, incluindo **borda** e **preenchimento**. O conteúdo será reduzido, se necessário, para se ajustar dentro da caixa com as bordas e o preenchimento incluídos.
> Usar esse modelo de caixa garante um layout mais previsível, especialmente ao trabalhar com margens, bordas e preenchimento, tornando o design mais fácil de controlar.

<br>

:ballot_box_with_check: O **Flexbox** é uma poderosa ferramenta de layout em CSS, permitindo o controle eficiente da distribuição e alinhamento dos itens dentro de um contêiner. Com ele, você pode organizar os itens de maneira flexível e responsiva, tanto em uma linha (horizontalmente) quanto em uma coluna (verticalmente).

> [!TIP]
> 1. **Defina o contêiner como um flex container**:   Para tornar um elemento um contêiner flexível, basta definir a propriedade `display` como `flex`.
> 2. **Os filhos diretos do contêiner flexível são chamados de flex items**.


<details>

<summary><font color='#50FA7B'><strong>Exibir Exemplo de Código</strong></font></summary>

### :star: <font color='#BD93F9'><strong>Exemplo</strong></font> :star:

```css
.gallery {
  display: flex;  /* Torna o contêiner um flex container */
  flex-wrap: wrap; /* Permite que os itens quebrem para a linha seguinte, se necessário */
  gap: 10px; /* Adiciona um espaçamento entre os itens */
}
```
- **`display: flex;`** → Torna o elemento com a classe `.gallery` um contêiner flexível.
- **`flex-wrap: wrap;`** → Permite que os itens dentro do contêiner se movam para a próxima linha se não houver espaço suficiente.
- **`gap: 10px;`** → Adiciona um espaço de 10px entre os itens da galeria.
- Agora, os itens dentro de `.gallery` serão distribuídos automaticamente de forma flexível, ajustando-se conforme o espaço disponível e garantindo que os itens fiquem bem organizados! 🎨✨
 </details> 

<br>

:ballot_box_with_check:  O **Flexbox** utiliza dois eixos principais: o **eixo principal** (main axis) e o **eixo cruzado** (cross axis). O eixo principal é determinado pela propriedade **`flex-direction`**, que define a direção dos itens flexíveis dentro do contêiner.

- Valores possíveis para **`flex-direction`**:

1. **`row` (padrão)**:
   - O eixo principal é **horizontal**.
   - Os itens são dispostos da **esquerda para a direita**.
   - Usado quando você quer que os itens fiquem organizados na linha horizontal.

<br>

   ```css
   .gallery {
     display: flex;
     flex-direction: row; /* Itens alinhados na linha horizontal */
   }
   ```
<br>

2. **`row-reverse`**:
   - O eixo principal é **horizontal**.
   - Os itens são dispostos da **direita para a esquerda**.
   - Usado quando você deseja que os itens apareçam em ordem inversa na linha horizontal.

<br>

   ```css
   .gallery {
     display: flex;
     flex-direction: row-reverse; /* Itens alinhados da direita para a esquerda */
   }
   ```
<br>

3. **`column`**:
   - O eixo principal é **vertical**.
   - Os itens são dispostos de **cima para baixo**.
   - Usado quando você quer que os itens sejam dispostos em uma coluna.

<br>

   ```css
   .gallery {
     display: flex;
     flex-direction: column; /* Itens alinhados na coluna vertical */
   }
   ```
<br>

4. **`column-reverse`**:
   - O eixo principal é **vertical**.
   - Os itens são dispostos de **baixo para cima**.
   - Usado quando você deseja que os itens apareçam na coluna de baixo para cima.

<br>


   ```css
   .gallery {
     display: flex;
     flex-direction: column-reverse; /* Itens alinhados de baixo para cima */
   }
   ```
<br>

> [!NOTE]
> - A direção dos eixos pode variar dependendo da direção do texto (da esquerda para a direita ou da direita para a esquerda). Os valores apresentados são para uma direção de texto **da esquerda para a direita** (LTR).
> Agora, você pode controlar facilmente o layout de seus itens flexíveis, ajustando a direção dos eixos conforme necessário! 📏📐


<br>

:ballot_box_with_check: A propriedade **`flex-wrap`** controla como os itens flexíveis se comportam quando o contêiner flexível não tem espaço suficiente para acomodá-los. Ela determina se os itens devem **quebrar para a próxima linha ou coluna** ou se devem **ser comprimidos** para caber no espaço disponível.

- Valores possíveis para **`flex-wrap`**:

1. **`wrap`**:
   - Quando o contêiner não tiver espaço suficiente, os itens **se moverão para a próxima linha ou coluna**.
   - Isso permite que os itens se ajustem e ocupem mais de uma linha ou coluna, se necessário.
<br>

   ```css
   .gallery {
     display: flex;
     flex-wrap: wrap; /* Itens irão quebrar e ocupar mais de uma linha/coluna se necessário */
   }
   ```
<br>

2. **`nowrap`** (padrão):
   - Os itens **não vão quebrar** para a próxima linha ou coluna. Eles **serão comprimidos** para se ajustarem dentro do contêiner.
   - Esse é o comportamento padrão, onde os itens são mantidos em uma única linha ou coluna, e podem ser redimensionados para caber no espaço disponível.
<br>

   ```css
   .gallery {
     display: flex;
     flex-wrap: nowrap; /* Itens não irão quebrar e serão comprimidos para caber no contêiner */
   }
   ```
<br>

3. **`wrap-reverse`**:
   - Os itens **se moverão para a próxima linha ou coluna**, mas a ordem será **invertida**. Ou seja, a linha ou coluna de maior prioridade será posicionada no final.
   - Útil se você quiser controlar a direção do fluxo dos itens ao quebrar.
<br>

   ```css
   .gallery {
     display: flex;
     flex-wrap: wrap-reverse; /* Itens irão quebrar, mas a direção será invertida */
   }
   ```
<br>

<details>

<summary><font color='#50FA7B'><strong>Exibir Exemplo de Código</strong></font></summary>

### :star: <font color='#BD93F9'><strong>Exemplo</strong></font> :star:


```css
.gallery {
  display: flex;
  flex-wrap: wrap; /* Itens irão quebrar para a próxima linha, se necessário */
  gap: 10px; /* Espaço entre os itens */
}

img {
  width: 200px; /* Defina o tamanho da imagem */
  height: 200px;
}
```

Neste exemplo, quando o contêiner `.gallery` não tiver espaço suficiente para acomodar todas as imagens em uma linha, as imagens **quebrarão para a próxima linha** e serão organizadas conforme o espaço disponível.

A **`flex-wrap`** oferece mais flexibilidade e controle, especialmente em layouts responsivos! 📱💻

 </details> 

<br>


:ballot_box_with_check: A propriedade **`justify-content`** no Flexbox é usada para alinhar os itens flexíveis ao longo do **eixo principal** (main axis). Ela controla como os itens dentro de um contêiner flexível são **distribuídos** e **posicionados** ao longo da linha ou coluna definida pela propriedade **`flex-direction`**.

- Valores possíveis para **`justify-content`**:

1. **`flex-start`** (padrão): Os itens são **alinhados ao início** do contêiner ao longo do eixo principal.
   - No caso de uma linha (com `flex-direction: row`), os itens estarão alinhados à **esquerda**.

<br>

   ```css
   .gallery {
     display: flex;
     justify-content: flex-start; /* Itens alinhados ao início (esquerda) */
   }
   ```

<br>

1. **`flex-end`**: Os itens são **alinhados ao final** do contêiner ao longo do eixo principal.
   - Para uma linha, os itens serão alinhados à **direita**.

<br>

   ```css
   .gallery {
     display: flex;
     justify-content: flex-end; /* Itens alinhados ao final (direita) */
   }
   ```

<br>

1. **`center`**: Os itens são **centralizados** dentro do contêiner ao longo do eixo principal.

<br>

   ```css
   .gallery {
     display: flex;
     justify-content: center; /* Itens centralizados */
   }
   ```

<br>

1. **`space-between`**:  Os itens são distribuídos de maneira que o **espaço restante seja dividido igualmente** entre os itens, mas o primeiro item será alinhado ao início e o último ao final do contêiner.

<br>

   ```css
   .gallery {
     display: flex;
     justify-content: space-between; /* Espaço entre os itens */
   }
   ```

<br>

5. **`space-around`**: Os itens são distribuídos com um **espaço igual antes do primeiro item, entre os itens e após o último item**.

<br>

   ```css
   .gallery {
     display: flex;
     justify-content: space-around; /* Espaço igual ao redor dos itens */
   }
   ```

<br>

6. **`space-evenly`**: Os itens são distribuídos de forma que o **espaço entre todos os itens, incluindo o espaço antes do primeiro e após o último item, seja igual**.

<br>

   ```css
   .gallery {
     display: flex;
     justify-content: space-evenly; /* Espaço igual entre todos os itens */
   }
   ```

<br>

<details>

<summary><font color='#50FA7B'><strong>Exibir Exemplo de Código</strong></font></summary>

### :star: <font color='#BD93F9'><strong>Exemplo</strong></font> :star:


```css
.gallery {
  display: flex;
  justify-content: space-between; /* Distribui os itens com espaços iguais entre eles */
  gap: 10px;
}

img {
  width: 150px;
  height: 150px;
}
```

Neste exemplo, as imagens dentro do contêiner `.gallery` serão distribuídas com **espaços iguais** entre elas, começando da **esquerda para a direita** (se a direção for `row`).

A **`justify-content`** é muito útil para controlar como os itens são distribuídos ao longo do contêiner e ajuda a criar layouts mais organizados e flexíveis. 🖼️✨

 </details> 

<br>


:ballot_box_with_check: A propriedade **`align-items`** no Flexbox é usada para alinhar os itens flexíveis ao longo do **eixo transversal** (cross axis), que é o eixo **perpendicular** ao **eixo principal**. Enquanto o **eixo principal** é controlado pela propriedade **`flex-direction`**, o **eixo transversal** é orientado de forma oposta. Por exemplo, se os itens são organizados ao longo de uma linha (`flex-direction: row`), o eixo transversal será vertical.

- Valores possíveis para **`align-items`**:

1. **`stretch`** (padrão): Os itens **se esticam** para preencher o contêiner ao longo do eixo transversal. Isso significa que, se o contêiner for maior que o conteúdo, os itens irão se expandir para preencher o espaço disponível.
   
   ```css
   .gallery {
     display: flex;
     align-items: stretch; /* Itens esticados para preencher o contêiner */
   }
   ```

1. **`flex-start`**: Os itens são **alinhados ao início** do contêiner ao longo do eixo transversal. Para uma direção `row`, isso significa que os itens serão alinhados à parte superior do contêiner.
   
   ```css
   .gallery {
     display: flex;
     align-items: flex-start; /* Alinha os itens ao topo do contêiner */
   }
   ```

2. **`flex-end`**: Os itens são **alinhados ao final** do contêiner ao longo do eixo transversal. Para uma direção `row`, isso significa que os itens serão alinhados à parte inferior do contêiner.
   
   ```css
   .gallery {
     display: flex;
     align-items: flex-end; /* Alinha os itens à parte inferior do contêiner */
   }
   ```

3. **`center`**: Os itens são **centralizados** dentro do contêiner ao longo do eixo transversal. Eles serão alinhados no meio do contêiner.
   
   ```css
   .gallery {
     display: flex;
     align-items: center; /* Alinha os itens ao centro verticalmente */
   }
   ```

4. **`baseline`**: Os itens são alinhados de forma que **as linhas de base** de seus textos fiquem alinhadas. Este valor é útil quando os itens contêm texto ou quando você deseja alinhar os itens baseados nas linhas de texto.
   
   ```css
   .gallery {
     display: flex;
     align-items: baseline; /* Alinha os itens pela linha de base do texto */
   }
   ```

<details>

<summary><font color='#50FA7B'><strong>Exibir Exemplo de Código</strong></font></summary>

### :star: <font color='#BD93F9'><strong>Exemplo</strong></font> :star:


```css
.gallery {
  display: flex;
  align-items: center; /* Alinha os itens verticalmente no centro do contêiner */
  gap: 10px;
}

img {
  width: 150px;
  height: 150px;
}
```

Neste exemplo, as imagens dentro do contêiner `.gallery` serão **centralizadas verticalmente** dentro do contêiner.

A **`align-items`** é útil para controlar o **alinhamento vertical** (ou horizontal, dependendo da direção do eixo principal) dos itens dentro do contêiner flexível, criando layouts mais flexíveis e organizados. 🎨📐

 </details> 

<br>


:ballot_box_with_check: A propriedade **`object-fit`** é usada para controlar como o conteúdo de um elemento de mídia (como uma imagem ou um vídeo) deve se ajustar ao seu contêiner, mantendo ou não a proporção original. Quando você está lidando com imagens que têm diferentes proporções de aspecto, o **`object-fit`** pode ajudar a evitar que as imagens se distorçam ao se ajustarem ao espaço disponível.

- Valores possíveis para **`object-fit`**:

1. **`fill`**: A imagem será esticada para **preencher completamente** o contêiner, o que pode resultar em distorção da imagem.
   
   ```css
   img {
     object-fit: fill;
   }
   ```

1. **`contain`**: A imagem será redimensionada para **caber dentro** do contêiner, mantendo sua proporção original. Se necessário, serão adicionadas áreas em branco ao redor da imagem para preencher o espaço extra.
   
   ```css
   img {
     object-fit: contain; /* Mantém a proporção da imagem */
   }
   ```

2. **`cover`**: A imagem será redimensionada para **preencher todo o contêiner** sem distorção, mas pode **cortar** a imagem se a proporção do contêiner for diferente da da imagem.
   
   ```css
   img {
     object-fit: cover; /* Cobre o contêiner sem distorcer a imagem */
   }
   ```

3. **`none`**: A imagem **não será redimensionada** e manterá seu tamanho original, podendo ultrapassar o contêiner.
   
   ```css
   img {
     object-fit: none; /* A imagem mantém seu tamanho original */
   }
   ```

4. **`scale-down`**: A imagem será redimensionada para **ficar menor** que seu tamanho original, se necessário. É uma combinação de `contain` e `none`, pois ela redimensiona a imagem apenas se for maior do que o contêiner.
   
   ```css
   img {
     object-fit: scale-down; /* Redimensiona a imagem para caber no contêiner */
   }
   ```

<details>

<summary><font color='#50FA7B'><strong>Exibir Exemplo de Código</strong></font></summary>

### :star: <font color='#BD93F9'><strong>Exemplo</strong></font> :star:

```css
.gallery {
  display: flex;
  justify-content: space-between;
  gap: 10px;
}

img {
  width: 150px;
  height: 150px;
  object-fit: cover; /* A imagem cobre o espaço sem distorção */
}
```


- Usando **`object-fit: cover`**, as imagens dentro da `.gallery` vão se ajustar para **preencher completamente o espaço** de 150px por 150px, mantendo sua proporção, mas podem ser **cortadas** se a proporção da imagem for diferente da do contêiner.

Ao usar **`object-fit`**, você garante que as imagens não fiquem distorcidas, independentemente das suas proporções originais, o que cria um layout mais bonito e profissional para a galeria de fotos ou outros elementos de mídia. 📸🎨


 </details> 

<br>

:ballot_box_with_check: A propriedade **`gap`** no CSS é usada para definir o **espaçamento entre itens** dentro de um contêiner flexível, de grade (grid), ou de várias colunas. Ela é muito útil quando se quer um controle de espaçamento uniforme entre os elementos, sem precisar definir margens individuais para cada item.

- Sintaxe de `gap`:

```css
.container {
  gap: <row-gap> <column-gap>;
}
```

- **`<row-gap>`**: Define o espaçamento entre as linhas (horizontal ou vertical, dependendo do layout).
- **`<column-gap>`**: Define o espaçamento entre as colunas (horizontal ou vertical, dependendo do layout).

Se você usar apenas um valor, ele será aplicado tanto para **`row-gap`** quanto para **`column-gap`**.

- Exemplos:

1. **Espaçamento entre linhas e colunas com valores diferentes**:

```css
.container {
  display: grid;
  gap: 20px 10px; /* 20px entre as linhas e 10px entre as colunas */
}
```

2. **Espaçamento uniforme entre as linhas e colunas**:

```css
.container {
  display: grid;
  gap: 15px; /* Aplica 15px de espaçamento entre linhas e colunas */
}
```

3. **Usando `gap` em um layout flex**:

```css
.container {
  display: flex;
  flex-wrap: wrap;
  gap: 15px; /* Aplica 15px de espaçamento entre os itens */
}
```

- Propriedades Subjacentes:
  - **`row-gap`**: Define o espaçamento entre as **linhas**.
  - **`column-gap`**: Define o espaçamento entre as **colunas**.


<details>

<summary><font color='#50FA7B'><strong>Exibir Exemplo de Código</strong></font></summary>

### :star: <font color='#BD93F9'><strong>Exemplo</strong></font> :star:

```css
.container {
  display: grid;
  row-gap: 20px; /* Espaçamento entre linhas */
  column-gap: 10px; /* Espaçamento entre colunas */
}
```

- **Compatibilidade**: A propriedade **`gap`** funciona bem com:
  - **Flexbox** (a partir do CSS Flexbox Level 1).
  - **CSS Grid** (a partir do CSS Grid Layout).
  - **Layouts de múltiplas colunas**.

Usar **`gap`** é uma maneira eficaz de controlar o espaçamento em layouts modernos sem precisar usar margens manuais, simplificando o código e mantendo a consistência visual.


 </details> 

<br>

:ballot_box_with_check: A pseudo-classe **`::after`** no CSS é usada para inserir conteúdo após o conteúdo de um elemento selecionado. Pode ser útil para adicionar elementos visuais ou outros elementos decorativos, sem a necessidade de modificar o HTML.

:ballot_box_with_check: No caso de uma galeria de imagens, você pode usar **`::after`** para adicionar um elemento após a última imagem. Se você definir o mesmo **`width`** para o pseudo-elemento como o das imagens, isso pode **empurrar a última imagem para a esquerda** quando a galeria estiver em um layout de duas colunas, por exemplo.

<details>

<summary><font color='#50FA7B'><strong>Exibir Exemplo de Código</strong></font></summary>

### :star: <font color='#BD93F9'><strong>Exemplo</strong></font> :star:


```css
.gallery {
  display: grid;
  grid-template-columns: repeat(2, 1fr); /* 2 colunas */
  gap: 10px;
}

.gallery img {
  width: 100%; /* As imagens ocupam 100% do espaço disponível em cada célula da grid */
}

.gallery::after {
  content: ""; /* Cria um elemento vazio */
  display: block; /* Torna o pseudo-elemento um bloco */
  width: 100%; /* O mesmo tamanho das imagens */
}
```



- **`grid-template-columns: repeat(2, 1fr)`**: Isso cria uma grade com **2 colunas** de tamanhos iguais.
- **`gap: 10px`**: Define um espaçamento de **10px** entre as colunas e as linhas da galeria.
- **`::after`**: Cria um pseudo-elemento após o conteúdo da `.gallery`. 
  - **`content: ""`** cria um **elemento vazio**.
  - **`display: block`** faz com que o pseudo-elemento ocupe um espaço de bloco, ou seja, ele vai quebrar a linha.
  - **`width: 100%`** define a largura do pseudo-elemento igual à das imagens.


Quando a galeria for exibida em duas colunas, o **pseudo-elemento** vai ocupar a largura da **última imagem**, o que fará com que a última imagem seja empurrada para a **esquerda**. Isso pode ser útil para alinhar corretamente os itens e garantir que o layout da galeria fique consistente.

 </details> 

<br>


