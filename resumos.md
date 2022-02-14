Resumo dos artigos lidos

############################################

## A Survei on LiDar Scanning Mechanisms ##
Mecanismos tipo em LiDar:
  - Opto-mechanical
  - Eletromechanical
  - Micro eletromechanical systems (MEMS)
  - Solid state scanning 
  
ELETROMECHANICAL SCANNING
É a tecnilogia mais promissora.
Solução de conversão 1D para 3D mais atrativa se o "low scanning rate" não for um problema.

MEMS
É a melhor alternativa para aplicações pequenas, leves e de baixo consumo (SWaP)
É a tecnilogia mais matura comparada com solid-state

SOLID-STATE
Preenche o vazio nas aplicações ADAS (Advanced driving assistence systems)
É uma tecnologia permatura nas demonstra grande potência
  - robustez, campo de visão, velocidade de scanning superiores.
  
OPTO-MECHANICAL 1D
Usa espelhos ou prismas para defletir o laser. 
  - Usa um motor para mover o espelho (torna-o 2D)
      - FOV (Field Of View) limitado a 180º 

ELETROMECHANICAL 2D
Com um motor passa a 3D
Dependendo do eixo de rotação pode dar scan até 360º
Podem ser usados servos ou steppers
  - já usaram steppers com anéis para fazerem as ligações
  - conseguiram uma leitura mais fluída
  - tem as suas desvantagens (??)
  
############################################

## Scan Pattern Characterization of Velodyne VLP-16 ##
Lidar sensor para UAS laser scanning
  - Unoccupied aircraft systems (UAS)
  
 Um dos pontos mais cruciais no que diz respeito a fazer-se um mapeamento com Lidar é a DENSIDADE DE PONTOS
 
 O cálculo da densidade de pontos depende de algumas características do sensor
  - Pulse rate
  - Geometria dos pulsos do laser
  
Existem algumas soluções para este tipo de cálculos que envolvem as características do sensor be como as características do voo
  - Altura de voo
  - Velocidade de voo
  - Percent overlap
  
 Outros parametros que são importantes e que devem ser levados em consideração
  - variação da distância dos objetos
  - ângulo de incidência do laser
 Uma altura de voo mais elevada e um "swath width" (??) mais baixo promovem uma baixa variação da distância dos objetos bem como baixas variações no ângulo de incidência.
 
 Velodyne VLP-16 lidar sensor
  - é um dos sensores mais populares no campo de "mapping"
  - é composto por 16 feixes
    - 30º vertical FOV (-15º a +15º)
    
 Conclusões
 Point density é inversamente propocional à altura de voo e à velocidade de voo.
 Existem gaps no mapeamento
  - há uma equação que "prevê" os gaps
    - mesmo assim dependendo das condições esta equação pode não conseguir "detetar" todos os gaps.
    
############################################

## Dense point cloud aquisition with low-cost Velodyne VLP-16 ##
Velodyne VLP-16
  - tem 16 feixes num suporte rotativo
  - cada laser recorda até 1875 pontos a cada 1/10s
    - o que corresponde  a uma resolução horizontal algular de 0,2º para um FOV de 360º
  - a resolução vertical é de apenas 30º
    - implica uma baixa resolução vertical angular de 2º
    
Modelo matemático do VLP-16 que calcula as coordenadas (x,y,z)
(ver caderno ou artigo)

############################################

## On Solving Mirror Reflexion in LiDar Sensing ##
Lidar sensor: - narrow beamwidth
              - fast time of flight
  - Faz com que o lidar seja apropriado para aplicações de precisão no campo da robótica.
 
O Lidar estima a distância medindo o "round-trip time of flight of an emitted pulse of light"
  - Só uma pequena parte dos fotões emitidos é que são refletidos de volta até ao sensor.
  
############################################

## Velodyne VLP-16 Laser Scanner Acceptance ##
Hardware/Software configuration
(ver caderno)

O scanner aproveita-se do Garmin GPS antenna (??) para o timming.
Power and Ethernet communications são feitas atravez de uma interface diferente.
O scanner é controlado usando HYPACK (no PC)

Offsets - não entendo bem como se medem nem para que servem (?????)

HYPACK Software
  - Veloview é um software package qye serve para dar display e capturar data packetes
  - Grava em pcap format
  - Pode ser exportado para xyz e cvs
  - É necessário uma driver para a integração do sensor com o meio de aquisição e processamento da data.
  
A driver do HYPACK permite
  - incluir offsets e patch test values
  - filtros por ângulo de distância
  - logging of data within HSX file format in TOP or RMB message 
  - visualização simultânea do VLP-16 e MBES coverge
  - aquisição e atribuição de pontos como objetos do tipo S57 (??)
  
############################################

## Positioning and perception in LIDAR point clouds ##
Na literatura existem 2 grupos no que diz respeito à percepção de objetos
  - geometria tradicional
  - deep learning
  
É um bom artigo para ter umas noções basicas dos vários métodos que existem para trabalhar a informação recolhida por um LIDAR.
  



  
  
