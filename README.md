# Blockchain Instructions

## Instructions
1. Ensure that you have downloaded and installed anaconda, puppeth, geth, and MyCrypto. These tools are needed to to access elitrade's blockchain network and crypto wallets. 
2. Direct to the folder in which you have geth saved
3. To initialize the first node on the blockchain, run the command: ./geth init z.json --datadir znode1
4. To initialize the first node on the blockchain, run the command: ./geth init z.json --datadir znode2
5. Create a file called "password.txt" with the password for the node(s), and save it in the same directory as your node files
* Ensure that there is an empty line below the password in the file (i.e. hit enter)
6. To start mining the first node, run the command: ./geth --datadir znode1 --mine --minerthreads 1 --rpc --unlock "4539A10D61ff4C4c11f19B5565bBE022Bb36d340" --allow-insecure-unlock --password password.txt
* The --mine flag tells the node to mine new blocks.
* The --minerthreads flag tells geth how many CPU threads, or "workers" to use during mining. Since our difficulty is low, we can set it to 1.
* The --unlock flag unlocks the node for use - the password.txt value calls the file we created above
* The --allow-insecure-unlock flag allows us to unlock in an insecure mananer 
* The --rpc flag allows this node to communciate via the internet
7. To start mining the second node, run the command: ./geth --datadir node2 --port 30304 --bootnodes "enode://84d51582daacef23ed6b3f4ace2e73d68878bdff63f5eb18439654fe0f6201b0a8cfc34bbc98a2988303c10d8eabc31787403c719ffeefee3454fb97af394d2d@127.0.0.1:30303" 
8. Open the MyCrypto app, and create create a test working as shown in the "network-config" image in the Screenshots folder
9. Once you have set up the network on your app, go to "View & Send" in the top left, and choose "Keystore File" as your authentication method. This will prompt you to direct to the file path of one of the crypto wallets below on your device. Select the file, and enter the password when prompted (also listed below).
10. You should now be in the wallet. In order to send ETH to the other account you are not currently in, copy and paste the receiving account's public key from below into the "To Address" input box, choose how much ETH you would like to send, and click on "Send Transaction"


## Network Information
* Network Name: elitrade
* Chain ID: 255
* Blocktime: 15

## Accounts:
* node 1 
** password = 123
** Public address of the key:   0x4539A10D61ff4C4c11f19B5565bBE022Bb36d340
** Path of the secret key file: node1\keystore\UTC--2021-09-21T18-38-01.329799400Z--4539a10d61ff4c4c11f19b5565bbe022bb36d340


* node 2
** password = 123
** Public address of the key:   0x19c1190a85b915C9bf0441508cCEe51fFe001027
** Path of the secret key file: node2\keystore\UTC--2021-09-21T18-44-03.839864100Z--19c1190a85b915c9bf0441508ccee51ffe001027
