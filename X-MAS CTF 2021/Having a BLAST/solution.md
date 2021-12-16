# Having a BLAST
50 Points obtained at that moment

# Category
Bioinformatics

# Question
Hi! We have just opened our first Lapland Bio Lab, where we are trying to build the toys of the future! (Ethics not included. We are thankfully not concerned about them, that's the Legal department's job!).

While scavenging through files, we have found this DNA sequence that contains a few exons from what the file says, a "homo sapiens gene that encodes the [REDACTED] enzyme". There is nothing more descriptive than that, huh. Can you find the enzyme encoded by this gene? We need this done by today. Thanks!

Attached DNA sequence:
```CGCTTCCTCCCCAAATTGCTCAGCGCCACCGGTATGCAGGGGCCAGCGGGCAGCGGCTGGGAGGAGGGGAGTGGGAGCCCGCCAGGTGTAACCCCTCTCTTCTCCCCCTAGCCTCGGAGGCTCCCAGCACCTGCCCAGGCTTCACCCATGGGGAGGCTGCTCGGAGGCCCGGCCTCCCCCTGCCCCTCCTCCTCCTCCACCAGCTTCTCCTCCTCTTCCTCTCCCACCTCCGGCGGCTGTGAACACGGCCTCTTCCCCTACGGCCACAGGGGCCCCTCCTCTAATGAGTGGTCGGACCGTGGGGAAGGGCCCCACTCAGGGATCTCAGACCTAGTGCTCCCTTCCTCCTCAAACCGAGAGACTCACACTGGACAGGGCAGGAGGAGGGGGCCGTGCCTCCCACCCTTCTCAGGGACCCCCACGCCTTTGTTGTTTGAATGGAAATGGAAAAGCCAGTATTCTTTTTATAAAATTATCTTTTTGGAACCTGAGCCTGACATTGGGGGGAAGTGGGAGGCCGGACGGGTAGCACCCC ```


(The flag format is X-MAS{enzymename})

Author: Milkdrop

# Solution
This category led me mislead to the point where I attempted to tamper with the DNA sequence by decoding it, wasting valuable time working out how to solve it. However, thanks to the resources shared by the Discord community, I was able to grasp the issue, which could lead to the usage of a tool for my genomic research to solve the challenge. I was able to understand the hint by looking at the bolded challenge title **BLAST**. 

As a result, I did some further research and discovered that there is a BLAST (Basic Local Alignment Search Tool) tool that can help with this challenge.
![BLAST Tool](https://user-images.githubusercontent.com/55530196/146302553-3dead57a-bb25-4a28-8327-ec927e4252e9.png)

To use this tool, I must first identify if I am working with a Nucleotide BLAST or a Protein BLAST. As a result, looking up the homo sapiens gene that codes for the enzyme I'm looking for reveals that it's a Nucleotide BLAST. 

I was able to search the database for the enzyme that I'm seeking for by loading the DNA Sequence in the **Query Sequence** tab.
![BLAST tool Query Sequence Tab](https://user-images.githubusercontent.com/55530196/146303318-e99f8888-2a4e-4cc8-9c61-2c6a40a51fb0.png)

Finally, the results show that the enzyme that is encoded by homo sapiens gene is **acetylcholinesterase** which the challenge is then solved by putting in the correct flag format.

![image](https://user-images.githubusercontent.com/55530196/146303522-1307aa66-2297-4c05-b2f2-cf04111ba1a6.png)

``` Flag: X-MAS{acetylcholinesterase} ```

# Additional Resources
[Article on Reverse Engineering the source code of the vaccine](https://berthub.eu/articles/posts/reverse-engineering-source-code-of-the-biontech-pfizer-vaccine/) </br>
[Video on How to Use BLAST for Finding and Aligning DNA or Protein Sequences](https://www.youtube.com/watch?v=WRKQGwh_Mw0) </br>
[BLAST tool](https://blast.ncbi.nlm.nih.gov/Blast.cgi)
