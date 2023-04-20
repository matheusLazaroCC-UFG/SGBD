18/04/2023
* Arquitetura
    * Armazenamento
        * Velocidade: CPU -> Reg > RAM > SDD > Disco > Rede
        * Localidade espacial na carga de trabalho
            * Controle espacial doa dados
    * Processamento
    * Transações
    *
    20/04
    * Arquitetura centralizada
        * Inicialmente: IDEs
        * IMS - associado a COBOL
        * Flexível, confiável e desempenho
        * Independência de dados
        APP -> SQL -> SGBD -> armazenamento
        * Projetar um SGBD:
            * Encapsulamento
            * Organização hierárquica
                * Camadas (5)
                    * Usuário
                    * C3
                    * C2
                    ...
                    * Hardware
                * Contratos de entrada e saida bem ddfinidos entre as camadas.
                C5
                C4
                C3 - represesntação
                    * compressão de dados
                    * criptografia
                    * índices (estrutura de dados para acessar os dados das páginas)
                C2 - Controle de propagação de dados (disco-memória, memória-disco - buffer / cache) - Controle temporal de dados
                    * páginas
                    * gerenciamento de memória.
                    * Controle temporal
                    * SGBD Postgres: Shape buffer (memória utilizada)
                C1 - Principal: abstração do meio de armazenamento. do hardware: DIsco, ssd, ....
                    * blocos
                    * COntrole espacial de daddaos.
                    * Uso do sistema de arquivos do SO
                        * DIstribuição por frequência de acesso dos dados , nos diferentes hardwares (disco, ssd, RAM, ...) - HOT SPOTS.
                    * Uso direto - RAW 10
                    * Table space
                