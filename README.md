# Hsimulator
My purpose is to simulate the benifit of Hybrid memory .vs. DRAM.

That is to say, just compare the performance of :
1) CPU-DRAM-DISK
2) CPU-(DRAM pairs NVRAM)-DISK

This is what I am thinking when designing this simulator:

Overview of the architecure:
1) CPU module
2) DRAM module
3) NVRAM module
4) HDD or SDD(when page faults occur, the system will fetch data from the Disk or SSD)
note: we can configue the system to use only DRAM or only NVRAM or hybrid memory(Pair DRAM and NVRAM)

How to design the simulator?
1. CPU just simulator the behavior when computing the CNN
   1) cache prefetch
   2) access DRAM and NVRAM 
   3) Memory(DRAM & NVRAM) prefetching data from Disk

2. for DRAM
   1) some of the capacity if for parameters and some of the capicity is for Dataset.
   2) all of the capacity of NVRAM is for Dateset.

3. for NVRAM
   1) just save the dataset all the time, without updating the dataset.

4. for HDD
   1) always store all the dataset.




