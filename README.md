# Servidor All the Mons

Servidor de Minecraft com o modpack **All the Mons 1.3.0** (Cobblemon: Pokémon dentro do Minecraft) para um grupo de amigos, aceitando **Minecraft original e pirata**. Rodando num PC antigo que estava parado no quarto.

**Site com o passo a passo para entrar:** https://joaoppk2.github.io/servidor-all-the-mons/

---

## A ideia
Transformar um computador parado em servidor 24h, administrado à distância, sem gastar nada:
- O PC fica ligado o tempo todo; o Minecraft só roda quando o dono quer.
- Pelo menos 8 jogadores, com e sem conta original.
- Amigos de fora de casa entram por um túnel gratuito, sem abrir portas no roteador.
- Backup diário do mundo em outro computador.
- Um site simples que explica tudo, para ninguém precisar perguntar nada.
- Só ferramentas gratuitas.

## Como entrar
| | |
|---|---|
| **Endereço** | `impairment-sequester.tun.ply.gg` |
| Se ficar preso em "Connecting" | `impairment-sequester.tun.ply.gg:65216` |
| Na mesma casa do servidor | `192.168.237.67:25565` |
| **Modpack** | All the Mons **1.3.0** (tem que ser essa versão) |
| Download do modpack (.zip oficial) | [CurseForge, All the Mons 1.3.0](https://www.curseforge.com/minecraft/modpacks/all-the-mons/files/8822048) |
| Memória para o jogo | 8 GB |
| Minecraft original | entra direto, sem senha |
| Minecraft pirata | `/register senha senha` na primeira vez, depois `/login senha` |

O passo a passo completo, separado para original e pirata, está no [site](https://joaoppk2.github.io/servidor-all-the-mons/).

## O computador do servidor (hardware)
| Peça | Modelo |
|---|---|
| Processador | Intel Core i5-4590 (4 núcleos, 3,3 GHz, 2014) |
| Memória | 16 GB DDR3 |
| Armazenamento | SSD 512 GB |
| Placa de vídeo | NVIDIA GeForce GTX 750 Ti (o servidor não usa) |
| Rede | Cabo, Realtek PCIe Gigabit Ethernet |
| Sistema | Windows 10 Pro 22H2 (mantido no 10 de propósito) |

O processador é o limite: um modpack com ~400 mods e 8 pessoas fica no limite dele. Por isso o mapa foi gerado antes (raio de 3.000 blocos) e as distâncias foram reduzidas.

## O que roda no servidor (software)
| Peça | Versão | Para quê |
|---|---|---|
| Minecraft | 1.21.1 | |
| NeoForge | 21.1.249 | carregador de mods (a mesma versão do pack) |
| All the Mons | 1.3.0 (Server Files oficiais, 375 mods) | o modpack |
| Java | Eclipse Temurin 21 | exigido pelo Minecraft 1.21.1 |
| [Crafty Controller](https://craftycontrol.com) | 4.11 | painel para ligar, desligar e ter vários modpacks |
| [MixAuth](https://modrinth.com/mod/mixauth) | 1.3.3 | login: original entra direto, pirata usa senha |
| [Chunky](https://modrinth.com/plugin/chunky) | 1.4.23 | gerar o mapa antes, para não travar no jogo |
| [playit.gg](https://playit.gg) | 1.0.8 (grátis) | túnel para quem está fora de casa |

Já vêm no pack e ajudam no desempenho: ModernFix, FerriteCore, AllTheLeaks, Clumps e spark.

## Configuração do servidor
| Opção | Valor |
|---|---|
| Memória do servidor | 10 GB (mínimo 6 GB) |
| Distância de visão | 7 chunks |
| Distância de simulação | 5 chunks |
| Jogadores | até 10 |
| Dificuldade | normal |
| Voo | permitido (alguns mods precisam) |
| Whitelist | desligada (o MixAuth protege as contas) |
| Mapa pré-gerado | raio de 3.000 blocos a partir do centro |

## Como foi montado (resumo)
1. **Preparar o PC para ficar ligado:** desligar suspensão, hibernação e inicialização rápida; IP fixo; placa de rede sem economia de energia; travar o Windows Update no Windows 10 e sem drivers automáticos.
2. **Acesso à distância:** Área de Trabalho Remota e SSH (só na rede de casa), para administrar sem ir até o quarto.
3. **Painel e Java:** Crafty Controller rodando com um usuário sem poderes de administrador, ligando junto com o Windows e reiniciando se cair.
4. **Modpack:** Server Files oficiais do All the Mons 1.3.0, com o mesmo NeoForge do pack.
5. **Login para original e pirata:** MixAuth.
6. **Mapa:** pré-geração com o Chunky.
7. **Amigos de fora:** túnel do playit.gg, sem abrir porta no roteador.
8. **Backup:** todo dia às 21h o mundo é copiado para outro computador (mantém os 7 últimos).
9. **Site:** esta página, no GitHub Pages.

## Atualizar o modpack
O botão de download do site aponta para **um arquivo fixo** (a versão 1.3.0). Ele não muda sozinho, de propósito: se mudasse, os jogadores baixariam uma versão diferente da do servidor e ninguém entraria.

Quando sair versão nova, a atualização é feita toda de uma vez: backup do mundo → servidor na versão nova → site (botão e textos) → aviso no grupo para todos atualizarem o pack.

## O que tem neste repositório
| Arquivo | O que é |
|---|---|
| `index.html` | O site (uma página só, sem dependências além das fontes do Google) |
| `video/` | Vídeo de fundo gravado dentro do próprio servidor (versão para PC e para celular) |
| `img/pokemon/` | Sprites dos Pokémon |
| `img/` | Print antigo do servidor (não usado mais) |

## Créditos
- Modpack: [All the Mons](https://www.curseforge.com/minecraft/modpacks/all-the-mons), da ATMTeam.
- Fundo: gravação do próprio servidor.
- Sprites: © Nintendo / Game Freak, via [PokeAPI](https://github.com/PokeAPI/sprites). Página de fã, sem fins lucrativos.
- Fontes: Pixelify Sans, Nunito e VT323 (Google Fonts).
