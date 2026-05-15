### Ph4nt0m 1ntrud3r
A digital ghost has breached my defenses, and my sensitive data has been stolen! 😱💻 Your mission is to uncover how this phantom intruder infiltrated my system and retrieve the hidden flag.To solve this challenge, you'll need to analyze the provided PCAP file and track down the attack method. The attacker has cleverly concealed his moves in well timely manner. Dive into the network traffic, apply the right filters and show off your forensic prowess and unmask the digital intruder!Find the PCAP file here [Network Traffic PCAP file](https://challenge-files.picoctf.net/c_verbal_sleep/586d0206891cc683bae1160ad6b0e05d7e10e7b2df122c0441ab06581038dd32/myNetworkTraffic.pcap) and try to get the flag.

### Solución
┌──(kali㉿kali)-[~/Tareas]
└─$ tshark -r myNetworkTraffic.pcap -Y "tcp.len > 0" -T fields -e frame.time_epoch -e tcp.segment_data | sort -n | awk '{print $2}' | xxd -p -r | base64 -d
tshark: Error loading table 'TLS Decrypt': ssl_keys:5: File '/home/kali/problemasPICO/webnet1/picopico.key' does not exist or access is denied.
���@�}7uW�ס��=<�T�l9��  �|��o�ڂ E��i�▒�G        [.��i�  7����^�B�œ<��Hv�<]�picoCTF{1t_w4snt_th4t_34sy_tbh_4r_f318db22} 


picoCTF{1t_w4snt_th4t_34sy_tbh_4r_f318db22}

### Notas
