from wordcloud import WordCloud, STOPWORDS
import matplotlib.pyplot as plt
from PIL import Image
import numpy as np
import pandas as pd

data = pd.read_csv('text.csv')
mask = np.array(Image.open('nirob.png'))

wordcloud = WordCloud(
    stopwords=set(STOPWORDS),
    mask=mask,
    background_color="black",
    colormap="Set3",
    width=1600,
    height=800
).generate(' '.join(data['text']))

background = np.array(Image.open('background.jpg'))

plt.figure(figsize=(10, 10))
plt.imshow(background, interpolation='bilinear')
plt.imshow(wordcloud, interpolation='bilinear', alpha=0.7)
plt.axis('off')
plt.show()
