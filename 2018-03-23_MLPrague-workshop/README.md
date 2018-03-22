# ML Prague: Gensim workshop setup sheet

Please bring your laptop, the workshop is interactive!

Follow the instructions below *before coming*, to minimize installation delays and make sure you’re ready for our Friday workshop.

## Requirements

- Python 3.5 preferred (but 2.7 should work too)
- Install dependencies, download datasets and models:
  ```sh
  pip install gensim==3.4.0 plotly==2.5.0 scikit-learn==0.19.1 jupyter==1.0.0 pandas==0.22 matplotlib==2.2.0
  python -m gensim.downloader --download text8
  python -m gensim.downloader --download 20-newsgroups
  python -m gensim.downloader --download fasttext-wiki-news-subwords-300
  python -m gensim.downloader --download word2vec-google-news-300
  ```
- Fetch the workshop notebooks (will be available on **March 22**):
  ```sh
  git clone https://github.com/RaRe-Technologies/talks.git
  cd talks/2018-03-23_MLPrague-workshop/
  ```
 
## Sanity check

Run the commands below to verify that you have installed all the dependencies successfully:

  - Сheck dependencies (shouldn’t raise an exception): `python -c "import gensim, sklearn, plotly, jupyter, pandas, matplotlib"`
  - Check datasets & models (should print `True`): `python -c "import os; from gensim.downloader import base_dir; print(all(os.path.exists(path) for path in [os.path.join(base_dir, '20-newsgroups', '20-newsgroups.gz'), os.path.join(base_dir, 'text8', 'text8.gz'), os.path.join(base_dir, 'fasttext-wiki-news-subwords-300', 'fasttext-wiki-news-subwords-300.gz'), os.path.join(base_dir, 'word2vec-google-news-300', 'word2vec-google-news-300.gz')]))"`

If in doubt, feel free to reach out at trainings@rare-technologies.com.

See you soon! 🙂
