<img src="https://avatars.githubusercontent.com/u/234659742?v=4" width="20%" /> PyBLOCK Bitcoin Node/Client/Wallet <img src="https://github.com/bitcoinknots/bitcoin/blob/29.x-knots/src/qt/res/icons/bitcoin.png?raw=true?v=4" width="20%" /> 


-----

sudo apt-get update

sudo apt-get upgrade -y

sudo apt-get install build-essential cmake pkgconf python3 git libevent-dev libboost-dev libsqlite3-dev libzmq3-dev libqrencode-dev imagemagick librsvg2-bin qtcreator libfontconfig1 qtbase5-dev qtchooser qt5-qmake qtbase5-dev-tools qttools5-dev-tools libgl-dev libglu-dev qttools5-dev qtdeclarative5-dev -y

git clone https://github.com/PyBLOCK-Bitcoin/bitcoin.git

cd bitcoin

mkdir build

cd build

cmake .. -DCMAKE_INSTALL_PREFIX="" -DBUILD_DAEMON="ON" -DBUILD_CLI="ON" -DBUILD_GUI="ON" -DAPPEND_CXXFLAGS="-O2" -DAPPEND_LDFLAGS="-flto"

cmake --build . --target install --parallel $(nproc)

cd bin

./bitcoin-qt

-----


<br />

License
-------
PyBLOCK is released under the terms of the MIT license.

See [COPYING](COPYING) for more information or see https://opensource.org/licenses/MIT.
