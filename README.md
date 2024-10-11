# Documentação do Projeto de Aplicativo de Classificação de Resíduos Baseado em Machine Learning

## Visão Geral

O projeto consiste em um aplicativo móvel para Android que utiliza Machine Learning para classificar resíduos a partir de imagens enviadas pelos usuários. O propósito é promover a gestão correta de resíduos recicláveis, ajudando a identificar diferentes tipos de materiais, como plástico, vidro, metal, e papel, e orientando sobre o descarte adequado.

## Objetivo

- Desenvolver um aplicativo que ajude na identificação e classificação de resíduos recicláveis.
- Utilizar técnicas de Machine Learning para análise de imagens e classificação precisa.
- Promover a educação sobre descarte correto de resíduos por meio de um aplicativo de fácil uso.

## Escopo do Projeto

### Funcionalidades da Interface

- **Tela inicial:** Telas simples e intuitiva que introduzem o aplicativo em um pequeno tutorial.
- **Tela principal:** Espaço onde os usuários podem fazer upload de imagens de resíduos.
- **Upload de Imagem:** Função de upload para que os usuários enviem imagens de resíduos.
- **Resultado da Classificação:** Exibição do tipo de resíduo identificado com instruções de descarte.
- **Feedback dos Usuários:** Sistema de avaliação por estrelas e comentários para coleta de feedback.

### Banco de Dados e Armazenamento

- **Banco de Dados Utilizado:** O aplicativo utilizará o **Supabase**, que é uma plataforma de banco de dados PostgreSQL gerenciada. O Supabase oferece funcionalidades em tempo real e autenticação, sendo ideal para o gerenciamento eficiente dos dados do projeto.
- **O que será armazenado:**
  - Feedback e avaliações dos usuários: Feedbacks fornecidos pelos usuários, contendo suas avaliações sobre a precisão da classificação (número de estrelas) e comentários.

### Desenvolvimento do Modelo de Machine Learning

O modelo de machine learning do projeto é baseado em **redes neurais convolucionais (CNNs)**, que são amplamente utilizadas para a classificação de imagens. No caso deste projeto, as CNNs são usadas para identificar e classificar resíduos recicláveis, como plástico, vidro, papel e metal, a partir das imagens fornecidas pelos usuários.

#### [Link para o código no Google Colab](https://colab.research.google.com/drive/1bHeq_2f9EdJ84O1rrmA01jIct_wj5jhA?usp=sharing)
O desenvolvimento e o treinamento do modelo podem ser acessados através do link: [Google Colab - Classificação de Resíduos](https://colab.research.google.com/drive/1bHeq_2f9EdJ84O1rrmA01jIct_wj5jhA?usp=sharing).

Este notebook do Colab contém as seguintes etapas principais:

1. **Pré-processamento dos Dados**: As imagens de resíduos são redimensionadas e normalizadas para garantir que estejam no formato adequado para serem processadas pelo modelo. Técnicas como aumento de dados (_data augmentation_) podem ser aplicadas para expandir o dataset de treinamento.

2. **Arquitetura da Rede Neural Convolucional**: A rede CNN é construída utilizando frameworks como TensorFlow e Keras. Ela consiste em várias camadas convolucionais seguidas de camadas de _pooling_ e camadas totalmente conectadas. Cada camada extrai características importantes da imagem para ajudar na classificação.

3. **Treinamento do Modelo**: O modelo é treinado utilizando um conjunto de dados previamente rotulado, com imagens de diferentes categorias de resíduos. Durante o treinamento, o modelo aprende a reconhecer padrões visuais associados a cada tipo de material.

4. **Avaliação e Métricas**: O desempenho do modelo é avaliado com métricas como **acurácia**, **precisão**, **recall** e **F1-score**, que fornecem uma visão detalhada sobre a eficiência do modelo em classificar corretamente os resíduos.

O Google Colab é uma ferramenta ideal para este tipo de trabalho, pois permite o uso de **GPUs** para acelerar o treinamento do modelo e facilita a colaboração entre desenvolvedores.

### Funcionalidades do Back-end

- **API:** Processamento de imagens e classificação com base no modelo treinado e os feedbacks.

### Hospedagem e Manutenção

- **Publicação na Google Play Store:** O aplicativo será publicado na **Google Play Store** para facilitar o acesso dos usuários. Será submetido para aprovação e disponibilizado para download diretamente pela loja oficial do Android.
- **Back-end e API:** O back-end e a API estão  hospedados no serviço da plataforma **Railway**, garantindo que os serviços de processamento de imagens e classificação, e feedback estejam disponíveis 24/7 para os usuários.

### Segurança e Privacidade

- **Conformidade com Regulamentações:** O aplicativo deve estar em conformidade com LGPD e GDPR.
- **Políticas de Privacidade:** Implementação de políticas de privacidade e termos de uso.

## Design da interface 
O design da Interface do aplicativo foi feito na plataforma Figma:  
Link para o design no [figma](https://www.figma.com/design/798PQZldCQgnwUOiJ0fHTI/BrazRecicla?m=auto&t=62oyYFSBwtPdFNVs-1)

### Segurança e Privacidade

- **Conformidade com Regulamentações:** O aplicativo deve estar em conformidade com a **LGPD** e **GDPR** para garantir que os dados dos usuários sejam tratados de forma segura e legal.
- **Políticas de Privacidade:** Implementação de políticas de privacidade claras e transparentes para informar os usuários sobre como seus dados serão armazenados e utilizados.
- **Segurança de Dados:** O uso de criptografia em trânsito (via HTTPS) e em repouso para proteger os dados dos usuários.

## Arquitetura do Sistema

O sistema é composto por quatro partes principais:

1. **Front-end React Native:** Aplicativo móvel com interface.
2. **Back-end (API):** Implementado com FastAPI para comunicação com o modelo de Machine Learning.
3. **Modelo de Machine Learning:** Treinado com /PyTorch para classificação de resíduos.
4. **Banco de Dados Supabase:** Utilizado para armazenar dados e manter a sincronização em tempo real entre os dispositivos.

## Guia de Uso

1. Abra o aplicativo em um dispositivo Android.
2. Faça o upload de uma imagem do resíduo que deseja classificar.
3. Visualize o resultado da classificação e obtenha instruções de descarte.
4. Forneça feedback sobre a precisão da classificação.

## Licença

Este projeto é licenciado sob a Licença MIT - veja o arquivo [LICENSE](LICENSE) para mais detalhes.

## Contato

Para dúvidas ou mais informações, entre em contato com:

- **Desenvolvedor:** Camilla Soares Sousa
- **E-mail:** [camillasoares818@gmail.com]
