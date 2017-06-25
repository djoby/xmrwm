# XMR Wolf Miner - xmrwm

```
NOTE: Wolf's XMR Miner is no longer maintained - please use https://github.com/genesismining/sgminer-gm.
```

## Requirement 

```
gcc 5 or newer
```

## Dependencies

```
sudo add-apt-repository ppa:ubuntu-toolchain-r/test -y && \
sudo apt-get update && \
sudo apt-get install gcc-6 g++-6 libjansson-dev -y && \
sudo update-alternatives --install /usr/bin/gcc gcc /usr/bin/gcc-6 60 --slave /usr/bin/g++ g++ /usr/bin/g++-6
```

## Building and running

```
make clean && make
./miner xmr.conf
```

## Sample Conf

```
olag@barmv8-01:~$ cat xmrwm/xmr.conf
{
  "threads": 3,
  "pools":
  [
    {
      "url": "stratum+tcp://xmr-eu1.nanopool.org:14444",
      "user": "<xmr address>.xmrwm-01",
      "pass": "x"
    },
    {
      "url": "stratum+tcp://xmr-eu2.nanopool.org:14444",
      "user": "<xmr address>.xmrwm-01",
      "pass": "x"
    }
  ]
}
olag@barmv8-01:~$ 
```

