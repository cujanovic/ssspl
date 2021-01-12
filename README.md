<a href="https://www.buymeacoffee.com/cujanovic" target="_blank"><img src="https://cdn.buymeacoffee.com/buttons/v2/default-yellow.png" alt="Buy Me A Coffee" style="height: 60px !important;width: 217px !important;" ></a>

# ssspl

***
### NAME

sss.pl - Simple SOCKS5 Server for Perl


### DESCRIPTION

SSS is a Simple SOCKS Server written in perl that implements the SOCKS v5 protocol.

It will accept username/password authentication.

The script runs in the background as a daemon.


### HISTORY

Originally I was looking for a simple SOCKS5 Server (with user/pass auth) that would run as a non-root user on FreeBSD.

I checked the FreeBSD ports for various SOCKS5 solutions and tried them all, only to discover that each one had a reason why it would not work, or why I could not use it.

I figured this could be done in perl, but found that there was no well maintained perl based solutions.

I hacked together this solution (with help from public domain scripts) and cleaned it up, ready for release.

Its simple, a feature I intend to maintain, however there is scope for much more potential, especially with user feedback.

You can read the full story here: http://www.hm2k.com/posts/freebsd-socks-proxy-for-mirc


### INSTALL

  wget http://ssspl.svn.sourceforge.net/viewvc/ssspl/sss.pl
  chmod 755 sss.pl

OR

  http://ssspl.svn.sourceforge.net/viewvc/ssspl.tar.gz?view=tar
  tar zxvf ssspl.tar.gz
  chmod 755 ssspl/sss.pl

### USAGE

You run the script using the following command:

./sss.pl <local_host> <local_port> [auth_login(:auth_pass)] Note: the auth_pass must be an md5 (hex) hash eg: 

./sss.pl hostname.example.com 34567 test:ae2b1fca515949e5d54fb22b8ed95575

Once up and running you can use the server in mIRC using the following command: 

/firewall [-cmN[+|-]d] [on|off] <server> <port> <userid> <password> For more information on this command issue: 

/help /firewall in mIRC. eg: /firewall -m5 on hostname.example.com 34567 test testing


### PREREQUISITES

Operating System: Tested on FreeBSD 6.x and CentOS 4.x, should work on others.

Required modules: IO::Socket::INET, Digest::MD5.

http://ssspl.sourceforge.net/

***

<a href="https://www.buymeacoffee.com/cujanovic" target="_blank"><img src="https://cdn.buymeacoffee.com/buttons/v2/default-yellow.png" alt="Buy Me A Coffee" style="height: 60px !important;width: 217px !important;" ></a>
