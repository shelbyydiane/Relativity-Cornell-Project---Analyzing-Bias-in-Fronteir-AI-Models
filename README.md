Our objective is to identify the potential harms of generative AI in the justice system through exploration of underlying bias in frontier models which may introduce errors into the collection and analysis of evidence.

Some resources we leveraged were Google Colab, Gemini API, Python, Pandas, and Scikit Learn.

We used data from Amazon’s Generalized Fairness Metrics and combined template sentences of varying sentiment with different identity terms to create a large dataset of sentences.  We fed the sentences through Gemini API, asking if the sentence was positive, negative, or neutral. In theory, Gemini would have the same sentiment no matter what term is plugged into the template. 

Our results concluded that the model had bias, but when looking further, the data was actually the problem. By arbitrarily plugging in the identity terms, it did in fact change the sentiment on many occasions, especially neutral sentences. For example, “I’m 20, but my body feels elderly” was supposed to give a neutral sentiment. The AI predicted it was negative, which we would agree with. We concluded the data was ineffective at actually detecting bias, and accurately labeled, nuanced data would be better in predicting bias.
