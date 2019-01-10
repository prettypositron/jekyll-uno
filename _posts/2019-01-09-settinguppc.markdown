---
title:  "Setting up the new PC"
date:   2019-01-09 17:52:25
categories: [software]
tags: [software, setting up]
---

It's interesting that I scarcely understood Python two years ago, but have picked up whatever language I had to in the years since. What started off as a fear of learning new things compounded by my peers being so ahead of me, turned into a cybernetic existence in which I feel all too comfy to be in. Afterall, I learned HTML and CSS from right clicking and hitting "view source" on Dragonball Z websites since I was 12 years old. What seemed to come naturally to me at that age, in addition to building a PC, I only learned in later years was not very normal. I still find it baffling that my peers who have degrees in Computer Science do not know how to format a computer, or how to pirate media, or how to navigate the dark web, or how to use a private VPN. 

Anyway, since I'm new to markdown, let me try making a list. Let me throw in a header as well.

#### After the hardware has been set up

1. You will need an **operating system.** Go to a bay that harbors individuals of the "Arrrr.." variety, and you will be able to obtain a ~3GB ISO of Windows 10 Professional 64-bit in <10 minutes. Take a USB stick, you probably have a bunch lying around that were given to you for free as some kind of promotion, format it and create a bootable ISO using some archaic program like PowerISO which you can get for free online on their website. Stick that badboy in, and get that OS installed. If you want to be *cool* you can just get a Linux distro, but I prefer not to waste my time. 

2. Now's time to download and install your drivers. Let me try to make a sub-list.
  * First go to your motherboard's website, and download all of the necessary drivers, especially the **BIOS Update**. This can scare certain people, but not me because ~~I have reduced gray matter in my amygdala,~~ as long as you keep your computer running while the BIOS is being flashed, you are in the clear. Aside from stupid human error like tripping over the power cable, your PC can turn off unexpectedly if it overheats. When I first set up my PC (last night), I noticed my CPU temperature was at 67°C and climbing all the way to 115°C!!! It shut off on its own, but it was just an issue with loose wiring on the liquid CPU cooler. Anyway, download and install the drivers for your graphics card, for your everything else. 
  * If you're smart, you probably have an SSD for your OS and a standard HDD for storage. So start by changing default folders to save on the HDD, for example the "Downloads" folder. Make sure everything is running smoothly and that all of your hardware is being recognized by your BIOS. I actually didn't realize that my PC only recognized half of my RAM (16GB out of the 32GB) because I had to put it in some inane arbitrary order. 
  * Once you have everything squared away, it's probably a good time to benchmark your PC and see the monster within. Do this for each component in an isolated fashion. For instance, run 3D Mark to benchmark your GPU but make sure you're not playing a video game or something while it's running the benchmark. Do this with PC Mark for the PC. There's a variety of other benchmarking software out there, so what I like to do is try them all out and save a pdf of the results in a folder somewhere. Might as well check your internet speed too while connected via LAN on Ookla. I tend to get ~70Mbps DL speed and like 40Mbps UL speed which is actually not bad. It *IS* bad compared to what I just ran right now at a computer at NYU: 814.61 Mbps DL and 826.87 Mbps UL. Ping is also 3ms, compared to 10ms that I get at home. 
  
3. Now comes the actual purpose of this PC, which is to use it as a deep learning rig. Not, contrary to what most think, to download the Mass Effect Trilogy with the latest texture mods ~~which I actually did right after building this PC.~~ 
  * Let me start by saying, **FUCK PIP**
  * Pip is a tool for downloading Python packages, except it is grossly inferior to (ana)conda, and using both will lead to much confusion as you will end up with a certain version of a package from pip and another version from conda, making you want to just pour thermite on your laptop and/or nuke it from orbit. Now, **conda** is far more than a tool for downloading simply python packages. You can use it to download packages in R, Ruby, Java, C/C++, and many more. It's also capable of running virtual environments. 
 * Use command prompt (or terminal if you're on a Mac) to download conda and install your packages through there. Do not bother downloading Python elsewhere. Speaking of command prompt, I'd like to introduce you to Powershell.
 
#### I highly recommend you print out some cheatsheets for remember commands

4. Back to PowerShell. I'm not going to talk about the ISE, because on my last computer (my trusty Thinkpad T450S), it would always freeze up. So I really only use the console, which is essentially like the command prompt but smarter. OH, I almost forgot:

#### Run everything as Administrator. Sometimes being the 'Administrator' isn't enough. I have programs like PowerShell automatically open as administrator. 

But back to why it's so much smarter than standard cmd. Well, you can run batch commands which I think of as 'objects' but I know that isn't precise enough because that is the foundation of C (object-oriented programming). All I know is that I don't have to download imagemagick to resize 30 images at once, and can do several large operations with a single script rather than manually one-by-one like in cmd. 

#### Basically the thing about PowerShell is that it transitions you into scripting, that is automating, processes instead of doing things one by one in a command prompt.

5. What's a good text editor for code, markup, and prose?!

#### It's NOT Notepad++. 

I've used Notepad++ for some time, but it's not my thing. I prefer Sublime Text. It's actually what I used to make this website, although at the moment I am on a Mac on the NYU Campus using TextWrangler. It's wonderful to use Sublime because you can open entire folders and work on individual files within subfolders. It works with any language, really, and it's color-coded which is something that I really like. On the far right, you will see your code but zoomed out and vertical, allowing you to have a larger grasp of it all. It's certainly my go-to when I am coding. 

#### Let's get to the real stuff. Machine Learning. Where to begin?!

6. Fortunately, the apps that we use have wonderful tutorials and instructions on their websites. For instance, Tensorflow and Keras. After half a year of running CNN's on single-CPU decade old computers, I simply cannot wait to install the GPU version of TensorFlow on my new rig. I should also say this before I forget:

#### Set things that you use frequently, like Python and Tensorflow, to your PATH. 
You don't want to 'cd' into some convoluted folder structure every single time. There are also a LOT of packages to install. Some obvious ones are numpy, pandas, scipy, etc etc etc. I can't tell you how many times I had to shut down Jupyter Notebook only because I hadn't installed a package I needed to import in the first line. OH yeah, Jupyter Notebook, that's a given. It's an online text editor, well it's more of a notebook, that enables you to run each line of code after inputting it. It's open-source and meant to be freely shared throughout the community. All of the ML work I've done, other than that I had to do using Matlab, was done on Jupyter Notebook. 

#### Concluding remarks and some theory to think about

7. I am not going to talk much about machine learning in this post just yet. But there are a few important theoretical concepts in probability that form the foundation of much of the approaches we take in ML. 

 * Markov Chains - well, really just a random walk in a state space (finite) that satisfies the Markov Property, which means that if you wish to predict where the chain will be at a future time, if we are given the present state, then the entire past history is irrelevant. Given the present, the past and future are conditionally independent
 
 * Bayes' Theorem - really, Bayesian inference, is very different from the works of Markov in that you update the probability for a hypothesis as more evidence/information becomes available. 

---

I'm off, I have to read up on Bioinformatics for a job interview coming up. Lots of stuff about histones. Fun. 
