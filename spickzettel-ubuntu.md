
# check if package is installed
* apt -qq list PACKAGE

# gnome-tweaks - issues with starting it
* first attempt to solve it
    * sudo nano /etc/apt/sources.list
    * add the following lines
        * deb http://security.kali.org/kali-security kali/updates main contrib non-free
        * deb http://http.kali.org/ /wheezy main contrib non-free
    * Now save it, press Ctrl + x press Y press enter
    * Back in the terminal
        * apt-get update
        * apt-get install gnome-tweak-tool
    * Now issue gnome-tweak-tool in the terminal and it should open.
        * error
            * ImportError: cannot import name '_gi' from partially initialized module 'gi' (most likely due to a circular import)
* second attempt to solve the issue    
    * cd /usr/bin/
    * rm python3
    * ln -s python3.6 python3
* now starting gnome-tweeks works
