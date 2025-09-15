# Detecção em imagens com a rede YOLO

O projeto teve como objetivo a detecção de objetos em imagens utilizando a rede YOLO (*You Only Look Once*), uma das arquiteturas mais eficientes para tarefas de visão computacional em tempo real. O foco principal foi aplicar o treinamento da rede YOLO sobre imagens já rotuladas, de forma a gerar um modelo capaz de identificar e localizar múltiplas classes de objetos em imagens novas.

Para fins de prototipagem e considerando as limitações de memória e processamento do Google Colab, foi utilizado apenas o conjunto de validação do COCO 2017 (val2017.zip), contendo aproximadamente 5.000 imagens. Apesar de não abranger todo o dataset, esse subset permitiu demonstrar a viabilidade do treinamento, geração de arquivos de labels no formato YOLO, e avaliação do modelo utilizando métricas padrão como precision, recall e mAP.

O workflow do projeto incluiu:

- Preparação do dataset: download das imagens e anotações, conversão das labels do formato COCO para YOLO, e criação de um split de treino, validação e teste.

- Treinamento do modelo YOLO: configuração de hiperparâmetros (tamanho da imagem, batch size, número de épocas) e salvamento dos pesos (best.pt e last.pt).

- Validação e avaliação: cálculo de métricas de desempenho e visualização de bounding boxes em imagens de teste.
