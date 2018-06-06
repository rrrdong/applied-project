## Welcome to GitHub Pages

You can use the [editor on GitHub](https://github.com/rrrdong/applied-project/edit/master/README.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown

```{r}
library(HistData)
library(plotly)
library(vcd)
library(magrittr)
data("Arbuthnot")
str(Arbuthnot)
maxR <- max(Arbuthnot$Ratio)

meanR <- mean(Arbuthnot$Ratio)

minR <- min(Arbuthnot$Ratio)

MR <- max(Arbuthnot$Ratio) + 0.1

IR <- min(Arbuthnot$Ratio) - 0.1

plot_ly(Arbuthnot, x = ~Year, y = ~Ratio, name = 'Ratio: Male vs. Female',type = 'scatter', mode = 'lines',line = list(color = 'black', width = 2))%>%
add_trace(y = ~maxR, name = 'Maximum', mode = 'lines',line = list(color = 'red', width = 2)) %>%
add_trace(y = ~meanR, name = 'Mean', mode = 'lines',line = list(color = 'green', width = 2)) %>%
add_trace(y = ~minR, name = 'Minimum', mode = 'lines',line = list(color = 'blue', width = 2))
```


- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/rrrdong/applied-project/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
