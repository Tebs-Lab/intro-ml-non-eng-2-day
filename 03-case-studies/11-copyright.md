# Regurgitation, Overfitting, and Copyright

Generative Models are known to sometimes return exact, or nearly exact, copies of their training data inputs. Here's an example from IEE Spectrum: (https://spectrum.ieee.org/midjourney-copyright)[https://spectrum.ieee.org/midjourney-copyright]

> Ultimately, we discovered that a prompt of just a single word (not counting routine parameters) that’s not specific to any film, character, or actor yielded apparently infringing content: that word was “screencap.” The images below were created with that prompt.

![](assets/a-grid-of-six-images-created-by-midjourney-showing-famous-pop-culture-characters.webp)

The aforementioned NYTimes lawsuit also contains examples of ChatGPT producing verbatim copies of NYTimes articles. 

In addition to intellectual property questions, similar behavior has raised privacy questions. For example, here's an article from the New York Times [https://www.nytimes.com/interactive/2023/12/22/technology/openai-chatgpt-privacy-exploit.html](https://www.nytimes.com/interactive/2023/12/22/technology/openai-chatgpt-privacy-exploit.html):

> My contact information was included in a list of business and personal email addresses for more than 30 New York Times employees that a research team, including Mr. Zhu, had managed to extract from GPT-3.5 Turbo in the fall of this year. With some work, the team had been able to “bypass the model’s restrictions on responding to privacy-related queries,” Mr. Zhu wrote.

> [...]

> OpenAI released its fine-tuning interface for GPT-3.5 last August, which researchers determined contained the Enron dataset. Similar to the steps for extracting information about Times employees, Mr. Zhu said that he and his fellow researchers were able to extract more than 5,000 pairs of Enron names and email addresses, with an accuracy rate of around 70 percent, by providing only 10 known pairs.

## Additional Questions:

* Why might models produce exact or near exact copies of their training data?
    * Is there anything about training that could make this more or less likely?
* Does this behavior create legal liability for end users?
* How substantial do you think the privacy concerns are?
    * Where are AI firms getting their training data?
* How could you mitigate or eliminate this behavior?