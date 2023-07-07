# Abstractive Text Summarizer
Our Abstractive Text Summarizer is designed to produce summaries that closely mirror human-like comprehension and synthesis abilities. The algorithm is capable of understanding context and distinguishing between homographs, such as "Python" as a programming language and "python" as a snake.

## Data Collection and Cleaning
Our data was manually collected, minimizing errors commonly found in automatically scraped data. Each article was thoughtfully summarized according to specific guidelines, ensuring consistency in the data set. A crucial aspect of our data collation process involved maintaining a consistent length across all input texts to prevent truncation during tokenization and also to prevent unncecessary padding which can demand more computational infrastructure.

## Pre-processing
As this project centers around summarization, extensive pre-processing like stop word removal, lemmatization, and stemming was not needed - each word and its context contribute significantly to a reliable summary. The preprocessing included lower-casing text and reducing multiple spaces to a single space.

## Tokenization
We employed BART Tokenizer for tokenization. Our tokenization process was straightforward and efficient, thanks to the data collation phase where we had already considered potential tokenization issues.

## Model Selection and Argument Setup
We utilized the pre-trained "facebook/bart-large" model. Training arguments were appropriately adjusted to optimize compatibility with our data. The model was trained and yielded a loss of 6.4. We intentionally refrained from using global perception metrics like "Rogue Score" or "BLEU" in favor of aligning our summaries with the given target column.

## Model Evaluation
During evaluation, the model surprisingly performed better than in the training phase, recording a lower loss of 3.9. This demonstrates the robustness and effectiveness of our Abstractive Text Summarizer.


