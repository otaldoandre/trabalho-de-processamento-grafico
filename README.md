# Trabalho de Processamento Gráfico - PP1

Projeto desenvolvido para a disciplina de **Processamento Gráfico** da UFSCar utilizando **Three.js**, **WebGL** e **GLSL Shaders**.

O projeto consiste em uma cena 3D interativa representando um sistema solar estilizado dentro de um globo de neve, integrado a um ambiente 3D completo com objetos, shaders personalizados, partículas e duas câmeras.

---

# Visão Geral

A aplicação renderiza uma cena 3D composta por:

- Sol procedural com shader próprio
- Planetas texturizados e animados
- Foguete com partículas e chama dinâmica
- Estrela cadente animada
- Ambiente interno 3D detalhado
- Globo de neve envolvendo a cena
- Textura em vídeo
- Sistema de duas câmeras
- Efeitos visuais utilizando GLSL

---

# Tecnologias Utilizadas

- JavaScript
- Three.js
- WebGL
- GLSL
- GLTFLoader
- DRACOLoader
- OrbitControls

---

# Funcionalidades Implementadas

## Objetos 3D Individuais
Cada integrante desenvolveu objetos da cena:

- Sol
- Mercúrio
- Vênus
- Terra
- Globo de neve
- Foguete
- Ambiente 3D
- Pequeno Príncipe

Todos os objetos possuem:
- posicionamento próprio
- escala individual
- transformações independentes

---

## Shader Personalizado

Foi implementado um shader próprio utilizando `RawShaderMaterial` para o Sol.

### Recursos do shader:
- Ruído procedural (FBM)
- Fresnel Glow
- Corona dinâmica
- Halo externo animado
- Animação baseada em tempo

Shaders utilizados:
- Vertex Shader
- Fragment Shader

---

## Movimento e Animações

O projeto possui diversas animações em tempo real:

### Planetas
- Rotação própria
- Movimento orbital

### Foguete
- Chama procedural
- Partículas animadas

### Estrela Cadente
- Movimento automático
- Reposicionamento aleatório

### Sol
- Pulsação da corona
- Glow animado

---

# Interação

## Controles

| Ação | Função |
|---|---|
| Mouse | Rotacionar câmera |
| Scroll | Zoom |
| Tecla C | Alternar câmeras |

---

# Câmeras

O projeto possui duas câmeras:

### Câmera Principal
Visualização próxima do sistema solar.

### Câmera Secundária
Visualização ampla do ambiente completo.

---

# Texturização

Texturas aplicadas em:

- Sol
- Terra (Phong material)
- Mercúrio Phong material)
- Vênus Phong material)
- Skybox
- Ambiente interno
- Nuvem cósmica
- Globo de neve

Também foi utilizada:
- `THREE.VideoTexture` para renderização de vídeo em uma tela do ambiente.

---

# Funcionalidades Extras

## Foguete Procedural
Modelo criado inteiramente por código utilizando geometrias primitivas.

## Estrela Cadente
Sistema animado com brilho e transparência.

## Ambiente Completo
O ambiente do quarto utilizado no projeto foi baseado no repositório:

- https://github.com/andrewwoan/sooahs-room-folio

Foram realizadas modificações e adaptações para integração com a cena principal, incluindo:
- alteração de texturas
- integração com o sistema solar
- ajustes de posicionamento e escala
- integração com iluminação e renderização da cena

## Globo de Neve
Sistema solar encapsulado em um modelo 3D de globo de neve.

---

# Conceitos de Computação Gráfica Aplicados

- Pipeline gráfico
- Renderização 3D
- Vertex Shader
- Fragment Shader
- Texturização
- Mapeamento UV
- Skybox
- Blending
- Transparência
- Partículas
- Modelos GLTF
- Animação procedural
- Controles de câmera

---

# Como Executar

## 1. Clone o repositório

```bash
git clone https://github.com/otaldoandre/trabalho-de-processamento-grafico.git
```

---

## 2. Entre na pasta do projeto

```bash
cd trabalho-de-processamento-grafico
```

---

## 3. Execute um servidor local

### Usando VSCode + Live Server

ou:

```bash
npx serve .
```

ou:

```bash
python -m http.server
```

---

## 4. Abra no navegador

```txt
http://localhost:3000
```

> Não abra o arquivo `index.html` diretamente no navegador, pois as texturas e modelos podem não carregar corretamente.
