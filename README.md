# LiFi-Full service
This project is an application that helps people search for the song's name based on a given audio from the user. We use the Neural Audio Fingerprint model which was proposed in a paper published in 2021, [NEURAL AUDIO FINGERPRINT FOR HIGH-SPECIFIC AUDIO RETRIEVAL BASED ON CONTRASTIVE LEARNING](https://arxiv.org/pdf/2010.11910.pdf) to embed audio, FAISS for getting items, and we use our method that we self-design to calculate the similarity between each candidate song and the input audio.
## Source code
Please follow the below link to access the source code.

[https://gitlab.com/thompsondd/lifi-fullservice](https://gitlab.com/thompsondd/lifi-fullservice)

## Getting started

### Manual
In order to run the application, you have to run it manually:
- File **app.py** in folder **Web_Server** to run website ( ``` python app.py ``` )
- File **run.py**in folder **API_Server** to initialize model and use it via API (``` python run.py ``` )

### Docker
You can also run the application by Docker thorough running the below commands:
```
cd YOUR_PROJECT_PATH
docker compose up -d
```

## Limitation
Because of the lack of resources to crawl music audio, we have to train the model in our small dataset which makes the system's accuracy unstable. In addition, the system can only recommend the name of the song in the dataset, so if you give it audio out of the dataset, it will return names of songs in our dataset and they will be similar given audio.

## Authors
- [Nguyễn Huỳnh Hải Đăng (gitlab - thompsondd)](https://gitlab.com/thompsondd)
- [Phạm Thiên Bảo (gitlab - beetibao)](https://gitlab.com/beetibao)
- [Trần Đình Khôi (gitlab - khoi03)](https://gitlab.com/khoi03)
- Bùi Quốc Thịnh

## Reference
- [NEURAL AUDIO FINGERPRINT FOR HIGH-SPECIFIC AUDIO RETRIEVAL BASED ON CONTRASTIVE LEARNING, ICASSP - 2021](https://arxiv.org/pdf/2010.11910.pdf)
