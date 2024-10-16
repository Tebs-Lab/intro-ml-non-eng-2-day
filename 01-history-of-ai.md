# Brief History of AI

A bit of background helps us understand both how we got here, and why people are excited about current models and methods.

*Instructor note: go fast, don't get into the weeds. Draw a timeline on the whiteboard*

## Early days: 1940s-50's: 
### Lots of experiments, lots of excitement, some limited success.

* 1943: the first Neural Network was described in a paper by Warren McCulloch and Walter Pitts
    * [https://link.springer.com/article/10.1007/BF02478259](https://link.springer.com/article/10.1007/BF02478259)
* 40-50, Bletchley Park -- Alan Turing and the Enigma code breaking effort.
    * 1950, he describes the "Turing Test" / "Imitation Game"
* 1950 Claude Shannon made the first chess playing program.
* 1951, the first neural network is built using a vacuum tube computer. (Marvin Minksy, Dean Edmunds)
* 1952, Arthur Samuel makes a checker playing system that learns on it's own.
* 1955, Dartmouth Summer Research Project on Artificial Intelligence (1956)
    * John McCarthy: "We think that a significant advance can be made in one or more of these problems if a carefully selected group of scientists work on it together for a summer."
    * This is when the term "Artificial Intelligence" was coined.
* 1955, Logic Theorist is invented, which eventually proves the first 38 theorems of Pricipia Mathematica.
* 1959, Arthur Samuel coins the term "machine learning"

* Fundamentally limited computers: low speed, small memory, hugely expensive.
    * Vast majority of systems were "rules based," with humans explicitly programing the rules. 
    * The learning models were very small, didn't work that well.
    * Learning systems were heavily augmented with rules
    * Noam Chomsky did a lot of work trying to model grammar mathematically
    
* Major areas of focus were:
    * Code breaking
    * Machine translation
    * Game playing (chess/checkers)
    * Formal Verification / Math proofs

* This was a period of extreme excitement, many people in the 50s declared machine translation would be a solved problem by the end of the decade
    * Narrator: It wasn't.

## 1960s: Excitement -> Disappointment
### Turns out this stuff is hard.

* The main theme of the 60's, especially the last half of the decade, is that everything was harder than originally thought.
    * Computers were still very slow and not that powerful.
    * Results weren't that impressive, especially compared to the hype.
    * Most systems were still "rules based" 
        * In fact one major paper by Marvin Minksy and Seymour Papert "Perceptrons: An Introduction to Computational Geometry" made a lot of fuss about the limitations of Neural Networks and basically argued against statistical learning as a meaningful path forward.
            * (Turns out they just needed much better computers...)
    * Research grants fell off substantially.

* 1961, Symbolic Automatic Integrator: a program that solves integrals (calculus)
* 1965, Herbert Simon: "machines will be capable, within twenty years, of doing any work a man can do."
    * Narrator: They weren't.
* 1965, I.J. Good: "the first ultraintelligent machine is the last invention that man need ever make, provided that the machine is docile enough to tell us how to keep it under control."
* 1965: ELIZA was one of the first successful "chatbots" 
    * Specifically it was a "reflection based" psychotherapist system.
    * Quite limited in scope and capability, in part due to computer memory constraints.
* 1969: Arthur Bryson and Yu-Chi Ho first describe **backpropagation** which remains key to modern learning systems.


## 1970's-85's:  AI Winter
### Computers are good at other stuff, who needs AI?

* Way less research funding and interest.
* Smaller cohort of researchers.
* Not a lot happened, honestly.
* 1973, James Lighthill sums it up: "in no part of the field have discoveries made so far produced the major impact that was then promised."

## 1985-2000: The Rise of Statistical Models, Death of Expert Systems
### Faster Computers and Internet Scale Data Revive AI

* Computing and AI was once again popular in the public zeitgeist.
* Widespread adoption of computers and the internet created huge amounts of data.
* Advances in computer hardware breathed new life into all kinds of AI.
    * Faster computation for statistical methods.
    * Larger vocabularies and rule sets for chatbots.
    * Larger search trees for game playing algorithms.
    * ...

* 1986, Geoffrey Hinton and Ronald Williams publish a compute-efficient system for applying backpropagation to neural networks.
    * The eventual impact of this work *cannot* be overstated.
* 1988, Judea Pearl, "Probabilistic Reasoning in Intelligent Systems"
    * Effectively invents the first Naïve Bayesiean learning models for making decisions with uncertinty.
* 1988, the Jabberwacky chatbot is created.
* 1988, IBM Watson Group publishes "A statistical Approach to Language Translation"  
* 1989, Yann LeCun successfully apply Hinton's Backpropagation method to a multi layer neural network.
    * They used it to train a model that can read handwritten zip codes. (MNIST dataset, baby!)
* 1993, Vernor Vinge, "within thirty years, we will have the technological means to create superhuman intelligence. Shortly after, the human era will be ended."
    * 30 years was 2023, so that hasn't quite happened.
* 1995, ALICE, another chatbot inspired by ELIZA, but with Learning and much more data.
* 1997, Deep Blue becomes the first computer program to beat a reigning world champion.

## 2000-2017: Learning "The Bitter Lesson" 
### Clever Algorithms < Statistical Pattern Matching At Scale
### Specialized Neural Network Architectures Dominate SOTA

* Richard Sutton will describe in 2017 the lessons learned in this era in his essay "The Bitter Lesson"
    * "Two methods scale infinitely with compute, Learning and Search." 
    * Huge data + powerful computers are the key combo for unlocking statistical methods
    * Basically, clever rules where we try to really understand and exploit the domain of the problem are less effective than letting the computer figure out the problem using "general methods" like learning and search.
    * Work begins to focus on taking data, turning it into a numerical format, and letting "general" learning systems figure out patterns on their own.
        * Mostly via Neural Networks and Backpropagation.

* Additionally, tech giants start finding good uses for AI tools, which drives huge investment.
    * Social Media, Netflix, Pandora: "recommendation systems" 
    * Pandora and the "Music Genome Project" (basically embeddings for songs)
    * Google, Search & Maps. 

* 2003, Yoshua Bengio coins the term "word embeddings" -- applying vector representations to text.
* 2006, Geoffry Hinton, "Learning Multiple Layers of Representation"
    * Important Scaffolding for generative systems and "Deep" neural networks.
* 2007, Fei Fei Li starts collecting ImageNet benchmark dataset.
* 2009, Andrew Ng et al publish Large-scale Deep Unsupervised Learning using Graphics Processors.
    * Modern CPU speeds had stagnated by now, so parallelizing the backpropagation was key to allowing Deep Neural Networks to continue getting faster.
* 2011, IBM's Watson plays "Jeopardy!" and wins.
* 2011 & 2012, Convolutional Neural Network's break SOTA results in several computer vision benchmarks.
* 2014, Goodfellow et al invent first "deep fake" GAN for human faces.
* 2016, AlphaGo defeats Lee Sedol.

## 2017-current: Leaning Into The Bitter Lesson
### Enormous Computers and Efficient Computation Methods Yield 
### Plus, "Generative" Models Emerge

* 2017, "attention is all you need," introduces the Transformer architecture
    * Basically instant obliterates every SOTA result in NLP by embracing the bitter lesson
    * Previous SOTA (Recurrent Neural Networks) could not take advantage of GPU hardware, Attention/Transformers can. Boom. 
* 2018, OpenAI releases GPT-1
* **2019, "The Bitter Lesson" published by Richard Sutton**
    * Researchers all but abandon all methods that aren't Learning or Search. 
    * Researchers focus on clever math/algorithmic tricks that improve the speed of specific kinds of calculations.
    * Researchers focus on representing data in ways that can take advantage of those speed improvements.
* 2020, GPT-3
* 2021, DALL-E-1 (Diffusion Models supplant GANs)
* 2022, ChatGPT
* ... You probably know the rest ...
