
# Análise de Bibliotecas de AES-256 e  Hash (SHA-256) em Python

## Método Utilizado

Para investigar as capacidades das bibliotecas SHA-256 e AES-256 em Python, realizamos 10 experimentos, com cada tecnologia sendo objeto de 5 deles. A hashlib foi empregada na criação de hashes SHA-256, e a pycryptodome foi usada para as operações de criptografia e descriptografia com AES-256.

Nos experimentos relacionados ao SHA-256, produzimos hashes para diversos tipos de conteúdo. Já nos testes com AES-256, o foco foi na encriptação e na subsequente decriptação desses mesmos conteúdos, com o objetivo de verificar a preservação da integridade e a eficiência do processo de criptografia.

## Resultados Obtidos

### AES-256 Criptografia e Descriptografia

Devido às características da criptografia AES, o resultado da encriptação é apresentado em forma de bytes, o que torna o texto criptografado ilegível diretamente. Portanto, a tabela concentra-se na comparação entre o texto original e o texto após descriptografia para assegurar a verificação da integridade.

| Entrada                                    | Texto Descriptografado                          |
|--------------------------------------------|-------------------------------------------------|
| texto simples                              | texto simples                                   |
| @#$%&*()_+=-\`~                            | @#$%&*()_+=-\`~                                 |
| A quick brown fox jumps over the lazy dog  | A quick brown fox jumps over the lazy dog       |
| 123456789                                  | 123456789                                       |
| texto simples (com espaço no final)        | texto simples                                   |


### SHA-256 Hashes

| Entrada                                    | Hash SHA-256                                                               |
|--------------------------------------------|----------------------------------------------------------------------------|
| texto simples                              | `a7bdbfb84f5369243bd0e7494947db69216ed9161d39f2522214b866bd5e1d95` |
| @#$%&*()_+=-\`~                            | `c5f19e10d4812336b8f2569a69a13d5681739385595fb5a8b1309fdd5418a35f` |
| A quick brown fox jumps over the lazy dog  | `afd63d45baadf7eaf2e9b861054f7b435ae5200d46bf4e145468dc38d1e110d7` |
| 123456789                                  | `15e2b0d3c33891ebb0f1ef609ec419420c20e320ce94c65fbc8c3312448eb225` |
| texto simples (com espaço no final)        | `e457845ed1be331a523d60b2c08afacfa1cb99b20195f0b908a673483d552c82` |

## Comparação entre AES-256 e SHA-256

Aplicações e Funcionalidades: O SHA-256 é empregado para assegurar a integridade de dados, criando um hash exclusivo para diferentes conjuntos de informações. Por outro lado, o AES-256 é aplicado na cifração e decifração de dados, promovendo a segurança na transferência e no armazenamento de dados.

Reação a Mudanças: O SHA-256 responde sensivelmente a alterações nos dados, onde variações mínimas resultam em hashes significativamente distintos. De forma similar, o AES-256 assegura que os dados decifrados sejam exatamente os mesmos que os originais, evidenciando sua elevada sensibilidade e integridade.

Desempenho: Ambas as tecnologias são eficazes, no entanto, o AES-256 pode apresentar uma performance ligeiramente inferior devido aos procedimentos de cifração e decifração, enquanto o SHA-256 produz um hash diretamente a partir dos dados fornecidos.

Proteção de Dados: O AES-256 é uma solução sólida para a salvaguarda de informações sensíveis, facilitando a recuperação dos dados originais por meio da decifração. Embora o SHA-256 não possibilite a recuperação dos dados a partir do hash, é crucial para a verificação da integridade e para identificar quaisquer modificações nos dados.

Em resumo, o SHA-256 e o AES-256 cumprem funções distintas na segurança digital, com o primeiro focado na preservação da integridade dos dados e o segundo na manutenção da confidencialidade. A escolha entre eles depende das necessidades específicas de segurança.

