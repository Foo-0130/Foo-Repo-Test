
library(ggplot2)
library(plotly)
library(htmlwidgets)

p_temp_hist <- ggplot(X008, aes(x = Temperature)) +
  geom_histogram(binwidth = 1, fill = "#0072B2", color = "white") +
  labs(
    title = "Distribution of Temperature (X008 Dataset)",
    x = "Temperature",
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

# p_temp_hist_plotly <- ggplotly(p_temp_hist)
# saveWidget(p_temp_hist_plotly, file = "media/plots/X008_temperature_histogram.html", selfcontained = TRUE)

