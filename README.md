Graphite
=================

graphite automation


generating graphite-web rpm:

```
# yum install ruby-devel gcc make rpm-build rubygems epel-release
# gem install --no-ri --no-rdoc fpm
# export PATH=$PATH:/usr/local/bin
# yum install gcc python-dev libffi-devel python-pip
# pip install --upgrade pip
# virtualenv /tmp/opt/graphite
# . /tmp/opt/graphite/bin/activate
# pip install Django cairocffi cffi django-tagging pycparser pyparsing pytz scandir six urllib3
# pip install --install-option="--prefix=/tmp/opt/graphite" --install-option="--install-lib=/tmp/opt/graphite/webapp" graphite-web

# /usr/local/bin/fpm -s dir -t rpm -n graphite-web -v 1.1.4 --description \
"Graphite is an enterprise-scale monitoring tool that runs well on cheap hardware. It was originally designed and written by Chris Davis at Orbitz in 2006 as side project that ultimately grew to be a foundational monitoring tool. In 2008, Orbitz allowed Graphite to be released under the open source Apache 2.0 license. Since then Chris has continued to work on Graphite and has deployed it at other companies including Sears, where it serves as a pillar of the e-commerce monitoring system. Today many large companies use it." \
-d cairo --prefix /opt/graphite -C /tmp/opt/graphite .

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
