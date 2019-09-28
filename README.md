# ansible-netconf
ansible netconf playbook for default (non ios/junos) platform
--> configure/enables ospf through jinja2/source file
--> configure/enables ospf through content
--> Save the netconf full configuration file as xml

Notes:
python3 interpreter is used.
Using python2/2.7 often causes UCS2/UCS4 mismatch issues as ansible netconf/netconf_config module mainly uses python's ncclient.
To get rid off this issue, 

check python3 is using ucs4

python3
>>> import sys
>>> print sys.maxunicode
1114111

use pip3 to install ncclient.

#pip3 install ncclient

check ncclient is working with with python3.

#python3
>>from ncclient import manager
