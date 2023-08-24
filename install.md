### dependancy here
```
apt install build-essential gcc libssl-dev libspeexdsp-dev cmake mlocate -y
```

```
cd /usr/src/
git clone git@github.com:romonzaman/mod_audio_stream.git
cd mod_audio_stream/
cd libs/
mv IXWebSocket IXWebSocketx
git clone git@github.com:machinezone/IXWebSocket.git
cd IXWebSocket
git checkout dfa10df5ae
cd ../

mkdir build
cd build/
cmake -DCMAKE_BUILD_TYPE=Release ..
make
make install
```

```
fs_cli-> load mod_audio_stream
```

```
uuid_audio_stream <uuid> start <wss-url> <mix-type> <sampling-rate> <metadata>
```
