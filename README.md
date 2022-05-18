# Envelope Follower

  

6 March 2022

Created for Project 2 of CIS 422 at the University of Oregon

  

Arden Butterfield

Zacree Carroll

Ethan Killen

Stephen Leveckis

Patrick Thomasma

  

# CONTENTS OF THIS FILE

----------------------

  

[1. Install Instructions](#Install-Instructions)

  

[2. Operation Instructions](#Operation-Instructions)

  

[3. Dependencies](#Dependencies)

  

[4. File Manifest](File-Manifest)

  

[5. Known Bugs and Fixes](#Known-Bugs-and-Fixes)

  

[6. References](#References)

  
  

## 1. INSTALL INSTRUCTIONS

-----------------------

Drag EnvelopeFollower.component to

~/Library/Audio/Plug-Ins/Components -OR- open

EnvelopeFollower/EnvelopeFollower.jucer with Projucer, click save

and open in IDE, and then build as AU. See EnvelopeFollowerDemo.mp4

or Installation_Instructions.pdf for more details.

  
  

## 2. OPERATIONS INSTRUCTIONS

-----------------------

Open Logic Pro and create a new track. Add an instrument or audio

file. In the Audio FX slot, add the Audio Unit EnvelopeFollower,

manufactured by AlternativesConsidered. While the track is playing,

the effect will send out MIDI CC messages, which can be learned to

another parameter using Logic’s learn command.

See EnvelopeFollowerDemo.mp4 or User_Documentation.pdf for more

details.

  

## 3. DEPENDENCIES

-----------------------

The plugin software relies on:

  

3.1 JUCE 6.1.4 or higher (https://juce.com/get-juce/download)

3.2 Logic Pro 10.4 or higher (https://www.apple.com/logic-pro/)

  

## 4. FILE MANIFEST

-----------------------

This directory contains a number of PDF files, describing the

  

SRS.pdf

SDS.pdf

Project_Plan.pdf

README.txt

Programmer_Documentation.pdf

Installation_Instructions.pdf

User_Documentation.pdf

EnvelopeFollowerDemo.mp4

EnvelopeFollower.component

EnvelopeFollower/

EnvelopeFollower.jucer

Assets/

Inversionz.otf

coolBackground.png

knob1.png

Source/

PluginProcessor.cpp

PluginProcessor.h

PluginEditor.cpp

PluginEditor.h

CustomKnobs.cpp

CustomKnobs.h

SignalProcessor.cpp

SignalProcessor.h

  

## 5. KNOWN BUGS AND FIXES

-----------------------

  

(MacOS 10.5+) Unidentified Developer Error

  

Occasionally, MacOS users on OS software version 10.5 or greater

will encounter an “Unidentified Developer” error with the plugin

software if the user did not compile it on their machine with JUCE.

This can be fixed by going to System Preferences > Security >

General and click the “Open Anyway” button next to a prompt

explaining that the plugin software was blocked. A development fix

has not been found for this other than becoming authorized

developers via the App Store,which is outside the scope

of this project.

  

Envelope Visualization Can Be Hard to See

The green visualization of the envelope is very faint and hard to

see, especially at higher recovery values. At higher gain settings,

the green line may actually clip outside of the bounds, and not be visible.

  

MIDI CC Messages Sometimes Fail to Send

On occasion, the plugin will open and the knobs and visualizations will work as normal, but the MIDI CC messages will not be sent correctly. The cause of this bug is still unknown.

  
  
  

## 6. REFERENCES

-----------------------

Juce AudioProcessor Class Reference @

[https://docs.juce.com/master/classAudioProcessor.html](https://docs.juce.com/master/classAudioProcessor.html)

Juce AudioEditor Class Reference @

[https://docs.juce.com/master/classAudioProcessorEditor.html](https://docs.juce.com/master/classAudioProcessorEditor.html)
