## RNN Text generation

Simple text genartion model using Recurrent Neural Networks and LSTM cells written in Python with Tensorflow (tested on v1.4). 

Model was trained on various metal lyrics, including The Black Dahlia Murder, Arch Enemy, Cannibal Corpse, Dethklok etc. and
produced some very interesting results. Nevertheless, the code should work with any custom input so feel free to play around.
More on that in the usage section below. The model works on the char-by-char basis, rather than word by word. As visible from the
sample below, RNN learn English and the idea behind metal very well ;) More samples available in sample.md

Feel free to use the pretrained weights available in ckpt folder. You can either play around with those or train them further. However, keep in mind that these will only generate metal lyrics, so if you want something different you might need to retrain the whole model.

## Sample output:

cannibalize the masters
<br>of his lost
<br>disemboweled fires
<br>bright and crossve of the reality on top of the power
<br>until the only things that should not a rige
<br>when life shades to the one that weals
<br>a face of life we're deface of the dead
<br>slaughter out the souls of my bloodied fate
<br>the spenches of hell is on the blood
<br>and their insane with blood
<br>so we shed our souls will be defe
<br>and the secret of destruction
<br>the beast in the stars and stretched on to your world
<br>they're all die
<br>will ther will befill their to decay
<br>see the touch of mortals will be dead
<br>the season of the touch of death
<br>in a pay the corpus of his flesh
<br>the blood of our end
<br>all the brown in the dead
<br>and the devoss the expure from the other side
<br>i would want is the pain
<br>with a savage beauty
<br>for sure burn i've been bestowed in my soul
<br>severed my heart
<br>i see the darkness in my face of flesh
<br>i will before you with blood
<br>you wnal the strength to find the shame
<br>the truth is of your name of life
<br>and it all belongs to feed of your own inside

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
