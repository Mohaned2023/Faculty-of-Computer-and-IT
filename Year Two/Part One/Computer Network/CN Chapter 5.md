> [!NOTE]
> - Data can be corrupted during transmission.  
> - Some applications require that errors be detected and corrected.
> - In a single-bit error, only 1 bit in the data unit has changed.
> - A burst error means that 2 or more bits in the data unit have changed.
> - To detect or correct errors, we need to send extra (redundant) bits with data.
> - In this book, we concentrate on block codes; we leave convolution codes to advanced texts.
> - In modulo-N arithmetic, we use only the integers in the range 0 to N −1, inclusive.


#### BLOCK CODING:
In block coding, we divide our message into blocks, each of k bits, called datawords. We add r redundant bits to each block to make the length n = k + r. The resulting n-bit blocks are called codewords.

#### 
> [!NOTE]
> - An error-detecting code can detect only the types of errors for which it is designed; other types of errors may remain undetected.
> - The Hamming distance between two words is the number of differences between corresponding bits.
> - The minimum Hamming distance is the smallest Hamming distance between all possible pairs in a set of words.