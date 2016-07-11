# kibana4-systemd

These are my files that I am using on CentOS and Redhat with systemd

Directory structure:

/
└── etc
    ├── logrotate.d
    ├── rsyslog.d
    └── systemd
        └── system


- there are 4 files:

/etc/logrotate.d/kibana
/etc/systemd/kibana.service
/etc/motd
/etc/rsyslog.d/kibana.conf


/etc/motd is just for fun, you know accountants.. like to 'see' things :-)

/etc/systemd/kibana.service is a very simple script after you copy the file then you need to enable it in systemd 

`systemctl enable kibana`

then copy rsyslog script to enable logging under `/var/log/kibana`

`systemctl restart rsyslog`

and you can start kibana

`systemctl start kibana`

if it is a fresh installation then you might need to fix weird permissions after 'optimize':

`chown kibana:root /opt/kibana/optimize/.babelcache.json`


Good Luck!
