# Tutorial -- Let's Chat

## Objectives

* Understand what is speech recoginition
* Know how to perform speech recognition on NAO
* Know how to set up threshold of speech recoginition

Anytime you have difficulty to read the interface of Choregraphe, please refer to the [interface graph in Tutorial 1](https://github.com/PaloAltoLibrary/NAO-Tutorials/blob/master/Tutorial%201/README.md#basics-of-choregraphe).


### Voice as a way to communicate

As a humanoid robot, some good ways to communicate with NAO are through touch and voice -- just like how humans. Isn't that cool?

But NAO does not hear with his ears, or talk with his mouth. What seem to be his ears at the side of his head are in fact his speakers, What seems to be his mouth is actually one of his eyes (one of the two cameras), What seem to be his eyes are mind control portals(infrared emitters), and his real ears(mic) are located on top of his head. What a camouflage! Good job, NAO.

<img src="readmeImages/mic.png" width=500 />

However, unlike our ears that listen for sounds all the time, NAO has to be programmed to listen for sounds at specific times. After it hears sound , NAO can perform speech recognition to convert what it hears into words that it knows.

In order to do this, we need to teach NAO some words or even a dictionary, so it can express what it hears in words. The Words can be as simple as "yes" and "no". Once it captures the word, we can further use conditional programming to ask nao to carry out new behaviors. 

For example, NAO asks "How are you feeling today?". If I answer "Yes", it will blink his ear LEDs. If I answer "no", it will blink his eye LEDs.### Speech Recognition in Choregraphe
The first thing to do as usual is to develope a new applilcation in Choregraphy. Click the <img src="readmeImages/new.png" width=20 /> ***new project button*** on the tool bar. This will open a new blank project. 

We will start a new program for a very simple task to make NAO hear and recognize two words, "yes" and "no". 

In choregraphe, look at the box libraries panel. Search and drag four boxes to the flow diagram panel:

* ***Speech Recognition***
* ***Set Language***
* ***Say***
* ***Twinkle*** (drag and drop two of these)

Next, we will configure the boxes a bit. 

Click the <img src="readmeImages/wrench.png" width=20 /> wrench button of the Speech Recognition box. By default, the word list is set to “yes;no”. The semicolons separate different words in the library. The default threshold is set to 30%. The robot won't recognize a word if it is not sure enough. If you want Speech Recognition to be more tolerant, you can decrease the confidence level number.

Double click the Say box, then in the "Localized Text" box, select the language to be "English", and in the input field, type in `Sorry, I do not understand`. We will use this box when NAO hear things it does not understand. 

Click `Root` on the top of the flow diagram panel to go back to the main view.

In the Switch Case box, enter `"yes"` with quotes in the first input field and `"no"` with quotes in the second input field.

Click both mouse buttons on the Twinkle boxes, a drop down menu will come up. Select the menu item "Edit box", and change one box's name to "Ear Twinkle", and the other one to "Eye Twinkle".

Finally, connect the boxes in the following way:

<img src="readmeImages/speech.png" width=500 />

 *Related Resource* <sup>[1](#1)</sup>

Click the the <img src="readmeImages/play.png" width=20 /> ***play button*** on the tool bar and see the result. If you are connecting to a virtual robot, you can double click the input buttons to mimick the behavior.

#### Exercise

1. Make NAO introduce itself when you ask it to.
2. Have NAO ask “How are you?” Depending on what you say, NAO should have different replies.
3. Use voice commands to control the robot. You can ask it to sit down, walk around, tell a joke etc..

---

<a name="1">1</a>: Download [SpeechRec](SpeechRec.crg) and open it in your Choregraphe.
