# CelebA_HQ_Downloader

Scripts for CelebA-HQ Dataset Download

## Reference

- [https://github.com/tkarras/progressive_growing_of_gans/tree/original-theano-version](https://github.com/tkarras/progressive_growing_of_gans/tree/original-theano-version)
- [https://github.com/willylulu/celeba-hq-modified](https://github.com/willylulu/celeba-hq-modified)

1. Make folder

```sh
cd CelebA_HQ_Downloader
mkdir celeba-hq
cd celeba-hq
mkdir celeba-64
mkdir celeba-128
mkdir celeba-256
mkdir celeba-512
mkdir celeba-1024
```

2. Download Data

- CelebA: [https://drive.google.com/drive/folders/0B7EVK8r0v71peklHb0pGdDl6R28](https://drive.google.com/drive/folders/0B7EVK8r0v71peklHb0pGdDl6R28)
- CelebA-HQ(delta): [https://drive.google.com/drive/folders/0B4qLcYyJmiz0TXY1NG02bzZVRGs](https://drive.google.com/drive/folders/0B4qLcYyJmiz0TXY1NG02bzZVRGs)
- Anno: [https://drive.google.com/drive/folders/0B7EVK8r0v71pOC0wOVZlQnFfaGs?resourcekey=0-pEjrQoTrlbjZJO2UL8K_WQ](https://drive.google.com/drive/folders/0B7EVK8r0v71pOC0wOVZlQnFfaGs?resourcekey=0-pEjrQoTrlbjZJO2UL8K_WQ)

3. Unzip `CelebA`

```sh
7za e img_celeba.7z.001
```

4. Make Folder Structure

```sh
celebA/
  A/
    img_celeba/
    Anno/

  B/
    deltas00000.zip
    ...
    ...

CelebA_HQ_Downloader/
  h5tool.py
  ...
```

5. Make a anaconda virtual environment

```sh
conda create --name python_2 python=2
source activate python_2
pip install scipy numpy Pillow cryptography
```

6. Start ^_^

```sh
cd CelebA_HQ_Downloader
python h5tool.py create_celeba_hq 123456.h5 ../celebA/A ../celebA/B
```
