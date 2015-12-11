# docker-sikuli-novnc
Dockerfile for ubuntu + lxde + x11vnc + chrome + sikuli + novnc

From Docker Index
```
docker pull kkochubey1/sikuli-novnc
```

Build yourself
```
git clone https://github.com/kkochubey1/docker-sikuli-novnc.git
docker build --rm -t kkochubey1/docker-sikuli-novnc docker-sikuli-novnc
```

Run
```
docker run -i -t -p 6080:6080 kkochubey1/docker-sikuli-novnc

# Mac: Open browser on dockerhost IP port 6080
dockerhost_ip=$(docker-machine ip $(docker-machine active))
open 'http://'$dockerhost_ip':6080' 
```


Browse http://192.168.99.100:6080

<img src="https://raw.github.com/kkochubey1/docker-sikuli-novnc/master/screenshots/lxde.png" width=400/>


Test (Mac)
```
# Test sikuli edit script
./test/sikuli-edit.sh test/test.sikuli

# Test sikuli run script
./test/sikuli-run.sh test/test.sikuli
```


License
==================

desktop-mirror is under the Apache 2.0 license. See the LICENSE file for details.