BadCoin
=======
  
Algo sha256d  
Halving 34,560 blocks  
Initial block reward 1,000 BAD  
Target spacing 5 min  
Target timespan 5 h  
Coinbase maturity 5 blocks  
Max supply 69,120,000 coins  

=======
boss@hashmebadly.com  
https://bitcointalk.org/index.php?topic=844023.0  
https://twitter.com/Bad_Coin

=======

Known compiling issue:  

@BadCoin/src: make -f makefile.unix  
Building LevelDB ...  
make[1]: Entering directory `/root/BadCoin/src/leveldb'  
make[1]: *** No rule to make target `libleveldb.a'.  Stop.  
make[1]: Leaving directory `/root/BadCoin/src/leveldb'  
make: *** [leveldb/libleveldb.a] Error 2  
  
How to fix:  
  
@BadCoin/src: sudo rm -r leveldb   
@BadCoin/src: git clone https://code.google.com/p/leveldb/  
@BadCoin/src: make -f makefile.unix  
  
