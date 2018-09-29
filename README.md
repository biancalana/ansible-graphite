Graphite
=================

graphite automation


generating graphite-web rpm:

```
# yum install ruby-devel gcc make rpm-build rubygems
# gem install --no-ri --no-rdoc fpm

# yum install gcc python-dev libffi-devel
# virtualenv /opt/graphite
# . /opt/graphite/bin/activate
# pip install Django cairocffi cffi django-tagging pycparser pyparsing pytz scandir six urllib3
# pip install --install-option="--prefix=/opt/graphite" --install-option="--install-lib=/opt/graphite/webapp" graphite-web

# /usr/local/bin/fpm -s dir -s dir -t rpm -n graphite-web -v 1.1.4 /opt/graphite

```


Role Variables
--------------



Example Playbook
----------------


License
-------

MIT

Author Information
------------------

Alexandre Biancalana (@biancalana)
