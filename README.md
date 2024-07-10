# Monitoramento de Tanques de Combustível na UnB

Este projeto visa monitorar tanques de combustível dentro da Universidade de Brasília utilizando sensores ultrassônicos e comunicação LoRa. A seguir, uma descrição detalhada do funcionamento e dos componentes do sistema.

## Descrição do Projeto

O projeto utiliza um sensor ultrassom HC-SR04 acoplado a um Arduino Uno com um LoRa shield. Este sensor mede a distância do nível do combustível no tanque. Os dados lidos pelo sensor são transmitidos via rádio frequência para outro Arduino Uno com LoRa shield, que atua como receptor.

O Arduino receptor realiza uma requisição POST a uma API, enviando a distância lida pelo sensor. A API, por sua vez, recebe os dados e os armazena em um banco de dados SQLite.

Uma interface web frontend realiza requisições GET à API para obter os dados e exibi-los em um dashboard, apresentando gráficos e estatísticas sobre o nível dos tanques de combustível.

## Pré-requisitos

- [Python 3.10+](https://www.python.org/downloads/)
- [pip](https://pip.pypa.io/en/stable/installation/)

## Instalação

### Passo 1: Crie e Ative o Ambiente Virtual

```bash
python3 -m venv .venv
source .venv/bin/activate
```

### Passo 2: Instale as Dependências

```bash
pip install -r requirements.txt
```

### Passo 3: Inicialize o servidor

```bash
cd backend
python meu_site.py
```




