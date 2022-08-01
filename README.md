
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

f


## Dataset

Trained on the "Spotify App Reviews" Dataset on kaggle.com (https://www.kaggle.com/datasets/mfaaris/spotify-app-reviews-2022)


## License

[MIT](https://choosealicense.com/licenses/mit/)

