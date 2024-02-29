# JammingWifiModule
A jamming Wifi Module For NS-3

This is an ns-3 module that can be used to perform simulations of a WiFi network.


## Getting Started
### Prerequisites

> system: ubuntu 16.04

1. install **ns-3.30.1** (Not tested on later versions, but it's certain that it won't work on versions after 3.36)

2. install [ns-3 gym, which suited for ns-3.30.1](https://github.com/tkn-tub/ns3-gym/tree/app)  to use and create Smart Mitigation method and Smart Attack (**cannot be skipped**).

### install the module

1. download the module **outside** the ns3 project
    ```
    git clone https://github.com/cflycloud/JammingWifiModule.git
    ```

2. copy the folder "jamming" into the `ns-3/src/`

	```
	cd JammingWifiModule
	cp -r jamming /your path to ns-3.30.1/ns-3.30.1/src/
	```

3. copy the follwing files into ` ns-3/src/wifi/model`

   ```
   interference-helper.cc
   interference-helper.h
   wifi-phy.cc
   wifi-phy.h
   wifi-preamble.h
   ```

### Compilation 

In the ns-3 folder compile and build the code

``` 
cd ns-3

./waf configure --enable-tests --enable-examples

./waf build
```

Finally, make sure tests run smoothly with:

```
./test.py -s jamming-components-test
```

If the script returns that the lorawan test suite passed, you are good to go. Otherwise, if tests fail or crash, consider filing an issue

### Licence

This software is licensed under the terms of the GNU GPLv2 (the same license that is used by ns-3). See the LICENSE.md file for more details.



