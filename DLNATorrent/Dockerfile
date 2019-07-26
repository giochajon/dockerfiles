# MiniDLNA and Transmission Daemon with web
from ubuntu:18.04
RUN apt-get update && apt-get install minidlna transmission-cli transmission-common transmission-daemon -y
WORKDIR /media

run sed -i s+"\\\/var\\\/lib\\\/transmission-daemon\\\/downloads"+"\\\/media"+g /etc/transmission-daemon/settings.json

run sed -i s+"127.0.0.1"+"127.0.0.1,*.*.*.*"+ /etc/transmission-daemon/settings.json

EXPOSE 9091
EXPOSE 8200

run sed -i s+media_dir=/var/lib/minidlna+media_dir=/media+g /etc/minidlna.conf

run sed -i s+#merge_media_dirs=no+merge_media_dirs=yes+g /etc/minidlna.conf




run echo friendly_name=DMediaServer >> /etc/minidlna.conf

run echo inotify=yes >> /etc/minidlna.conf

run usermod -a -G debian-transmission root

run chgrp -R debian-transmission /media

run chmod -R 775 /media

##run service transmission-daemon start


##run service minidlna force-reload




# en mera sudo ufw allow 8200

# docker run -it -p 9091:9091 -p 51413:51413 -p 51413:51413/udp -p 8200:8200 -v ~/media:/media --rm dlnatrans

# http://127.0.0.1:9091/transmission/web/



#CMD exec /etc/transmission-daemon/transmission.run
#USER debian-transmission
run service transmission-daemon reload


#service transmission-daemon start

#docker build --tag=dlnatrans .
#docker run -it -p 9091:9091 -p 51413:51413 -p 8200:8200 -p 51413:51413/udp  -v ~/media:/media --rm dlnatrans


#https://www.smarthomebeginner.com/install-transmission-web-interface-on-ubuntu-1204/
#https://www.smarthomebeginner.com/install-transmission-using-docker/

#https://mylinuxramblings.wordpress.com/2016/02/19/mini-how-to-installing-minidlna-in-ubuntu/

