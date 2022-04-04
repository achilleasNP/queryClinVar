# queryClinVar

## Description
This program queries the Clinvar Database api through http requests
To convert a file with variants from RNA and Protein co-ordinates as the example below:

```
    variant,Amino acid
    PALB2 04 1129C>T,p.Gln377X
    PALB2 04 509_510delGA,p.Arg170IlefsX14
    RET 14 2410G>A,p.Val804Met
    SDHC 05 387G>A,p.Trp129X
```

To a file that contains spdi canonical ids and genomic locations:

```
    variant,Amino acid,spid,chrom,pos,ref,alt,bcftoolsQuery
    PALB2 04 1129C>T,p.Gln377X,NC_000016.10:23635416:G:A,16,23635417,G,A,chr16:23635417-23635417
    PALB2 04 509_510delGA,p.Arg170IlefsX14,NC_000016.10:23636035:TCT:T,16,23636035,ATC,A,chr16:23636035-23636035
    RET 14 2410G>A,p.Val804Met,NC_000010.11:43119547:G:A,10,43119548,G,A,chr10:43119548-43119548
    SDHC 05 387G>A,p.Trp129X,NC_000001.11:161356821:G:A,1,161356822,G,A,chr1:161356822-161356822

```

## Installation

Requirements you will need to have stack available. On some servers that's available with the haskell installation (e.g.: module load haskell).

1. Clone the repository git clone 
2. Change to the local repository directory
3. Run stack build
4. Optional: Run stack install 

## Usage

- If you used stack install:
```
    queryClinVar-exe INPUT\_FILE OUTPUT\_FILE 
```

- Running using stack
  From the local repository directory

```
   stack run -- INPUT\_FILE OUTPUT\_FILE 
```



