#### XX-Net-Linux 3.13.1
Mini version of [XX-Net](https://github.com/XX-net/XX-Net) for Linux user.

Usage: 

    git clone https://github.com/miketwes/XX-Net-Linux.git -b master

    #replace $HOME/pip2_lib/hyper/common/bufsocket.py with replace/bufsocket.py

    export PYTHONPATH=$PYTHONPATH:$HOME/pip2_lib
    sudo /etc/init.d/miredo start
    cd XX-Net-Linux/local && python2.7 proxy.py
    
    # chromium
    chromium --proxy-server="http://127.0.0.1:8087"
    
    # Firefox about:config
    network.proxy.type 1     
    network.proxy.http 127.0.0.1
    network.proxy.http_port 8087  
    
    #after terminate proxy.py
    
    find . -type f -name "*.pyc"  -exec rm {} \;
    pkill -9 python && pkill -9 python2 &&  pkill -9 python2.7
    sudo /etc/init.d/miredo stop

Note: all XX-Net related python2 libs are latest version and installed in $HOME/pip2_lib by pip2.
