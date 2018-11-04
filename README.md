# kmer-counter-emilib

The `kfs` program reads in multiline FASTA records, counts canonical kmers using Emil Ernerfeldt's [`emilib::HashMap` hash table](https://github.com/emilk/emilib/blob/master/emilib/hash_map.hpp), and measures time taken to read in and process records. A discussion about performance characteristics compared with the C++ STL `std::unordered_map` is [available from the author](http://www.ilikebigbits.com/blog/2016/8/28/designing-a-fast-hash-table).

## Usage

### Compilation

```
$ make kfs
```

### Performance

Specify variables `K` (integer) and `FASTA` (path to FASTA sequences).

```
$ /usr/bin/time -l ./kfs -k ${K} -i ${FASTA}
...
```
