# AITele

Program to generate desktop backgrounds for GNOME. Generates an initial background based on a user input. Program then feeds this image into AI image analysis to give an interpretation on the previously generated image. This interpretation is then used to generate a subsequent image and the cycle repeats...

Can use Open AI for [image generation](https://platform.openai.com/docs/guides/images/image-generation) and or [image processing](https://platform.openai.com/docs/guides/vision) so we can use the same API key. Could also split up to use a cheaper imager generator but may not be worth it. 

To start with, program will support GNOME desktop. Will abstract interaction with desktop layer so expantion to new operating systems will be simplified. Everything that deals with API calls and file system should be OS agnostic to start with. Will need installer to run process as Linux daemon using systemd for initialization (deamon will be per user unique, not root). 

Program will create a log of both past ~100 images as well as prompts used to create images. User will be able to set the time between desktop background updates and will default to once every 24 hours. 
