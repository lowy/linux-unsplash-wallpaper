#!/bin/bash
WORKDIR="$HOME/Wallpaper/"
RANT=$(date +%s)

wget -q --spider https://www.bing.com
if [ $? != 0 ]; then
	exit
fi

if $DO_WE_ERASE_FILES
then
	rm $WORKDIR*'.jpg'
else
	mv $WORKDIR*'.jpg' $WORKDIR'old/'
fi
wget -O ${WORKDIR}${RANT}'.jpg' -q https://source.unsplash.com/1600x900

#gsettings set org.gnome.desktop.background picture-uri 'file://'${WORKDIR}${RANT}'.jpg'

#xfce4
xfconf-query -c xfce4-desktop -p /backdrop/screen0/monitor0/workspace0/last-image -s ${WORKDIR}${RANT}'.jpg'
