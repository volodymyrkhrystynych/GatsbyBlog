#Natural Language Processing and machine learning in Alzheimer's detection
##Jaketerina Novikova
##Winterlite labs
##Director at company trying to diagnose cognitive health

Alzheimer's disease is a n irreversible neurodegenerative diseaese that destroys brain cells, causing thinking ability and memory deterioration.

They have a prototype app that requires a user to describe a picture that is shown to them, using this they can analyse the speach and distinguish the different features in their speech, ie duration of pauses, frequency, word use.

Pyaudio analysis is an open source tool that allows you to extract such audio features.
Can generate transcripts using kaldi or asr
Extract linguistic from the transcript using spacy

Consensus networks

motivation:
to improve accuracy you can either increase training data, or gather more features using expert advice. Both are quite expensive

consensus networks are inspired by GANs with no generator, just discriminator

Features go into dimentional reduction agents, all go into a classifier as well as a discriminator, discriminator gets a noise impot as well

Tricks that improve performance
noise modality
cooperative optimisation
natural modalities

adding gaussian noise to the discriminator forces it to study the details improves the accuracy by 5%
Using the ephysicians to produce both indistinguishable and beneficial representations improves the accuracy by 15%
Dividing features into subsets according to their natural modalities is better than doing so randomly
Given the same combinations of features, letting NN produce representations in agreement does improve the performance

It is important to not just use all the features, but to use the agreement between the features

discriminator does not need labeled data to recognize modalities, thus a consensus network can be used in semi superviced learning

Modalities that she was refereing to were audio features, symantic features and so on.
Each agent that reduces the dimention is a simple neural network.
