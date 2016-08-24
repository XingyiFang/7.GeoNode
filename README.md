# 7.GeoNode

1. download ubuntu-14.04.ios
2. install oracle VM
3. install ubuntu-14.04 on VM
4. change resolution - first, 'sudo apt-get remove libcheese-gtk23', then 'sudo apt-get install xserver-xorg-core' and 'sudo apt-get install -f virtualbox-guest-utils virtualbox-guest-x11 virtualbox-guest-dkms'
5. install geonode

##steps
    1 sudo apt-get install apache2 gcc gdal-bin gettext git-core libapache2-mod-wsgi libgeos-dev libjpeg-dev libpng-dev libpq-dev libproj-dev libxml2-dev libxslt-dev openjdk-7-jre patch postgresql postgis postgresql-9.3-postgis-scripts postgresql-contrib       python python-dev python-gdal python-imaging python-pastescript python-psycopg2 python-support python-urlgrabber python-virtualenv    unzip zip
    2  sudo apt-get install gdal-develop
    3  sudo apt-cache search gdal
    4  sudo apt-get install libgdal-dev
    5  ls
    6  mkdir geonode
    7  cd geonode/
    8  virtualenv --no-site-packages env
    9  . env/bin/activate
   10  git clone https://github.com/GeoNode/geonode.git
   11  ls
   12  cd geonode/
   13  git fetch --tags
   14  git checkout 2.4 -b 2.4
   15  git branch 
   16  git log
   17  ls
   18  gdalinfo --version
   19  pip install pygdal==1.10.1
   20  ls
   21  pip install -e .
   22  ls
   23  python manage.py syncdb
   24  paver setup
   25  paver start
