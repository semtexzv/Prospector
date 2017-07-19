# Prospector
Multi-algorithm cryptocurrency miner. This miner can utilize all resources provided by your mining rig. It mines on all your CPUs and GPUs. Currently, this miner is in alpha stage, and can only mine Ethash coins on GPU and CryptoNight coins on CPU.



# Usage
1. Download  
To download this miner, simly go to [Releases page](https://github.com/semtexzv/Prospector/releases) and download newest version for your platform. Currently supported platforms are 64bit Linux and Windows.  

2. Unzip miner into directory of your choosing
3. Run `prospector` or `prospector.exe`  
This will generate example configuration file named `config.json` in current directory.

4. Update configuration information.  
You will probably want to replace pools and/or worker names associated with these pools. You can also disable cpu mining, or disable individual graphics cards.

5. Profit  
Just start the miner, and let the money roll in :)

# Alpha 
Currently, the miner only supports OpenCL platform for GPU mining. You can still mine on both AMD and NVIDIA cards with one small caveat. Most ethash coins require large amounts of memory, and NVIDIA does not allow allocation of these larges portions of memory on windows, so for the time being, mining on nvidia cards is only advised on Linux.

### Reporting issues
When you encounter an issue with this miner, please open new Github issue with as much information as you can provide. You can also include the `info.db` file, that is created by miner. This file is a SQLite database that contains some information about mining sessions. It does not however contain any of your adresses, or pools on which you mine. You can inspect this file to ensure it does not contain sensitive information.

# Hashrates
Miner achieves hashrates, that are competitive with other miners.

measured:

    ETH GTX 1070 OC - 30 MH/s
    XMR Intel i5-4670K stock - 180 H/s



# Upcoming features
1. Support of other coins, namely Sia, Dcr, Zcash on GPU and HodlCoin on CPU
2. More optimized OpenCL kernels 
3. Open-source monitoring and control server implementation, that you can use to monitor your large scale mining operation.
4. Mobile applications to use with monitoring server

# Reasons you should use prospector

1. Support for multiple coins
2. Parallel CPU and GPU Mining
3. Easy extendability, which means awesome future upgrades.
4. Look into upcoming features.

# Reasons you might not want to use prospector

One thing you might not like about this miner is that it dedicates small portion of your hashrate as a fee to the developers. Every 2 hours, miner connects to another mining pool under the developers account, and for 70 seconds, mines on this account. This means, that your effective hashrate will be about 0.97% lower, you will probably not even notice this decrease, but it helps funding the developers of this miner.

Devfee mining is separate for each coin. Miner does not transfer devfee time to another coins like claymores miner. That means mining both Eth and Xmr will not lead to 2% devfee on Eth. 

# Is this a virus ?
No. One reason for false positives might be the fact that the executable is packed to prevent easy reverse engineering.
