
# Spotify Review Prediction & Analysis

This project utilizes a bi-directional RNN in order to predict and analyze the rating of a review from its text content.


## Usage/Examples

```py
reviews = [
  "Really buggy and terrible to use as of recently", 
  "Really good experience. Amazing app and I highly reccomend!"
]

predictions = model.predict(np.array(reviews))

# return values to a 1-5 scale
normalized = np.round(predictions * 5)

print(normalized)
# [[1.], [5.]]
```


## How it works

The model is made up of 5 layers. First the text goes into an encoder or "TextVectorization" layer. This layer is trained on the text and creates a vocab. It assigns each word its own value inside the vocab. This is because its much easier to process numbers instead of strings in the next layer. The next layer is an Embedding layer. It takes the encoded values and maps them to the lookup table of the Embedding layer. The Embedding layer works by mapping together similar words and phrases and their meanings.

The next layer utilizes a bidirectional layer that uses a LSTM (long-short term memory) recurrent neural network. The RNN analyzes the text in a both forward and backward manner due to its bidirectional state. Since the data text is static in this analysis the bidirectional nature helps. Finally there are 2 dense layers to classify the review.


## Dataset

Trained on the "Spotify App Reviews" Dataset on kaggle.com (https://www.kaggle.com/datasets/mfaaris/spotify-app-reviews-2022)


## License

[MIT](https://choosealicense.com/licenses/mit/)

