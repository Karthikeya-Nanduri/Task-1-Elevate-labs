1) Installing Nmap from website -- I have done this task in my kali linux environment. So I have run a command to install nmap ( It will already be installed in the latest version of kali).
     COMMANDS --  sudo apt-get install nmap
                  sudo apt-get update

2) Finding my local IP range -- I have used a command which gives my ip range along with its subnet mask.
   COMMAND --   ip a
    MY IP - 10.0.2.15
    MY SUBNET MASK - 24
   (10.0.2.15/24).

3) Nmap scan for my IP -- I have scanned my ports and ip range to observe which ports are open and what are running on them currently.
   COMMAND --   nmap -sS 10.0.2.15/24

4) IP addresses and Open ports : 3 ip hosts are up and 9 ports are open.
            IP -- 10.0.2.2 , 10.0.2.3 , 10.0.2.15
            OPEN PORTS -- 135,445,1042,1043,1234,5432,7778,8080,8090

5) Analyzed packet capturing with wireshark
      Filters used -- tcp.flags.syn == 1 && tcp.flags.ack == 0
                     ip.addr == 10.0.2.2
                     tcp.flags.syn == 0 && tcp.flags.ack == 1

6) Researched what are the common services that are running on the active ports -- Detailed explanation is there in the word doc attachment file with number 6.

7) Identified and analysed what could be the potential security risks from the ports that are open -- My views are in the doc number 7 that is attached above.

8) Downloaded my wireshark scan result from the wireshark app in my kali linux. ***(PLEASE VIEW WITH RESPECTED APP AS IT IS IN THAT FORMAT)***.
