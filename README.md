wget -qO- "https://cmake.org/files/v3.18/cmake-3.18.6-Linux-x86_64.tar.gz"|sudo tar --strip-components=1-xz -C /usr/local
apt-get update &&\

apt install -y clang-format-10 clang-tidy-10
apt-get install -y g++ gcc make lcov libtool m4 autoconf automake ccache libssl-dev zlib1g-dev libboost-regex-dev libboost-program-options-dev libboost-system-dev libboost-filesystem-dev libboost-serialization-dev python3-dev libboost-python-dev libcurl4-openssl-dev gfortran libtbb-dev pkg-config bison
 
curl -s -S -L https://raw.githubusercontent.com/moovweb/gvm/master/binscripts/gvm-installer | bash
source ~/.gvm/scripts/gvm
gvm install go1.18 -B
gvm use go1.18 -default
apt autoremove cmake-data libjsoncpp1 librhash0
apt install libaio1 libgoogle-perftools4 libtcmalloc-minimal4 libunwind-dev libunwind8
apt install gnupg2 libaio-dev libaio1 libgoogle-perftools-dev libgoogle-perftools4 libtcmalloc-minimal4 libunwind-dev
apt-get upgrade libunwind8
pip3 install conan==1.58.0
https://zhuanlan.zhihu.com/p/625626785
conan install aws-c-event-stream/0.2.12
apt-get install libblas-dev
export BLAS_DIR=/path/to/blas/library
apt-get install liblapack-dev
export LAPACK_DIR=/path/to/lapack/library
 
cd milvus
./scripts/install_deps.sh
make VERBOSE=1
