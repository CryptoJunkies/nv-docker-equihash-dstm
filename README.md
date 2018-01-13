# nv-docker-equihash-dstm [![Build Status](https://travis-ci.org/CryptoJunkies/nv-docker-equihash-dstm.svg?branch=master)](https://travis-ci.org/CryptoJunkies/nv-docker-equihash-dstm)
[Image on Docker Hub](https://hub.docker.com/r/cryptojunkies/dstm/)

Dockerfile to build cryptojunkies/dstm GPU container for mining Equihash based crypto currencies.

## Pre-requisites

Requires a working installation of Docker CE or EE and Nvidia-Docker2 and at least one NVidia GPU of course.

## Installation

docker build -t cryptojunkies/dstm ./build

## Usage

docker run --runtime=nvidia -e "NVIDIA_VISIBLE_DEVICES=0" cryptojunkies/dstm "--server mypool.net --port 1234 --user myuername --pass x"

## Contributing

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request :D

## History

2018-13-01
Initial creation and build by CultClassik

## Credits

TODO: Write credits

## License

TODO: Write license