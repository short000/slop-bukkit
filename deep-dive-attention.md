**Deep Dive into the Transformer Attention Mechanism**

Chip Huyen's book "AI Engineering" Chapter 2, "Understanding Foundation Models" has a short introduction to the transformer architecture. She goes into enough Query, Key, and Value vectors (Q, K, V) details to get started, but it felt very incomplete the first time I went through it. Here are my study notes on filling that gap:

1. Strongly recommended: go through all 8 of these 3Blue1Brown Neural Network videos first.
   - https://www.3blue1brown.com/topics/neural-networks

Somewhat time consuming, but important enough to watch several times. I usually do not like watching videos more than once, but that series is a strong exception.

2. Optional: assuming you already know back propagation (as part of the background in #1 above), it may also help for you to understand how LLMs are trained before getting into attention mechanisms.
   - Watch CodeEmporium's intro: https://www.youtube.com/watch?v=TQQlZhbC5ps
   - Watch CodeEmporium's explanation of Transfer Learning: https://www.youtube.com/watch?v=QHS9ZZBdK-g
   - Watch Bingyang Wei's general explanation on the steps used to train ChatGPT. Step 2, Supervised Fine Tuning, is a type of Transfer Learning used to train ChatGPT and other LLMs: https://www.youtube.com/watch?v=Mem2LWNCXek
   
3. Switch to Serrano Academy's 4-video playlist on Attention Mechanisms.
He deliberately introduces the math concepts in a highly oversimplified manner so that it is just enough to know WHY and WHEN you would want to deep dive into understanding the math.
   - https://www.youtube.com/watch?v=OxCpWwDCDFQ&list=PLs8w1Cdi-zvYskDS2icIItfZgxclApVLv&index=1
   - https://www.youtube.com/watch?v=UPtG_38Oq8o&list=PLs8w1Cdi-zvYskDS2icIItfZgxclApVLv&index=2
   - https://www.youtube.com/watch?v=qaWMOYf4ri8&list=PLs8w1Cdi-zvYskDS2icIItfZgxclApVLv&index=3
   - https://www.youtube.com/watch?v=RFdb2rKAqFw&list=PLs8w1Cdi-zvYskDS2icIItfZgxclApVLv&index=4

4. Click through the 20 steps in the visual Transformer Explainer for GPT-2.
   - https://poloclub.github.io/transformer-explainer/

5. Watch the CodeEmporium guy walk the concepts all the way through the architecture.
   - https://www.youtube.com/watch?v=ekg-hoob0SM&t=40s

6. Expose yourself to the compact math summary in Andriy Burkov's 100 Page Language Models Book. You might be able to skip to Chapter 4, "Transformers" if the content in Chapters 1 & 2 look like a review to you.
   - https://thelmbook.com

6. Get Welch Lab's Illustrated Guide to AI 
($22 PDF, $79 hard cover) It has 9 chapters, each paired with high-quality YouTube videos.
Math dense but heavily illustrated, also backed by high quality videos dense with animated 2D and 3D visualizations.
Chapter 8, "Attention" is paired with "How DeepSeek Rewrote the Transformer [MLA]"
