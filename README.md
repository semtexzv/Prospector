
# Prospector - Ethereum, Siacoin, Signatum, Monero and Zcash miner
Multi-algorithm cryptocurrency miner. This miner can utilize all resources provided by your mining rig. It mines on all your CPUs and GPUs. Currently, this miner is in alpha stage.
List of supported coins and pools is available at: [Pools page](https://github.com/semtexzv/Prospector/wiki/Supported-pools)


# Hashrates
Miner achieves hashrates, that are competitive with other miners.

measured:

    ETH GTX 1070 OC - 30 MH/s
    ZEC GTX 1070 OC - 380 - 400 SOL/s
    SIGT GTX 1070 Stock - 18.2 MH/s
    SIGT RX 480 19.8 MH/s (faster than sgminer)
    
    XMR Intel i5-4670K stock - 180 H/s
    
Currently this is the fastest Signatum SkunkHash miner on AMD cards.
    


# Usage
1. Download  
To download this miner, simly go to [Releases page](https://github.com/semtexzv/Prospector/releases) and download newest version for your platform. Currently supported platforms are 64bit Linux and Windows.  
Miner can be also found on MEGA [Download](https://mega.nz/#F!DtMHRIoI!2YzTj8u7UrSOeVCJZyFFjA).

2. Unzip miner into directory of your choosing
3. Run `prospector` or `prospector.exe`  
This will generate example configuration file named `config.toml` in current directory.

4. Update configuration information.  
You will probably want to replace pools and/or worker names associated with these pools. You can also disable cpu mining, or disable individual graphics cards. More information is available on [wiki](https://github.com/semtexzv/Prospector/wiki/Configuration-File)

5. Profit  
Just start the miner, and let the money roll in :)

# Alpha 
Currently, the miner only supports OpenCL platform for GPU mining. You can still mine on both AMD and NVIDIA cards with one small caveat. Most ethash coins require large amounts of memory, and NVIDIA does not allow allocation of these larges portions of memory on windows, so for the time being, mining on nvidia cards is only advised on Linux.

### Reporting issues
When you encounter an issue with this miner, please open new Github issue with as much information as you can provide. You can also include the `info.db` file, that is created by miner, and last entry from `logs` directory. The `info.db` file is a SQLite database that contains some information about mining sessions. It does not however contain any of your adresses, or pools on which you mine. You can inspect this file to ensure it does not contain sensitive information.

# Upcoming features
1. Support of other coins
2. More optimized OpenCL and CUDA kernels 
3. Better support for remote monitoring.
4. Integrated web interface

# Reasons you should use prospector

1. Support for multiple coins
2. Parallel CPU and GPU Mining
3. Easy extendability, which means awesome future upgrades.
4. Look into upcoming features.

# Reasons you might not want to use prospector

One thing you might not like about this miner is that it dedicates small portion of your hashrate as a fee to the developers. Every 2 hours, miner connects to another mining pool under the developers account, and for 70 seconds, mines on this account. This means, that your effective hashrate will be about 0.97% lower, you will probably not even notice this decrease, but it helps funding the development of this miner.

Devfee mining is separate for each coin. Miner does not transfer devfee time to another coins like claymores miner. That means mining both Eth and Xmr will not lead to 2% devfee on Eth. 

# Is this a virus ?
No. One reason for false positives might be the fact that the executable is protected to prevent easy reverse engineering.
