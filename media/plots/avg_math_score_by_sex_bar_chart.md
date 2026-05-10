
library(ggplot2)
library(plotly)
library(dplyr)
library(htmlwidgets)

p2 <- bigclass %>%
  group_by(sex) %>%
  summarise(avg_math = mean(Math)) %>%
  ggplot(aes(x = sex, y = avg_math, fill = sex)) +
  geom_col() +
  scale_fill_manual(values = c("M" = "#0072B2", "F" = "#D55E00")) +
  labs(
    title = "Average Math Score by Sex",
    x = "Sex",
    y = "Average Math Score"
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

# p2_plotly <- ggplotly(p2)
# saveWidget(p2_plotly, file = "media/plots/avg_math_score_by_sex_bar_chart.html", selfcontained = TRUE)

