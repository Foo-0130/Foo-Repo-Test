
library(ggplot2)
library(plotly)
library(htmlwidgets)

p3 <- ggplot(bigclass, aes(x = sex, y = weight, fill = sex)) +
  geom_boxplot() +
  scale_fill_manual(values = c("M" = "#0072B2", "F" = "#D55E00")) +
  labs(
    title = "Weight Distribution by Sex",
    x = "Sex",
    y = "Weight"
  ) +
  theme_minimal() +
  theme(
    axis.title.x = element_text(size = 18),
    axis.title.y = element_text(size = 18),
    axis.text.x = element_text(size = 14),
    axis.text.y = element_text(size = 14),
    plot.background = element_rect(fill = "white", color = NA),
    legend.position = "none"
  )

# p3_plotly <- ggplotly(p3)
# saveWidget(p3_plotly, file = "media/plots/weight_distribution_by_sex_boxplot.html", selfcontained = TRUE)

