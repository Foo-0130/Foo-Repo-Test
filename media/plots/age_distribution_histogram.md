
library(ggplot2)
library(plotly)
library(htmlwidgets)

p1 <- ggplot(bigclass, aes(x = age)) +
  geom_histogram(binwidth = 1, fill = "#0072B2", color = "white") +
  labs(
    title = "Distribution of Age",
    x = "Age",
    y = "Frequency"
  ) +
  theme_minimal() +
  theme(
    axis.title.x = element_text(size = 18),
    axis.title.y = element_text(size = 18),
    axis.text.x = element_text(size = 14),
    axis.text.y = element_text(size = 14),
    plot.background = element_rect(fill = "white", color = NA)
  )

p1_plotly <- ggplotly(p1)
# saveWidget(p1_plotly, file = "media/plots/age_distribution_histogram.html", selfcontained = TRUE)

