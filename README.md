# Google - American Sign Language Fingerspelling Recognition

Attempt at Google's competitiom on American Sign Language Recognition hosted on Kaggle.

Download the datasets from following links:

[1] [Google - American Sign Language Fingerspelling Recognition](https://www.kaggle.com/competitions/asl-fingerspelling)

[2] [ASLFR dataset tfrecords](https://www.kaggle.com/datasets/irohith/aslfr-dataset-tfrecords)

The goal of this competition was to detect and translate American Sign Language (ASL) fingerspelling into text. We were to create a model trained on the largest dataset of its kind, released specifically for this competition. The data included more than three million fingerspelled characters produced by over 100 Deaf signers captured via the selfie camera of a smartphone with a variety of backgrounds and lighting conditions.

For training the model, I used [preprocessed dataset](https://www.kaggle.com/datasets/irohith/aslfr-dataset-tfrecords) that had precomputed mean, standard deviation of the landmarks present on both hands, arms and shoulder and lips.

The model is based on Transformer architecture as the input and output to the models are sequential. CTC Loss was used while Adam optimizer (RectifiedAdam and Lookahead) was used. The model consists of 18M parameters. More information on model can be found in the notebook attached above. The modelling and inference were successful and tflite model was also created. The model achieved private score of 0.647 and public score of 0.696 which was able to secure me 371 out of 1315 teams. 