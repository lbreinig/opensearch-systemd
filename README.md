# opensearch-systemd

Files for using on CentOS and Fedora with systemd
Originally forked from Shellmaster/kibana4-systemd

- there are 3 files:

 - /etc/logrotate.d/opensearch-dashboards
 - /etc/systemd/opensearch-dashboards.service
 - /etc/rsyslog.d/opensearch-dashboards.conf


`/etc/systemd/opensearch-dashboards.service` is a very simple script after you copy the file then you need to enable it in systemd 

`systemctl enable opensearch-dashboards`

then copy rsyslog script to enable logging under `/var/log/opensearch-dashboards`

`systemctl restart rsyslog`

and you can finally start opensearch-dashboards

`systemctl start opensearch-dashboards`


