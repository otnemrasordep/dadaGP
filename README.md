# DadaGP

[**Paper**](https://archives.ismir.net/ismir2021/paper/000076.pdf) | [**Generation Results**](https://drive.google.com/drive/folders/1USNH8olG9uy6vodslM3iXInBT725zult?usp=sharing)

DadaGP is:

1. a dataset* of ~26k GuitarPro songs in ~800 genres, converted to a token sequence format for generative language models like GPT2, TransformerXL, etc.
2. an encoder/decoder (v1.1) that converts gp3,gp4,gp5 files to/from this token format.

*\* Please contact Dadabots or Pedro Sarmento via email or twitter, [@dadabots](http://twitter.com/dadabots) / [@umpedronosapato](https://twitter.com/umpedronosapato), to request access to the dataset for research purposes.*

## Usage

#### Requirements

* python3
* PyGuitarPro 0.6 *(it ONLY works with 0.6 -- if you're using a newer version, install 0.6 in a virtual environment to run dadagp.py)*
```
pip install 'PyGuitarPro==0.6'
```

#### ENCODE (guitar pro --> tokens)
```
python dadagp.py encode input.gp3 output.txt [artist_name]
python dadagp.py encode examples/progmetal.gp3 progmetal.tokens.txt unknown
```

#### DECODE (tokens --> guitar pro)
```
python dadagp.py decode input.txt output.gp5
python dadagp.py decode progmetal.tokens.txt progmetal.decoded.gp5
```

Note:
* only gp3, gp4, gp5 files supported by encoder;
* rare combinations of instruments and tunings may not be supported;
* banjo is not supported;
* instrument-change events are not supported;

## How to Cite
```
@inproceedings{dadagp2021,
  author = {Sarmento, Pedro and Kumar, Adarsh and Carr, CJ and Zukowski, Zack and Barthet, Mathieu and Yang, Yi-Hsuan},
  booktitle = {Proceedings of the 22nd International Society for Music Information Retrieval Conference},
  title = {{DadaGP: a Dataset of Tokenized GuitarPro Songs for Sequence Models}},
  url = {https://archives.ismir.net/ismir2021/paper/000076.pdf},
  year = {2021}
}

