# Applying LDA 

Suppose we've a text corpus 
- We will assume that it has N number of documents
- We will have to search "k" number of topics (this is difficult for LDA to search for indefinite number of topics, and we must decide on the number of topics according to the factors such as situation, field of work and volume of the data etc. 
- We will have to determine that from the given k topics, how many are represented in each documents as probablity
- We will also find the probablity of each word (words only from that text corpus) in each topic


What we will do initially, is that we go through each document and randomly assign a word to a k topic, and by doing this we will get

- Every topic's represented in each document
- Every words's representation in each topic

Note: We are initially assigning Randomly, which doesn't make any sense, as assigning this way we are not going to get the results upon which we can trust. 

Which is why in the next stage, we are going to enumerate through each word in each document and try to better the results we got from the Random Assignment strategy in the Initial stage. 

We will apply the following on all topics from each document

```
p(topic t | document d) 
means the probability of each topic by each document
```

Then we will apply the same for each word against the Topic as follows

```
p(word w | topic t) 
means the probability of each word by each topic
```

Then we will assign a new word to the topic t, where the topic t will be represented in the following way

```
p(topic t | document d) * p(word w | topic t)
means we are multiplying the probablity of the topic t in document d with the probablity of that word w in the topic t
```

By doing this, we will get the probablity representation of the word which is given to us by the Topic. 

We are going to repeat the above steps, numerous number of times, until we get a reliable result.
After doing the above excercise, we will be getting a representation of (say 7 topics) across the text corpus.
And we will be getting the top 10 words by probablity in each topic. 

and Off course we will be able to apply an appropriate Topic name (rememebr LDA doesn't do that for us) to each topic.


