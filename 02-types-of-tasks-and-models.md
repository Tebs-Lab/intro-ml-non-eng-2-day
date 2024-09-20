# Big Picture AI and ML Concepts

## Narrow vs Broad AI & General AI 

* "Artificial General Intelligence" is what most sci-fi movies portray: A machine that "thinks" in very much the same way we imagine humans and many other animals thinking.
    * Such machines take in all kinds of input (like animals) and can perform reasoning based on those inputs in a wide variety of contexts.
    * The SOTA in AI is currently quite far from this. 

* Instead, we have "narrow" AI systems.
    * These can achieve superhuman results, but only in quite limited domains.
    * AlphaGo can play Go, but it cannot answer even the most basic math questions.
    * Watson can answer a variety of well-formed questions, but can't play Go.
    * Self driving cars can't ride a bike...
        * In fact the "navigation" and "driving" components are separate, and several more purpose-built AI systems power different aspects of driving.
            * A CNN system for object localization
            * A separate system to process LIDAR input
            * A Reinforcement Learning agent to process the outputs of these other AI's and make decisions to turn the wheel or accelerate/decelerate...
            * Explicitly NOT one unified system making decisions. Many smaller systems added together.

* LLMs are probably the most general systems we've made.
    * They can only really produce text... but they can produce realistic text in a wide array of formats.
    * "Emergent behavior" allows them to perform lots of tasks via text generation.
        * e.g. "classify this text for me [the text]"
        * e.g. "score this essay from 1-10 [the essay]"

## Common Types of AI Tasks

"AI" can mean a huge number of things because it's not really a term of art. But here are some things people have historically called "AI": 

* Game Playing
    * Chess, Checkers, Go
* Puzzle Solving
    * Sudoku
    * Crossword
    * Logic problems
* Scheduling & Logistics
    * Planning all the games in an MLB season.
    * Trucking & Freight
* Robotics Control
    * Self Driving
    * Factory automation
* Recommendation Systems
    * Social media feeds
    * Advertising
    * Netflix, Spotify, Pandora, etc.
* Navigation
    * Google Maps
    * Self Driving again
* Classification
    * Facial recognition
    * Object detection / identification
    * Optical Character Recognition
    * Spam Filtering
    * Anomaly Detection
    * Disease screening / detection
* Regression
    * House Price Prediction
    * Patient Recovery time prediction
* Forecasting
    * Financial
    * Weather
    * Physics (3 body problem, for example)
* Generation
    * Image, Audio, and Text are common. Video is emerging.


## Common Types of AI Tactics / Algorithms

Some tactics work better for specific tasks, some tactics are very general and work well for nearly all possible tasks.

* Search
    * Model your problem as a tree or graph, and find relevant connections or paths
    * Game playing systems use this extensively to "look ahead" at possible states. 
    * Google Maps is fundamentally a search problem.
    * Many data mining applications.

* Learning
    * Show the computer many examples and have it build a model from those examples.
    * Very VERY popular now. 
    * 3 main types
        * Supervised -- learn from labeled data
        * Unsupervised -- learn from unlabeled data
        * Reinforcement -- learn from taking actions and receiving rewards in an environment

* Constraint Satisfaction
    * Logic problems and scheduling are great use cases
    * Sudoku and Crosswords are another good use case

* Expert Systems / Rules Based Systems / Symbolic Reasoning
    * Experts explicitly design rules for handling inputs.
    * Formal logic and formal verification systems.

* There are others, but honestly 95% of current AI research is just Learning and Search.

## ML vs Non-ML systems

* Machine learning systems are a form of AI that involve automatically finding patterns in large datasets
* Many AI systems don't work this way. For example:
    * Google Maps uses an explicit model of the world and graph search to find the shortest path between two places.
        * Although ML is now used to predict traffic.
    * Deep Blue (the chess AI) was an "expert system" that just did tree search and used hand crafted algorithms to determine the value of each move.
    * (there are many others, feel free to share your favorite)

* ML is becoming especially popular for a few reasons:
    1. Hardware is much faster now than ever before, and ML works best with access to lots of computational power.
    2. The internet age has resulted in a wide variety of incredibly large datasets.
    3. Some types of patterns are extremely hard to define explicitly, and ML systems have become adept at finding some such patterns. 
        * Computer vision and weather prediction are two prime examples.

## Models, Agents, and Applications

* A final thing to keep in mind is the difference between an "agent" a "model" and an "application"

* Models just take input and turn it into output.
    * It's highly transactional
    * Each input -> output sample is independent.
    * We're going to look at how models are built in significant depth in just a moment.
    * "Model" means something pretty specific to AI people.

* Agents take action over time in an environment
    * Some agents are "trained," similar to how neural networks are trained
    * Others are more simplistic rules followers
    * They may incorporate one or more models.
    * Refer to the above examples (Siri, self driving, ChatGPT)

* Applications are far more general. Anything is an application.
    * ChatGPT's interface is an application that includes an agent
    * Game playing AI's are agents, but to actually enact the game itself (so a human can play too) there would need to be more application code.

* Increasingly, the definition of an "agent" is becoming muddled and confusing. 
    * Partly this is because it's becoming a kind of marketing term. 
    * Partly it's because "AI" capabilities have just gotten much better and more varied, which inherently expands the scope of the definition
    * Partly it's because they're becoming more deeply integrated into systems, blurring the line between "application" and "agent" 
        * In June 2024 for example, Siri

 * Talk through a couple examples:
    * GPT-4 is a model, ChatGPT is an agent.
        * ChatGPT relies heavily on GPT-4 to read and write text.
        * ChatGPT produces text repeatedly in the chat environment.
        * ChatGPT has some memory of the various prompt/responses in a session.
        * ChatGPT can do additional things like perform web searches and execute code snippets sent to the service. 

    * Siri is an agent that (as of June 2024) is about to get much more complicated. 
        * For many years Siri was quite simple
            * Set timers, send texts, do a web search... 
            * Speech to text model first, then text to possible actions model (likely an LLM). 
            * Finally some code that causes the actions to happen. (set timer, send text)
        * But following the Apple Intelligence announcements, Siri is going to have much more access to other applications and the operating system.  

    * Self Driving Cars are more complex agents
        * Many models for processing the various inputs (visual, audio, LiDAR, etc.)
        * An agent then makes decisions about how to drive at each time step based on the various models.