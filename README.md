# AVR
Repositório dedicado ao armazenamento de projetos utilizando microcontroladores AVR

# Índice:

# Placas:

# Fuses - Objetivo e configurações:
## Low Fuse (LFUSE)
| Pino | Nome                 | Funções                                                                                                    |
| ---- | -------------------- | ---------------------------------------------------------------------------------------------------------- |
| 7    | CKDIV8               | Habilita a divisão do clock por 8.                                                                         |
| 6    | CKOUT                | Habilita a interface JTAG. Se não estiver usando JTAG, pode desativar para liberar os pinos PC2 a PC5.     |
| 5..4 | SUT1, SUT0           | Define o tempo de inicialização do oscilador. Para estabilidade com cristal, usar 01.                      |
| 3..0 | CKSEL3..0            | Seleciona o tipo de clock. Para cristal externo acima de 8MHz, usar 1111.                                  |

## High Fuse (HFUSE)
| Pino | Nome                 | Funções                                                                                                    |
| ---- | -------------------- | ---------------------------------------------------------------------------------------------------------- |
| 7    | OCDEN                | Habilita o Debug por OCD (On-Chip Debug). Se ativado, pode interferir na execução normal.                  |
| 6    | JTAGEN               | Habilita a interface JTAG. Se não estiver usando JTAG, pode desativar para liberar os pinos PC2 a PC5.     |
| 5    | SPIEN                | Habilita a programação via SPI.                                                                            |
| 4    | WDTON                | Habilita o funcionamento do Watchdog Timer (WDT)                                                           |
| 3    | EESAVE               | Se ativado, preserva a EEPROM após um "chip erase".                                                        |
| 2..1 | BODLEVEL2, BODLEVEL1 | Configura o Brown-Out Detection (BOD), que impede que o microcontrolador funcione com tensões muito baixas.|
| 0    | BOOTRST              | Se ativado, o microcontrolador inicia a execução na seção de boot.                                         |
