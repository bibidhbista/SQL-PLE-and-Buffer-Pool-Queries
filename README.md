# SQL-PLE-and-Buffer-Pool-Queries


-- PLE QUERY
/*
		1.  All NUMAs have good PLE if (ple_per_4GB is > 300 sec)
		2.  If ple_per_4gb<300, memory is not reused efficiently as the performance will rely on the disk which is much slower than memory,
			and will generate a lot of disk IO and stress the storage. So, by looking at the PLE normalized to 4GB and per numa node, we can spot 
			the opportunity for optimization and investigate further (which objects are using the most of buffer cache memory, the distribution of 
			“hotness” of it’s indexes and partitions etc).
*/
