# startup and security

Minecraft has some poorly-explained "security" fix every few months. That 
worries me.

You can mitigate some of that craziness by running minecraft java instances
from a script that is constrained by Linux's apparmor.

Install these files in the appropriate locations. Then,

{{
$ sudo apparmor_parser -a /usr/local/bin/minecraft-server
$ sudo apparmor_parser -a /usr/local/bin/minecraft-client
$ sudo aa-enforce /usr/local/bin/minecraft-server
$ sudo aa-enforce /usr/local/bin/minecraft-client
}}
