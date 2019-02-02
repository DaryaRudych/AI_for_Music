# Music Generation with LTSM RNN
(Darya Rudych: data & modeling, 

![header image](https://i.ytimg.com/vi/WqE9zIp0Muk/maxresdefault.jpg)


## Objective
As a group of Austin-based music lovers, we got very upset when we heard Austin is no longer a music capital of the world. We decided to take the matter in our own hands and built a BeatBot capable of generating new music on demand (we're tech hub too, after all!). Extending the models used for generating text, we use it to generate notes/chords and evaluate its performance. 

## Model Choice

For this project we used CBLTSM RNN Model. The choise of the model was determined by the following considerations:
1. RNN models are best suited for sequential information as they perform the same function for every single element of a sequence, with the result being dependent on previous computations. 
2. LSTMs are extremely useful to solve problems where the network has to remember information for a long period of time as is the case with music. 
3. Character-based LTSM is specific to replicating patterns in text. Being a recurrent neural network it stores memory as it moves along learning patterns and understanding the concept of cause and effect. Music can be represented as text (notes ABC etc) which is convenient since text is lightweight and discrete which makes training fast. 
4. In addition, once CBLTSM is set up it can generate output indefinitely. There is no maximum length of generated music. 

## Data
1. For this project we are using scraped MIDI (Musical Instrument Digital Interface) files that contain information about note, pitch, octave, chord, offset
2. Music21 toolkit that allows to extract notes, chords, pitch from our data set.
3. Since MIDI files are not very common, for each of the genres we had different number of available MIDI files.

![Alt text](https://github.com/DaryaRudych/AI_for_Music/blob/master/DataTable.png)
