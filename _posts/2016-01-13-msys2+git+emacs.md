#Config msys2 + git (windows)

Thanks kelvin!

1. Install msys2
2. Config proxy for bash:
   1) Open ~/.bashrc
   2) Append proxy:
      export http_proxy=web-proxy.oa.com:8080
      export https_proxy=web-proxy.oa.com:8080
3. Update msys2:
   run "update-core"
4. Install Git
   run "packman -S git"
5. Install Connect
   run "packman -S connect"
6. Config Git proxy
   put the config file under ~/ssh


##git proxy config

ProxyCommand connect -H web-proxy.oa.com:8080 %h %p

Host github.com
User git
Port 22
Hostname github.com
TCPKeepAlive yes
IdentitiesOnly yes

Host ssh.github.com
User git
Port 443
Hostname ssh.github.com
TCPKeepAlive yes
IdentitiesOnly yes



