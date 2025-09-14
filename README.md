This project explores how marketing and direct response levers drive revenue over a two-year weekly dataset. The goal is not just to fit numbers, but to answer a real business question: what actually moves revenue, and how can we measure it responsibly?

I built a reproducible pipeline in Python that prepares the data, handles weekly trends and seasonality, and accounts for zero-spend weeks. To respect the causal structure, I modeled Google spend as a mediator between social channels (Facebook, TikTok, Snapchat) and revenue. This two-stage approach first predicts Google from social activity, then predicts revenue from predicted Google plus other levers like price, promotions, email, and SMS.

The model of choice is ElasticNet regression: interpretable, regularized, and robust to collinearity. Time-series cross-validation ensures no look-ahead bias, while residual checks highlight where the model under- or over-explains. I also stress-tested sensitivity to price and promotions, since those often drive real-world trade-offs.

The outputs are designed for growth and marketing teams: insights into which levers matter, guardrails on interpretation (e.g., mediated effects, diminishing returns), and practical recommendations for budget allocation.
