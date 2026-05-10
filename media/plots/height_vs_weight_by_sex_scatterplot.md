
library(ggplot2)
library(plotly)
library(htmlwidgets)

p4 <- ggplot(bigclass, aes(x = height, y = weight, color = sex)) +
  geom_point(size = 3) +
  scale_color_manual(values = c("M" = "#0072B2", "F" = "#D55E00")) +
  labs(
    title = "Height vs. Weight by Sex",
    x = "Height",
    y = "Weight",
    color = "Sex"
  ) +
  theme_minimal() +
  theme(
    axis.title.x = element_text(size = 18),
    axis.title.y = element_text(size = 18),
    axis.text.x = element_text(size = 14),
    axis.text.y = element_text(size = 14),
    plot.background = element_rect(fill = "white", color = NA)
  )

# p4_plotly <- ggplotly(p4)
# saveWidget(p4_plotly, file = "media/plots/height_vs_weight_by_sex_scatterplot.html", selfcontained = TRUE)

