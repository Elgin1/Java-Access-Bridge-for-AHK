# Java Access Bridge wrapper for AutoHotkey and JControlWriter #

The Java Access Bridge for Windows is an API provided by Oracle to use the accessibility features of Java-Swing GUIs (http://www.oracle.com/technetwork/articles/javase/index-jsp-136191.html). This repository contains wrappers for this API to use the Java Access Bridge from AutoHotkey.

The files in this repository are:
JavaAccessBridge.ahk		A function based wrapper for the Java Access Bridge
JavaAccessBridge_class.ahk	A class based wrapper for the Java Access Bridge
JControlWriter.ahk			A browser for accessible controls in Java applications
JAB Swingset3 Demo.ahk		A demo how to use the JAB with SwingSet3.jar (various download locations)
JCWGUIStrings.ini			The GUI-strings for JControlWriter


## How to use ##

Before you can access Java applications through the Java access bridge you need to enable or install (for Java SE 7 Update 5 or earlier) the Java Access Bridge first. Instructions can be found here
http://www.oracle.com/technetwork/articles/javase/index-jsp-136191.html

To get an overview of which accessible information is published by your Java application you can use JControlWriter.ahk. With your Java application as active window press either Ctrl-Alt-F10 or Ctrl-Alt-F11 to show a list of the accessible controls.


## Known issues ##

- not all functions are wrapped yet; see comment section at the end of JavaAccessBridge.ahk
- Java applications can sometimes behave strangely. For instance when you use an action to call a function that opens a dialog, this call may not return until the dialog is closed again, effectively freezing your script. Use the "left click" action in those cases.

