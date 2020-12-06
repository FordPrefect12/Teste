## Welcome to GitHub Pages

You can use the [editor on GitHub](https://github.com/FordPrefect12/Teste/edit/main/README.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown

import networkx as nx
import pandas as pd
dfs = pd.read_excel("Twitter.xlsx", sheet_name = ["Elementos", "Perfil", "Conexoes", "Conexoes2"])
node_data = dfs["Elementos"]
edge_data = dfs["Perfil"]
edge_data1 = dfs["Conexoes"]
edge_data2 = dfs["Conexoes2"]

A = nx.from_pandas_edgelist(edge_data, source = 'Perfil1', target = 'Seguindo1')
B = nx.from_pandas_edgelist(edge_data1, source = 'Seguindo', target = 'Recomendado')
C = nx.from_pandas_edgelist(edge_data2, source = 'Recomendado1', target = 'Recomendado2')
U = nx.compose(A, B)
Z = nx.compose(U,C)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/FordPrefect12/Teste/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
