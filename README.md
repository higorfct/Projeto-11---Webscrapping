# Projeto 11 - Webscrapping


🌍 **Foco do projeto:**

O script faz web scraping diretamente da Wikipédia, na página
“Lista de países por riqueza total”. Ele busca uma tabela HTML
específica (com style text-align: right) e extrai os dados.

🔧 **Funcionamento da coleta:**

Usa BeautifulSoup para parsear o conteúdo HTML.
Procura dentro do <tbody> da tabela as linhas <tr>.
Em cada linha, coleta as células <td>, limpa caracteres
como o espaço especial '\xa0' e organiza os valores.

🚨 **Tratamento de exceções:**

O código verifica se a tabela foi encontrada. Caso contrário,
lança uma Exception (“Table não encontrada” ou “Corpo da tabela não encontrado”).
Isso garante robustez caso o layout da página mude.

📋 **Organização dos dados:**

Para cada linha da tabela, o script cria uma lista temporária,
acumula os valores e depois constrói uma lista geral de países
e suas respectivas métricas econômicas.

📊 **Utilização do pandas:**

Os dados extraídos são transformados em um DataFrame,
permitindo manipulação tabular, exportação e análises
posteriores de forma simples e eficiente.

📈 **Visualização e Insights:**

O script utiliza matplotlib para gerar gráficos a partir dos dados obtidos.
Foi criado um gráfico que permite observar de forma clara:
- Arábia Saudita, Grécia e Polônia são os 3 maiores do ranking, apresentando níveis de riqueza total bastante semelhantes.

- Logo atrás vêm Israel, Portugal e Chile, ainda com valores elevados, mas já mostrando leve declínio em relação aos primeiros.

- Países como Irlanda, África do Sul e Finlândia aparecem no grupo intermediário, mantendo uma certa relevância econômica.

- Mais ao final, observa-se queda acentuada com Peru, Paquistão, Argentina e Romênia, evidenciando disparidades significativas na distribuição de riqueza.

- O gráfico revela claramente essa transição gradual e destaca a diversidade geográfica entre os 20 países listados.

   <img width="1525" height="650" alt="Captura de tela 2025-07-15 094801" src="https://github.com/user-attachments/assets/d6dcc2fc-95ef-447f-bc44-0e38713a5d3b" />


💡 **Principais aprendizados deste projeto:**

- A extração direcionada (por estilo ou estrutura) aumenta a precisão.
- O pré-processamento de texto é indispensável para limpar dados HTML.
- Tratar exceções durante a coleta evita falhas silenciosas.
- Usar pandas para organizar dados facilita análises e gráficos.
- A geração de gráficos potencializa a interpretação, evidenciando padrões e extremos de forma imediata.
- Mesmo dados públicos da web exigem verificação constante, pois mudanças na página podem quebrar a pipeline.

🚀 **Conclusão:**

Este projeto exemplifica uma pipeline robusta:
1) Leitura do site.
2) Localização e parsing da tabela.
3) Limpeza e estruturação dos dados.
4) Exportação e possibilidade de visualização gráfica.
Resultado: uma base confiável sobre países e sua riqueza total, pronta para análises e visualizações futuras.

