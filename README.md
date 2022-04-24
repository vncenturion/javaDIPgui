# javaDIPgui
 Atividade disciplina de processamento de imagens.

1.	APRESENTAÇÃO

    O presente trabalho é realizado como requisito parcial de nota na disciplina de processamento de imagens, no curso de graduação em Ciências da Computação, consistindo em relatório de desenvolvimento de aplicação de processamento de imagens digitais com interface gráfica para usuário em linguagem JAVA. A aplicação tem o escopo a construção e aplicação dos filtros de seleção de coloração por banda, de aumento de tonalidade por banda do sistema RGB, de conversão para escala de cinza pela média de valores RGB e por seleção de banda, de aplicação de limiar, de conversão para escala negativa pelo sistema RGB e YIQ, manipulação aditiva de brilho por RGB e YIQ, e manipulação multiplicativa de brilho por RGB e YIQ.

2.	DESCRIÇÃO DE ATIVIDADES

    As atividades abrangeram: a criação dos respectivos métodos para cada filtro, separados, a priori, em duas classes: uma para os filtros do sistema RGB, e outra para os filtros do sistema YIQ; a criação de interface gráfica para o usuário; e, a elaboração de relatório de desenvolvimento de software.

3.	ANÁLISE DE RESULTADOS

    3.1.	Estrutura do código
    
    A estrutura do código divide-se em três classes principais e uma auxiliar. As classes principais são: a de interface de usuário, responsável pela manipulação dos componentes e layouts da aplicação; a de filtros RGB, responsável pelos métodos de aplicação de filtros de escala de cinza, negativa, seleção e aumento de tonalidade, manipulação de brilho e limiarização de imagens; e, a de filtros YIQ, que compreende os métodos de conversão de sistema RGB para YIQ, e também o de YIQ para RGB; além dos filtros de manipulação aditiva e multiplicativa de brilho, e ainda escala negativa para o modelo.

    Uma classe auxiliar ‘form’ é gerada pela IDE netbeans para facilitar o desenvolvimento das interfaces gráficas. Foi utilizada também a ferramenta intelliJ IDEA para desenvolvimento das classes “FiltroRGB” e “FiltroYIQ”, sendo estas desenvolvidas com utilização dos pacotes: io.File, awt.*, awt.image.BufferedImage, javax.swing.*, javax.imageio.ImageIO.
    
    De modo geral, cada método utiliza uma imagem de arquivo fornecida pelo usuário, e realiza a manipulação (aplicação do filtro) a partir de uma BufferedImage e da análise pixel a pixel da imagem, retornando, então, uma nova imagem já com o efeito desejado. Para manipulação das imagens pelo sistema YIQ é necessária a conversão a partir do sistema RGB (método rgb2YIQ), que acaba gerando uma matriz de cores no sistema YIQ para cada um dos pixels da imagem. Tal matriz é utilizada para alterações dos componentes de luminância, matiz e saturação do sistema. Na aplicação é manipulado apenas o brilho das imagens a partir do componente ‘Y’. Posteriormente, é feita nova conversão para retornar ao sistema RGB e exibir a imagem alterada.
    
    O layout da interface gráfica utiliza um painel de abas (tabbedPane), com cada aba correspondendo a um determinado filtro. Cada painel de aba apresenta um espaço para visualização da imagem original e outro para imagem com filtro aplicado, além de um botão responsável por solicitar do usuário, a partir de uma tela de seleção, a imagem a ser manipulada, e a seguir, aplicar o filtro chamando o método correspondente a partir da classe do respectivo filtro. Componentes específicos para cada filtro foram adicionados de acordo com sua especificidade e necessidade, como spinner, radio button e sliders. 

    3.2.	Desafios encontrados
    
    Os maiores desafios encontrados foram concernentes ao desenvolvimento da interface gráfica e não dos filtros de processamento de imagem da aplicação. A ferramenta utilizada para criação da interface gráfica (APACHE NETBEANS) demanda muitos recursos da máquina, de modo que equipamentos mais antigos ou com menor disponibilidade de recursos de memória e processamento, acabam apresentar travamentos ou lentidão excessiva. Outrossim, há de ser considerada a ausência de material e referências em língua vernácula, o que prejudica também a resolução de problemas e indicações de usos de cada componente do layout da ferramenta; bem como a superação do escopo do tema avaliado.

4.	TRABALHOS FUTUROS

    Sugere-se a incrementação da interface gráfica para abranger um método de salvamento das imagens geradas a partir de um botão próprio ou de caixa de diálogo exibida ao usuário após a pré-visualização. Também, a melhoria da interface para que seja fornecida a imagem uma vez e todas as pré-visualizações sejam geradas nas respectivas abas automaticamente. Por fim, melhoria dos paneis de visualização das imagens de modo a manter a proporção de formato da imagem, bem como a inclusão de recursos de detalhamento, como zoom.

5.	REFERÊNCIAS

    APACHE NETBEANS. Java GUI Applications Learning Trail. Disponível em: <https://netbeans.apache.org/kb/docs/matisse.htm >. Acesso em 24/04/22.

    ORACLE. Class BufferedImage. Documentação da linguagem Java. Disponível em: <https://docs.oracle.com/javase/7/docs/api/java/awt/image/BufferedImage.html>. Acesso em 24/04/22.

    TUTORIALS POINT. Java Digital Image Processing Tutorial. Disponível em: <https://www.tutorialspoint.com/java_dip/index.htm>. Acesso em 24/04/2022.

    Anotações de material desenvolvido em sala de aula.
