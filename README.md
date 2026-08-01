# NDJ File Format Specification (.ndj)

> **Dynamic Vector-Raster Hybrid Format for Real-Time Canvas Rendering & Smart Media Streaming.**

O **.ndj** é um formato de arquivo de mídia de alta precisão projetado para redefinir o processamento de imagens e quadros de vídeo. Combinando mapeamento direto de pixels, tabelas de cores chaveadas e indexação por faixas contínuas, o formato elimina perdas por compressores destrutivos convencionais enquanto reduz a pegada de dados e viabiliza injeção dinâmica de conteúdo em tempo de execução.

---

## 🎯 Pilares da Tecnologia .ndj

* **Precision Indexing:** Mapeamento de 100% dos pixels por varredura direta, sem artefatos de compressão lossy ou perda de detalhes em superfícies complexas.
* **Dynamic Selective Rendering (DSR):** Suporte nativo a múltiplos níveis de precisão no mesmo arquivo — ideal para reprodução leve em tempo real com renderização de ultra-definição ao pausar ou focar um quadro.
* **Runtime Asset Layering (Dynamic Insertion):** Estrutura modular por chaves `@cKey` que permite a substituição, modificação e injeção de elementos visuais (como anúncios, marcas e assets regionais) diretamente no player, sem necessidade de re-renderizar o arquivo base.
* **Lightweight & Standalone:** Interpretação direta por scripts no client-side (web browser, players nativos e sistemas embarcados), eliminando dependências de APIs pesadas de terceiros.

---

## 📋 Estrutura de Arquivo (.ndj)

O arquivo `.ndj` é compilado em instruções de canvas, tabelas de cores e sequências de índices de pixels:

```ndj
# NDJ Custom Image Format - Precision Map
CANVAS 740 740
PALETTE_SIZE 2560

@c0 (#F8F8F8): {1..82140}
@c1 (#000000): {499501..547600}
@c2 (#F0F0F0): {82141..96200}
@c3 (#C8C8C8): {150221..167240}


Não, esse sistema não tem uma versão tradicional para terminal Linux ou qualquer outro.
