# Music-Style-Recombination-and-Interpolation
Final Project for Introduction to Computer Music at NYU Shanghai

link for demo:

# Description
Inspired by the findings of Mukherjee, Asnani, Eugene and Kannan that interpolation in the latent space can be preserved, We design an algorithm to implement music style recombination and interpolation with manipulation of the latent variables and attempt to close the loop of music. We first extract pitches and chords from two groups of wav files: group for pitches and group for rhythms. With extracted information, We reconstruct the audio as simple midi files for which the pitches and rhythms are preserved. We then use EC2VAE to obtain the latent variables for both groups. We use a user-defined interpolation method to obtain representative latent variables for the two groups and recombine pitch and rhythm to generate a new piece. In addition, We use midi- level composition technique and wave level synthesis to process the raw file, increasing the musicality and variation of the piece.

# Music Information Retrieval
Pitch extraction: Different options: Madmom, librosa, sonic-visualizer built-in; Our choice: python implemented pYIN + algorithms to merge short notes and notes with similar frequency

Chord extraction: Madmom function

# Quantization
Transform standard midi files into forms suitable for EC2VAE. Divide the audio into units of two measures

# Formalization
Use EC2VAE to preprocess the melody we extracted before combining it with other melodies.

# Style Recombination
Get representative latent variables from input songs using interpolation (Interpolation in latent space is preserved).
Feed them into EC2VAE and generate a new piece in the midi format.

# Composition and Synthesis
MIDI level: Canon, Play chord in a 16th note level, Pitch Interpolation
WAV level: Decomposition of chords into 16th note, Sound generation (cos wave)

# Last but not least...
With great thanks to Professor Xia, Instructor Wang and Instructor Jiang who guided us through the implementation of this project.

# References
M. Sudipto, A. Himanshu, L. Eugene and K. Sreeram, “ClusterGAN: Latent Space Clustering in Generative Adversarial Networks” in Proc. of the AAAI Conference on Artificial Intelligence, vol. 33, pp. 111–117, 2019

R. Yang, D. Wang, Z. Wang, T. Chen, J. Jiang and G. Xia, “Deep Music Analogy Via Latent Representation Disentanglement”, in Proceedings of the 20th International Society for Music Information Retrieval Conference, Delft, The Netherlands, Nov. 2019, pp. 596–603.

M. Tasroc, “Mathematical equation for the sound wave that a piano makes,” Signal Processing Stack Exchange, 10-Apr-2020. [Online]. Available: https://dsp.stackexchange.com/questions/46598/mat hematical-equation-for-the-sound-wave-that-a- piano-makes. [Accessed: 15-Dec-2021].


