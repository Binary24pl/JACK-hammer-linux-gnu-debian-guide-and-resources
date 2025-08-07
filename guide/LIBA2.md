# Assumptions:
I will assume that you followed my recomendations in regards of JACK root folder location.

# 32 bits

Install required files through apt-get.
 ```sh
sudo apt-get install libaudio2:i386
 ```

 Then go to your user library directory for 32 bit architecture.
 ```sh
cd /usr/lib/i386-linux-gnu
 ```

 Then you may copy the file to your JACK root folder.
 ```

cp libaudio.so.2 ~/JACK/
 ```

 # 64 bits

Install required files through apt-get.
 ```sh
sudo apt install libaudio2
 ```

 Then go to your user library directory for 64 bit architecture.
 ```sh
cd /usr/lib/x86_64-linux-gnu
 ```

 Then you may copy the file to your JACK root folder.
 ```

cp libaudio.so.2 ~/JACK/
 ```