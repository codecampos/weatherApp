# 🌦️ Weather App

Aplicação web simples de previsão do tempo. Digite o nome de uma cidade e veja a temperatura atual, a umidade e a velocidade do vento, com um ícone que representa a condição climática.

Projeto desenvolvido para estudo de **HTML, CSS e JavaScript puro**, consumindo a API do [OpenWeatherMap](https://openweathermap.org/api).

## ✨ Funcionalidades

- Busca do clima por nome de cidade
- Exibição de temperatura (°C), umidade (%) e velocidade do vento
- Ícone dinâmico conforme a condição (nuvens, céu limpo, chuva, garoa, neve, neblina)
- Mensagens de erro para cidade não encontrada, chave inválida e falha de conexão
- Layout responsivo em formato de card

## 🛠️ Tecnologias

- HTML5
- CSS3
- JavaScript (ES6+), com `fetch` e `async/await`
- [OpenWeatherMap API](https://openweathermap.org/current) (endpoint `weather`)

## 📁 Estrutura do projeto

```
weatherApp/
└── img/            # Ícones (clear, clouds, drizzle, mist, rain, snow, humidity, wind, search)
├── index.html      # Estrutura da página
├── style.css       # Estilos do card, busca e detalhes
```

## 🚀 Como executar

1. Clone o repositório:

   ```bash
   git clone https://github.com/SEU-USUARIO/weatherApp.git
   cd weatherApp
   ```

2. Crie uma conta gratuita no [OpenWeatherMap](https://openweathermap.org/api) e gere sua **API key**.

3. Copie a **API key** e coloque sua chave:

   ```js
   // linha 44
   const apiKey = "SUA_API_KEY_AQUI";
   ```

4. Abra o `index.html` no navegador (ou use a extensão *Live Server* do VS Code).

## 🧭 Como funciona

1. O usuário digita a cidade e clica no botão de busca.
2. A função `checkWeather(city)` (em `script.js`) faz uma requisição à API do OpenWeatherMap com `units=metric`.
3. Se a API retornar `404`, a mensagem de erro é exibida.
4. Caso contrário, os dados (`name`, `main.temp`, `main.humidity`, `wind.speed`) são mostrados no card e o ícone é escolhido com base em `weather[0].main`.
