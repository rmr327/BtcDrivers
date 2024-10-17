# Overview
In this exercise, our goal is to utilize a Random Forest model to forecast directional changes in Bitcoin prices (will the price tomorrow go up or down). We will employ explainable AI methods to gain insights: both local (ICE plots) and global (PDP & ALE plots) explanations will be explored for our model. Our objective is to understand how each feature in our final model impacts Bitcoin price movements for the next day. To enhance the accuracy of our model during training, we opted to use the 15-day moving average price (15DAR) as the response variable rather than the raw closing price. Previous findings from our project demonstrate that 15DAR effectively predicts Bitcoin price movements.

# Sample ICE & PDP Plot (Prone to multicollinearity issues)

![image](https://github.com/user-attachments/assets/5d42d07f-4bbf-4c6b-b649-dc30e625ce11)

> RSI: Based on the PDP and ICE plots, there appears to be a correlation where as RSI rises, the price of Bitcoin also tends to increase. However, this presents a problem since RSI traditionally signals overbought and oversold conditions for assets. Ideally, one would anticipate RSI to exert both positive and negative influences on the Bitcoin price.

# Sample ALE Plot (Better for datasets with multicollinearity issues)

![image](https://github.com/user-attachments/assets/1f268ee5-7db3-4141-ba60-bcff7acd10cf)

>RSI: The ALE plot indicates that the model's Bitcoin price prediction is negatively affected by lower RSI values, whereas higher RSI values positively impact it. Low RSI values indicate oversold conditions, while high values indicate overbought conditions. Our findings suggest that in oversold markets, prices tend to decline further the next day, while the opposite is true for higher RSI values.


# References

https://github.com/nogibjj/Flamingo-ML

https://github.com/AIPI-590-XAI/Duke-AI-XAI/tree/main/explainable-ml-example-notebooks

I used ChatGPT 3.5 to rephrase some text.

I used google gemini for code complettion.

> Check out the google colab notebook for the full demo!!
