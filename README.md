## RNN Text generation

Simple text genartion model using Recurrent Neural Networks and LSTM cells written in Python with Tensorflow (tested on v1.4). 

Model was trained on various metal lyrics, including The Black Dahlia Murder, Arch Enemy, Cannibal Corpse, Dethklok etc. and
produced some very interesting results. Nevertheless, the code should work with any custom input so feel free to play around.
More on that in the usage section below. The model works on the char-by-char basis, rather than word by word. As visible from the
sample below, RNN learn English and the idea behind metal very well ;) More samples available in sample.md

Feel free to use the pretrained weights available in ckpt folder. You can either play around with those or train them further. However, keep in mind that these will only generate metal lyrics, so if you want something different you might need to retrain the whole model.

## Sample output:

terror the seeds of silent, we've on the seed of the one that i see
<br>the seed of our sacrifice the skin
<br>the burning heats
<br>and we are the tribulation within this world with blood
<br>and the story of their dead are
<br>slaughtered by the dead
<br>the bones of the strongest will sure
<br>the skulls of the storm
<br>the soul will all the strike
<br>one that i seek to the world of the storm
<br>we're the ones of the dead and soul with the dead
<br>and the shadows of the dead and the strong will remain
<br>strains the blood of the soul
<br>incisination and the stars
<br>we are the shadow of the strong
<br>well we are one
<br>we are the sky
<br>and the sword of the dead in hell
<br>sheep inside my head one with the floshes of the soul
<br>and the strendt of the dead,
<br>the dead cold be one with the pain
<br>stretch of the dead on the storm
<br>that is worth of flesh they shed their flesh
<br>there will be the one to thing today
<br>see them all die
<br>i am the strength
<br>to the tree of horror i will be the one to made this war
<br>welcome to the corpse of the strength of conscion fragment

## Usage:
1) Copy or download the rnn.py code. 
2) Hyperparameters can be adjusted inside the *if __name__ == 'main':* statement at the bottom of the code
3) The function of all of the hyperparameters are nicely commented in the code iteself. I won't go too much into details of RNN specific
hyperparameters, as there are countless blogs doing better job at explaining that than I could ever have done. Nevertheless, here 
are some useful custom options I've decided to add to the code to 'visualize' the training. Those include the following:
<br> - *log_step* - logs the progress to the console after specified training step
<br> - *sample_step* - generates a sample at the specified training step
<br> - *sample_text_size* - how many characters should the sample have 
<br> - *save_step* - saves the model after specified amount of steps
<br> - *first_sequence* - first sequence from which the model will predict the next characters in the sample step. Set to whatever fits your data
4) You can train the model on your own data by changing line 264 in the code: *PARAMS = preprocess_data(PARAMS, 'YOUR_OWN_DATA.txt')*
5) Run from console with commands listed below. If you have trained the model before and want to continue training using those weights, set *restore=True*
<br> - *python rnn.py train*
<br> - *python rnn.py sample*

**
If you have any questions or ideas how to improve the model, feel free to contact me.
