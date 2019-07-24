## Installation

You will need `libpcap` installed.  Most OSX machines seem to have it.  All major Linux distributions have it available
either by default or with a package like `libpcap-dev`.

The easiest way to get `node_pcap` and its tools is with `npm`:

    npm install pcap

If you want to hack on the source code, you can get it from github.  Clone the repo like this:

    git clone https://github.com/sieteunoseis/node_pcap.git

To compile the native code bindings, do this:
    
    npm install -g node-gyp
    cd node_pcap
    node-gyp configure build or node-gyp configure build --target=v11.12.0
    node-gyp rebuild --target=1.2.3 --arch=x64 --dist-url=https://electronjs.org/headers
    //replace target version with your version of electron

Assuming it built without errors, you should be able to run the examples and then write your own packet
capture programs.
