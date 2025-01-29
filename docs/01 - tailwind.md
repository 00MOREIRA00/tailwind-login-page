# Configurando o Tailwind

Para configurar o Tailwind CSS, siga as instruções abaixo. Estamos utilizando o Tailwind via CLI, sem o uso de frameworks de desenvolvimento de front-end.

## Instalação do Tailwind

Execute o comando abaixo para instalar o Tailwind CSS e a CLI do Tailwind:

```bash
npm install tailwindcss @tailwindcss/cli
```

## Gerando o arquivo de configuração do Tailwind

Crie um arquivo `src/input.css` e adicione a seguinte configuração:

```css
@import "tailwindcss";
```

## Compilando o arquivo Tailwind

Execute o comando abaixo para compilar o arquivo Tailwind:

```bash
npx @tailwindcss/cli -i ./src/input.css -o ./src/output.css --watch
```

> O arquivo compilado será usado como nosso CSS principal. Importe-o nos arquivos `.html`.

## Configurando o arquivo de configuração do Tailwind

Crie um arquivo `tailwind.config.js` com o seguinte conteúdo:

```javascript
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: ["./**/*.{html,js,jsx,ts,tsx}"],
  theme: {
    extend: {},
  },
  plugins: [],
};
```

> Isso garante que todos os arquivos com as extensões `html`, `js`, `jsx`, `ts` e `tsx` sejam lidos pelo Tailwind.

## Por que compilar o arquivo?

A compilação permite personalizar o código gerado, evitando que o framework compile classes que não serão usadas, otimizando o tamanho do arquivo CSS final.

## Bibliotecas do VSCode para ajudar no desenvolvimento

- **Live Server**: Para recarregar automaticamente o navegador ao salvar arquivos.
- **HTML Boilerplate**: Para facilitar a criação de arquivos HTML com estrutura básica.