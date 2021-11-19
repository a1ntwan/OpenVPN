First of all, if you want everything to be fine, you do definitely need to:
1) Turn off or set to permissive SElinux/apparmor;
2) Turn off or allow required ports in your firewall settings;
3) Make sure you time is synchronized on all of you nodes;
4) Your locale settings are configured properly.

This is simple **OpenVPN 2.4** config, which includes: 
 - server installation and basic configuration;
 - iptables most basic rules (server);
 - CA and server certificate files creation; 
 - OpenVPN key and DH key creation (may take some time);
 - client keys creation;
 - client config files creation;
 - fetching client configs from server and copying them to clients.
 
You may need extra ansible-galaxy collection to work with certificates:
```
ansible-galaxy collection install community.crypto
```

These playbooks have been tested on **Centos7** and **Ubuntu 20.04**.