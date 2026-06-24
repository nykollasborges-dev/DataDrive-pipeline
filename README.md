
Este repositório contém o código-fonte desenvolvido para o processamento, extração e caracterização de redes complexas, focado na transformação de dados brutos de topologia da internet em infraestruturas de fibra óptica preparadas para modelagem de comunicação quântica.

O pipeline está dividido em três Jupyter Notebooks sequenciais:

1. **01_etl_extracao_caida.ipynb (Fase 1):** Processamento em fluxo e *chunking* dos dados brutos do CAIDA ITDK. Realiza a limpeza de memória, sanitização via Regex e filtragem intra-continental, contornando limitações de RAM.
2. **02_modelagem_fisica_quantica.ipynb (Fase 2):** Validação geoespacial (fórmula de Haversine) e construção estocástica da rede fotônica baseada em parâmetros de atenuação de fibra de sílica.
3. **03_caracterizacao_topologica.ipynb (Fase 3):** Benchmarking estrutural comparando as redes reais com modelos sintéticos (Brito-Rozenfeld, Brito-Soares e homogeneos) através de métricas de centralidade, assortatividade e leis de potência.

Para executar os notebooks, recomenda-se um ambiente com pelo menos 12 GB de RAM. As principais bibliotecas utilizadas são:
* `networkx`
* `pandas`
* `geopy`
* `cartopy`
* `matplotlib` e `scipy`
Os dados brutos utilizados como *input* da Fase 1 pertencem ao projeto [CAIDA ITDK](https://www.caida.org/catalog/datasets/internet-topology-data-kit/). Devido à alta dimensionalidade (~40 GB), os arquivos originais `.nodes.geo` e `.links` não estão inclusos neste repositório.