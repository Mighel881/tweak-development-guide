# setting everything up 
## so you've read the [intro](https://github.com/demhademha/tweak-development-guide/blob/master/intro.md) and you've made it to the first chapter!      well done !
## let's get started already!
# what we'll do in this chapter 
* Install a terminal application 
* Install a file manager
* connect to our device using ssh 
# Setting up the terminal 
So, a **terminal** is what allows us to communicate to our device,    its one of those black and white screens you normally associate with **hackers** (which you're becoming) well sort of..
Its necessary we have a terminal application otherwise, we won't be able to build our tweaks, nor will we be able to do other  very important things like collaborating on [github](https://github.com) (like google docs for coders,) or to test wether our bash scripts work. All in all, without a terminal, we can't do anything much. 
The terminal app that we are going to install works even in the jailed state (the unjailbroken state) providing us more functionality than others (such as newterm2) that only work when  you are jailbroken.) the terminal we are going to install is called "ish" and it emulates a  linux terminal on our device. 
# steps to installing ish:
1. Install TestFlight from the AppStore or visit [here](https://apps.apple.com/gb/app/testflight/id899247664) 
2. visit [here](https://www.google.co.uk/url?sa=t&rct=j&q=&esrc=s&source=web&cd=&ved=2ahUKEwjZjo2jx_rqAhUuQkEAHS6JBT4QFjADegQIAxAB&url=https%3A%2F%2Ftestflight.apple.com%2Fjoin%2F97i7KM8O&usg=AOvVaw1I9cM-8axRNb1XRvTgM7AA)
3. Tap on "accept" 
4. Tap on "install" 
5. open ish, and it will say "welcome to alpine"
Note: you may change the theme to black if you wish by tapping the settings button in ish
## You've done it, you've installed a terminal app on your device, time to move on
Ok, we need to install an application called **filza** as we will use this as our file manager.
## why not use the regular files app?
apple's files app doesn't give us access to the full file system of our device. Which means we need to use filza if we want to navigate our device's filesystem. In addition, filza is very easy to use. 
## steps to install filza. 
1. Open your package manager (I'll be using sileo)
2. Tap on "sources" 
3. Tap on "eddit" 
4. Tap on "add"
5. Insert the following url: "https://data.tigisoftware.com/cydia/"
6. Add the source 
7. Go to the source
8. Install filza (use normal filza and not the 64 bit version)
9. Open filza, and tap on name (this will arrange everything alphabetically)
### you've successfully installed filza, now time to connect to our device over ssh #
## Note: follow the jailbreak that applies to you:
## Checkra1n (not odysseyra1n)
1. Open "ish" 
2. Type "apk add openssh"
3. After it finishes, type "ssh localhost -p44"
4. it'll say "the authenticity of xxx can't be established" type "yes"
5. It'll say root@localhosts password
6. The default password is "alpine"
7. it'll now say your device name followed by the word root
8. You've successfully logged into your device using ssh

## unc0ver, chimera and  electra (devices not using the procursus bootstrap)
1. go to the cherries repo (added by default) and install "localssh" 
2. Install "openssh" (unc0ver users go to the bingner repo, electra and chimera jailbreak users go to the chimera repo)
3. Open settings, > tap the I icon next to the    wifi you are connected and remember the IP address, for example, 192.168.0.24 (yours might be different)  
4. Open ish, 
5. Type "apk add openssh"
6. After it finishes, type "ssh your IP address -p2222"
7. it'll say "the authenticity of xxx can't be established" type "yes"
8. It'll say something like root@your IP address   password: (mine is root@192.168.0.24)   
9. The default password is "alpine"
10. it'll now say your device name followed by the word root
11. You've successfully logged into your device using ssh

## procursus based jailbreaks (odyssey, odysseyra1n)

1. Install "openssh" (go to the procursus repo)
2. Open settings, > tap the I icon next to the    wifi you are connected and remember the IP address, for example, 192.168.0.24 (yours might be different)  
3. Open ish, 
4. Type "apk add "openssh"
5. After it finishes, type "ssh your IP address  -p2222"
6. it'll say "the authenticity of xxx can't be established" type "yes"
7. It'll say something like root@your IP address   password: (mine is root@192.168.0.24)   
8. The default password is "alpine"
9. it'll now say your device name followed by the word root
10. You've successfully logged into your device using ssh

## connecting from a laptop over wifi 
 1. Install "openssh" (you will need to know how to install this for your own os)
2. open "terminal" 
3. On the device, install openssh (see above for jailbreak specific instructions)
 4.Open settings, > tap the I icon next to the    wifi you are connected and remember the IP address, for example, 192.168.0.24 (yours might be different)
 5. type "ssh root@your IP address"
6. it'll say "the authenticity of xxx can't be established" type "yes"
7. It'll say something like root@your IP address  password: (mine is root@demhademha)   
8. The default password is "alpine"
9. it'll now say your device name followed by the word root
10. You've successfully logged into your device using ssh
## using ssh over usb 
1. Install [libimobiledevice](https://github.com/libimobiledevice/libimobiledevice) through your package manager, or compile it yourself
2. Connect your device via usb (make sure you don't have any other devices connected)
 3. open "terminal"
 4. Type "iproxy 2222 22
5. Open a new terminal and  type "ssh root@localhost -p2222" 
6. it'll say "the authenticity of xxx can't be established" type "yes"
7. It'll say root@localhosts password, the default is "alpine"
## Few, we’ve completed getting ish, installing filza and you now  know how  to connect using ssh! # 

## let's move on!
