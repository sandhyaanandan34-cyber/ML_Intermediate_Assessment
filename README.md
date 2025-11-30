# ML_Intermediate_Assessment
Intermediate Assessment -  Chinese Automobile Market

<h3>Overview</h3>

You are required to model the price of cars with the available independent variables. It
will be used by the management to understand how exactly the prices vary with the independent
variables. They can accordingly manipulate the design of the cars, the business strategy, etc., to meet
certain price levels. Further, the model will be a good way for the management to understand the pricing
dynamics of a new market.

<h3>Modals Used:</h3>

- Linear Regression
- Decision Tree Regressor
- Random Forest Regressor
- Gradient Boosting Regressor
- Support Vector Regressor

<h3>Insghts Learned from Modals</h3>

- Linear Regression struggles because car price relationships are not purely linear.
- Decision Tree overfits easily, leading to lower generalization.
- SVR requires careful kernel tuning and scaling; with default settings, it underperforms.
- Gradient Boosting is strong but slightly less stable than Random Forest in this dataset.
- Random Forest balances bias and variance, making it the most reliable predictor of car prices.

Best Performing Model
  - Random Forest Regressor usually comes out on top:
  - Highest R² (~0.95) → explains the largest proportion of variance in car prices.
  - Lowest MSE and MAE → smallest average prediction errors, both squared and absolute.

Why it’s best:
  - Combines multiple decision trees (ensemble learning), reducing overfitting compared to a single tree.
  - Captures non‑linear relationships between features (engine size, horsepower, curb weight, etc.) and price.
  - Robust to noise and categorical encodings, which are abundant in this dataset.
Best Performer

Gradient Boosting is the best performer
  - Highest R² (0.94) → explains ~94% of variance in car prices.
  - Lowest MSE (0.077) → smallest squared error, meaning predictions are closest to actual values.
  - MAE is slightly higher than Random Forest, but still competitive.
  - This shows Gradient Boosting balances bias and variance extremely well.

Random Forest is a close second
  - Very strong R² (0.92) and lowest MAE (0.185).
  - More robust and less sensitive to hyperparameters compared to Gradient Boosting.
  - If interpretability and stability are priorities, Random Forest is a safer choice.


<h3>Significant Variables</h3>

From correlation analysis, Random Forest feature importance, and Gradient Boosting results, the following variables consistently emerge as most predictive:
- Engine size → Strongest predictor; larger engines directly increase price.
- Horsepower → Closely tied to performance and cost.
- Curb weight → Heavier cars (luxury builds) are more expensive.
- Car width → Wider cars often signal premium design.
- Car length → Longer sedans and luxury cars tend to cost more.
- Car brand → Luxury brands (BMW, Jaguar, Porsche, Audi) command higher prices regardless of specs.
- Drive wheel (rwd vs fwd vs 4wd) → Rear‑wheel drive cars are typically higher‑end.
- Aspiration (turbo vs std) → Turbocharged engines add cost.
- Fuel system / Engine type → Advanced systems (mpfi, dohc) correlate with higher prices.


<h3>How Well They Describe Price</h3>

- Top numeric variables (engine size, horsepower, curb weight, car width) show strong correlations with price (R² > 0.7 individually).
- Brand and drive wheel add categorical explanatory power — they capture market positioning and engineering choices.
- When combined in ensemble models (Random Forest, Gradient Boosting), these variables explain over 93% of the variance in car prices (R² ~ 0.94).

