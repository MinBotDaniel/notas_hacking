### Scan Surprise

I've gotten bored of handing out flags as text. Wouldn't it be cool if they were an image instead?

You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_atlas/13/challenge.zip)

The same files are accessible via SSH here:

`ssh -p 58789 ctf-player@atlas.picoctf.net`

Using the password `f3b61b38`. Accept the fingerprint with `yes`, and `ls` once connected to begin. Remember, in a shell, passwords are hidden!
### Solución
┌──(kali㉿kali)-[~/Tareas]
└─$ ssh -p 58789 ctf-player@atlas.picoctf.net
The authenticity of host '[atlas.picoctf.net]:58789 ([18.217.83.136]:58789)' can't be established.
ED25519 key fingerprint is: SHA256:hVmbk/OaNT4902bBr7h26wfhmBuJWi4tub8AJqoAJCM
This key is not known by any other names.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[atlas.picoctf.net]:58789' (ED25519) to the list of known hosts.
** WARNING: connection is not using a post-quantum key exchange algorithm.
** This session may be vulnerable to "store now, decrypt later" attacks.
** The server may need to be upgraded. See https://openssh.com/pq.html
ctf-player@atlas.picoctf.net's password: 
Permission denied, please try again.
ctf-player@atlas.picoctf.net's password: 
                                                                  
SE ESCANEA EL QR CON EL CEL Y LISTO
picoCTF{p33k_@_b00_d4ca652e}
### Notas
