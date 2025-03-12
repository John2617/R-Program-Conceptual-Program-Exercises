library(ggplot2)

# Sample data
x <- c(1, 2, 3, 4, 5)
y <- c(2, 5, 3, 8, 7)

# Fit linear regression model
model <- lm(y ~ x)

# Extract residuals
residuals <- resid(model)

# Plot residuals vs fitted values
ggplot(data.frame(Fitted = fitted(model), Residuals = residuals), aes(x = Fitted, y = Residuals)) +
  geom_point() +
  geom_hline(yintercept = 0, linetype = "dashed", color = "red") +
  labs(title = "Residuals vs Fitted Values", x = "Fitted Values", y = "Residuals")

# Shapiro-Wilk normality test on residuals
shapiro_test <- shapiro.test(residuals)

# Q-Q plot of residuals
qqnorm(residuals)
qqline(residuals)
