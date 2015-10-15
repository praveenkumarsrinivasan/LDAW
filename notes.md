### What is Topic Modelling?
<hr/>

- Docs are mixture of Topics
- Topic is a Probability Distribution over words
- Topic Model is Generative Model for Documents
- Generative Probabilistic Model: A simple probabilistic procedure by which documents can be generated.
- A method for finding and tracing clusters of words (called “topics” in shorthand) in large bodies of texts.
- Topic: a recurring pattern of co-occurring words

Notes:
- Probability Distribution: Sum of all the probabilities of words is 1.
- Probabilities are on the scale 0-1.
- Example: Topic is Food
Here, The probability distribution is broccoli(0.3), bananas(0.5), breakfast(0.1), munching(0.1)

-----

### Types of Models

- Generative: is a model for randomly generating observable-data values, typically given some hidden parameters
    + can be used to generate values of any variable in the model
- Discriminative | Conditional: models the dependence of an unobserved variable y on an observed variable x
    + do not allow one to generate samples from the joint distribution of x and y
- Mixture: is a probabilistic model for representing the presence of subpopulations within an overall population, without requiring that an observed data set should identify the sub-population to which an individual observation belongs
- Graphical
- Geometrical

---

### How does Topic Modelling Work?

- Given, a collection of documents, and we want to identify underlying “topics” that organize the collection.
- Assume that each document contains a mixture of different topics.
- Let’s also assume that a “topic” can be understood as a collection of words that have different probabilities of appearance in passages discussing the topic

---

### Generative Model
<hr/>

- **Topics**: probability distribution over words
- Topic Model are based on the idea that **documents are mixture of topics**
- **Topic Model**: generative model for documents

-----

Objective: Discover topics that these sentences contain.

For example, given these sentences and asked for 2 topics

```
- I like to eat broccoli and bananas.
- I ate a banana and spinach smoothie for breakfast.
- Chinchillas and kittens are cute.
- My sister adopted a kitten yesterday.
- Look at this cute hamster munching on a piece of broccoli.
```

Output will be something like

```
- Sentences 1 and 2: 100% Topic A
- Sentences 3 and 4: 100% Topic B
- Sentence 5: 60% Topic A, 40% Topic B
```

- Topic A: 30% broccoli, 15% bananas, 10% breakfast, 10% munching
    (Topic A: Interpreted as food)
- Topic B: 20% chinchillas, 20% kittens, 20% cute, 15% hamster
    (Topic B: Interpreted as cute animals)

-----

### Generative Probabilistic Model
<hr/>

- Treats data as observations that arise from a generative probabilistic process that includes hidden variables
- Infer the hidden variables using posterior inference
- Fit the new data into the estimated model
---

- In reality, we can’t directly observe topics;
- all we have are documents.
- Topic modeling is a way of deducing backward from a collection of documents to infer the  “topics” that could have generated them
- There is no straightforward way to infer the topics exactly: there are too many unknowns
- Therefore we rely on Statistical techniques to invert the Generative process.

---

### Statistical Techniques to Invert Topic Modelling

- EM
- LSI
- PLSI
- LDA

---

### What is LDA?

- Introduced by David Blei, Andrew Ng, Micheal Jordan in 2003
- Generative Probabilistic Model

Notes:
- Theory and Formulation
- Core

---
How does LDA Work?


---

### Notations for LDA

---

### Theory of LDA

---

### Applications of LDA

- Topic Modelling

---

### Variations of LDA

- LDA
- Labelled LDA
- Supervised LDA
- Disc LDA
- MM LDA


---

### LDA in NER: Labelled LDA

---

### What is Labelled LDA?

- Christopher Manning
- Applications

---

### Labelled LDA vs LDA

---

### Existing Literature

- Nguyen

- Alan Ritter



<math xmlns="http://www.w3.org/1998/Math/MathML" display="block" style="padding: 15px;">
  <mo stretchy="false">(</mo>
  <munderover>
    <mo>&#x220F;<!-- ∏ --></mo>
    <mrow class="MJX-TeXAtom-ORD">
      <mi>k</mi>
      <mo>=</mo>
      <mn>1</mn>
    </mrow>
    <mrow class="MJX-TeXAtom-ORD">
      <mi>K</mi>
    </mrow>
  </munderover>
  <mi>p</mi>
  <mo stretchy="false">(</mo>
  <msub>
    <mi>&#x03B2;<!-- β --></mi>
    <mi>k</mi>
  </msub>
  <mrow class="MJX-TeXAtom-ORD">
    <mo stretchy="false">|</mo>
  </mrow>
  <mi>&#x03B7;<!-- η --></mi>
  <mo stretchy="false">)</mo>
  <mo stretchy="false">)</mo>
  <mo stretchy="false">(</mo>
  <munderover>
    <mo>&#x220F;<!-- ∏ --></mo>
    <mrow class="MJX-TeXAtom-ORD">
      <mi>d</mi>
      <mo>=</mo>
      <mn>1</mn>
    </mrow>
    <mrow class="MJX-TeXAtom-ORD">
      <mi>D</mi>
    </mrow>
  </munderover>
  <mi>p</mi>
  <mo stretchy="false">(</mo>
  <msub>
    <mi>&#x03B8;<!-- θ --></mi>
    <mi>d</mi>
  </msub>
  <mrow class="MJX-TeXAtom-ORD">
    <mo stretchy="false">|</mo>
  </mrow>
  <mi>&#x03B1;<!-- α --></mi>
  <mo stretchy="false">)</mo>
  <mo stretchy="false">(</mo>
  <munderover>
    <mo>&#x220F;<!-- ∏ --></mo>
    <mrow class="MJX-TeXAtom-ORD">
      <mi>n</mi>
      <mo>=</mo>
      <mn>1</mn>
    </mrow>
    <mrow class="MJX-TeXAtom-ORD">
      <msub>
        <mi>N</mi>
        <mi>d</mi>
      </msub>
    </mrow>
  </munderover>
  <mi>p</mi>
  <mo stretchy="false">(</mo>
  <msub>
    <mi>z</mi>
    <mrow class="MJX-TeXAtom-ORD">
      <mi>d</mi>
      <mo>,</mo>
      <mi>n</mi>
    </mrow>
  </msub>
  <mrow class="MJX-TeXAtom-ORD">
    <mo stretchy="false">|</mo>
  </mrow>
  <msub>
    <mi>&#x03B8;<!-- θ --></mi>
    <mi>d</mi>
  </msub>
  <mo stretchy="false">)</mo>
  <mo stretchy="false">(</mo>
  <mi>p</mi>
  <mo stretchy="false">(</mo>
  <msub>
    <mi>w</mi>
    <mrow class="MJX-TeXAtom-ORD">
      <mi>d</mi>
      <mo>,</mo>
      <mi>n</mi>
    </mrow>
  </msub>
  <mrow class="MJX-TeXAtom-ORD">
    <mo stretchy="false">|</mo>
  </mrow>
  <msub>
    <mi>z</mi>
    <mrow class="MJX-TeXAtom-ORD">
      <mi>d</mi>
      <mo>,</mo>
      <mi>n</mi>
    </mrow>
  </msub>
  <mo>,</mo>
  <msub>
    <mi>&#x03B2;<!-- β --></mi>
    <mi>k</mi>
  </msub>
  <mo stretchy="false">)</mo>
  <mo stretchy="false">)</mo>
  <mo stretchy="false">)</mo>
  <mo stretchy="false">)</mo>
</math>
