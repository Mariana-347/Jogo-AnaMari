Pascal nas Alturas:
Jogo de plataforma com Pygame. Controle Pascal, pule entre plataformas e colete sóis enquanto sobe até a porta de uma torre e, depois, até uma lanterna dourada.

Objetivo:
O jogo possui duas fases:
1. Torre: suba pelos matinhos até tocar a área da porta da torre.
2. Céu: pule sobre as lanternas flutuantes até encostar na lanterna dourada e vencer o jogo.
Ao concluir a primeira fase, pressione ENTER para continuar. A pontuação acumulada é mantida na segunda fase. Se Pascal atingir o limite inferior da tela sem escudo, a partida termina.

Controles:
Seta para a esquerda: Mover para a esquerda
Seta para a direita:	Mover para a direita
Espaço ou seta para cima:	Pular quando estiver apoiado
ENTER:	Iniciar, avançar de fase ou reiniciar após vitória ou derrota
ESC:	Encerrar o jogo

Plataformas e itens
- Plataformas normais: servem de apoio para os pulos.
- Plataformas azuis: movimentam-se na horizontal e transportam Pascal quando ele está apoiado.
- Plataformas alaranjadas: desaparecem após o pouso.
- Sóis: cada coleta vale 10 pontos.
- Escudo azul: protege de uma queda.
- Estrela amarela: aumenta a força dos pulos.
O espaço entre as plataformas aumenta conforme o avanço da fase.

Imagens necessárias:
- Torre dourada entre florestas e cachoeiras.png: Fundo da primeira fase
- Castelo sob lanternas no céu noturno.png: Fundo da segunda fase
- matinho p jogo.png:	Plataformas da primeira fase
- luz flutuante.png:	Plataformas da segunda fase
- pascal.png:	Personagem
- sol.png:	Item de pontuação
- lanterna_dourada.png:	Objetivo final

Os efeitos sonoros e os desenhos do escudo e da estrela são gerados pelo próprio código. Não são necessários arquivos de áudio separados.

Pontuação e recorde:
- A pontuação aumenta com a coleta de sóis e continua entre as duas fases. 
- O recorde começa em zero sempre que o jogo é aberto, mas permanece entre partidas reiniciadas com ENTER enquanto o programa estiver aberto.

Recursos:
- Tela inicial com instruções.
- Duas fases com cenários e objetivos próprios.
- Plataformas normais, móveis e frágeis.
- Itens de escudo e superpulo.
- Barra de progresso da subida.
- Animações do personagem e de chegada aos objetivos.
- Efeitos sonoros de pulo, coleta, derrota e vitória.
- Telas de conclusão de fase, vitória e derrota.
- Reinício da partida sem fechar o programa.

Referências e créditos de IA:
Referência de programação: Foi utilizado como referência o repositório pygame-snippets (https://github.com/Insper/pygame-snippets). Ele apresenta exemplos de sprites, movimento, pulo, colisão com plataformas, fundos em movimento, animações e múltiplas telas, especialmente nos arquivos:
- jump/jogo.py: movimento, gravidade e pulo.
- jump_platform.py: plataformas que permitem a passagem durante a subida e sustentam o personagem na descida.
- moving_background.py e moving_background_fixed_player.py: deslocamento do fundo e dos objetos do cenário.
- spritesheet.py: animação de personagens com sprite sheets.
- multiple_screens.py, text_animation.py e text_menu.py: organização de telas, textos e interação pelo teclado.

Uso de inteligência artificial: O ChatGPT foi utilizado como apoio na implementação dos recursos abaixo:
- criar_som(), tocar_som() e sons: Síntese dos efeitos sonoros com ondas senoidais; math.sin e array, incluindo tratamento para áudio indisponível. O repositório inicializa o mixer, mas não apresenta exemplo de síntese de sons.
- ItemEspecial e efeitos em jogar_fase():	Sistema de poderes: escudo que protege contra uma queda e superpulo com duração limitada.
- Colisão com o objetivo em jogar_fase():	Detecção de contato com a porta e a lanterna por máscaras de pixels, usando pygame.mask, em vez das colisões por retângulos dos exemplos.
- Cálculo e desenho da barra em jogar_fase():	Medição do progresso até o objetivo e preenchimento de uma barra com a porcentagem da subida.

Drive com vídeo do jogo e imagens:
- https://drive.google.com/drive/folders/1cpTDej7p9l2sgAPhxuQJJRuKq-s6PyYx 
