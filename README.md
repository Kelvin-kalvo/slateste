# Stellar Forge Sandbox

Jogo sandbox espacial desktop inspirado em sandboxes astronômicos, com foco em:

- exploracao livre em um espaco enorme
- criacao de estrelas, planetas, luas e buracos negros
- simulacao gravitacional simplificada com orbitas dinamicas
- progressao idle/clicker baseada em sistemas estaveis
- camera 2.5D com rotacao, zoom, foco e sensacao de profundidade
- save/load local, conquistas e modo sandbox

## Requisitos

- Windows
- Python 3.11+ recomendado

## Como executar

1. Abra um terminal na pasta do projeto.
2. Instale as dependencias:

```powershell
pip install -r requirements.txt
```

3. Rode o jogo:

```powershell
python main.py
```

## Controles

- `WASD`: mover a camera
- `Q / E`: rotacionar camera
- `Scroll`: zoom suave
- `Clique esquerdo`: selecionar objeto e gerar dinheiro por clique
- `F`: focar no objeto selecionado
- `Espaco`: pausar/retomar
- `1 / 2 / 3`: velocidade lenta, normal e rapida
- `Tab`: alternar entre campanha e sandbox livre
- `R`: reiniciar o universo atual
- `Ctrl+S`: salvar
- `Ctrl+L`: carregar

## Loop principal de progressao

- Clicar em corpos gera dinheiro.
- Renda passiva so existe quando um sistema contem:
  - 1 estrela
  - 1 planeta orbitando a estrela
  - 1 lua orbitando o planeta
- Orbitas mais estaveis aumentam a renda.
- Objetivo inicial da campanha: chegar a `1.000.000`.

## Estrutura

- `main.py`: ponto de entrada
- `src/core`: configuracoes, utilitarios, estado e loop principal
- `src/systems`: simulacao, progressao, audio e save/load
- `src/ui`: HUD, botoes e paineis
- `src/content`: presets e geracao inicial

## Observacoes

- O projeto foi construido para ser facil de expandir.
- O audio e procedural, evitando dependencias externas de assets.
- A fisica e simplificada para manter boa performance em mapas grandes.
