# Natural Language Processing - Assignment 1

Name: Divita Phadakale (diph8836)

Steps to run the code:

1. Write a function that calculates the unigram probability of a word appearing in some corpus.
- This can be run as it 
- input - the unigram word, word count table for the corpus
- output - (float) unigram probability

2. Importing all the required corpus
- For importing required corpus

3. Calculate V : unique words in vocabulary
- For calculating V to be used in the Laplace smooting later on
- input - corpus
- output - V (size of vocab)

4. Tokenize words of given corpus and store word count
- For getting tokens of given corpus and also calculate word counts to use later on (during conditional probability)
- input - corpus
- output - list of tokens

5. Create Bigrams: Write a function that finds all bigrams in a sentence and returns them as a list of tuples.
- To get all bigrams of corpus
- input - tokenized corpus
- output - list of bigrams as tuples

6. Conditional Probability (BIGRAMS)
- Calculate conditional probabilities of all the bigrams
- input:
    - word 1
    - word 2
    - bigrams count of a particular corpus
    - word count of that corpus (calculated in step 4.)
    - V of that corpus (calculated in step 3.)
- output - map of all bigram conditional probabilities 

7. Predict next word (BIGRAMS)
- predict next word using conditional probabilities
- input:
    - initial word
    - bigrams of a corpus
    - precalculated conditional probability map (from above step)
- output - next probable word

8. Predict sentence (BIGRAMS)
- predict a sentence by continually calling predict next word
- input:
    - initial sentence
    - bigrams of a corpus
    - precalculated conditional probability map (same as above step)
- output - a sentence

The same for trigrams with some additional but similar parameters

9. Perplexity for Bigrams
(have used sum of logs concepts here in place of product of probabilities as it was giving me division by zero error)
- input:
    - sentence for which perplexity is to be calculated
    - precalculated conditional probability map (from step 6.)
    - bigrams count of that corpus
    - word count of that corpus (calculated in step 4.)
    - V of that corpus (calculated in step 3.)
- output - perplexity of the given sentence

10. Perplexity for Trigrams
(have used sum of logs concepts here in place of product of probabilities as it was giving me division by zero error)
- input:
    - sentence for which perplexity is to be calculated
    - precalculated conditional probability map (from step 6.)
    - bigrams count of that corpus
    - trigrams count of that corpus
    - V of that corpus (calculated in step 3.)
- output - perplexity of the given sentence

11. Testing trained data using Brown, Webtext and Reuters corpus
- testing based on 5 sentences from Brown data
- testing based on 5 sentences from Webtext data
- testing based on 25 sentences from Reuters data + taking average perplexity


PS: 1 change i did from my previous submission is - i am storing bigram and trigram counts using counter to make it work in less time!