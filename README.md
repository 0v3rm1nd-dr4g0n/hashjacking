# hashjacking
All current versions of Windows are affected by an architectural vulnerability due to the presumptive nature of SMB authentication. Hashed credentials will secretly be sent in cleartext across the Internet. This attack vector is trivial to execute and has critical consequences. See proof of concept videos below.

The core of this issue is due to the presumptive nature of current SMB authentication methods. When a user accesses a file share or remote file, hashed Windows credentials from the current user are automatically sent to the remote server in cleartext in attempt to authenticate and access the remote file. The default behavior of assuming the remote server is trusted allows for systems to quickly access file shares in large corporations so that users won’t need to sign in with their company credentials each time to access network resources. However, this implementation presents a significant security risk to user accounts and passwords. *Read more on for the link below.

[Hashjacking: Anyone can steal your Windows password](https://www.praetorian.com/blog/hashjacking-anyone-can-steal-your-windows-password)

## Author
Written by Julian "hob0" Dunning ([@hob0man](https://twitter.com/hob0man))

##Proof of Concept Examples
###Email
![Email](https://raw.githubusercontent.com/hob0/hashjacking/master/email.gif)
###Direct Access With Chrome
![Direct with Chrome](https://raw.githubusercontent.com/hob0/hashjacking/master/Chrome.gif)
###Malicious image embedded in HTML
![HTTP](https://raw.githubusercontent.com/hob0/hashjacking/master/HTTP.gif)

