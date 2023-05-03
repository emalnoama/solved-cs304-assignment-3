Download Link: https://assignmentchef.com/product/solved-cs304-assignment-3
<br>
LINEAR PAGE TABLE

In this homework, you will use a simple program, which is known as paging—Ii near—t rans lat e . py, to see if you understand how simplevirtual-to-physical address translation works with linear page tables. See the README for details.

Questions

<ol>

 <li>Before doing any translations, let’s use the simulator to study how linear page tables change size given different parameters. Compute the size of linear page tables as different parameters change. Some suggested inputs are below; by using the -v flag, you can see how many page-table entries are filled. First, to understand how linear page table size changes as the address space grows, run with these flags:</li>

</ol>

—P 1k —a 1m —p 512m —v —n O

—P 1k —a 2m —p 512m —v —n O

—P 1k —a 4m —p 512m —v —n O

Then, to understand how linear page table size changes as page size

grows:

—P 1k —a 1m —p 512m —v —n 0

—P 2k —a 1m —p 512m —v —n 0

—P 4k —a 1m —p 512m —v —n 0

Before running any Of these, try to think about the expected trends.

How should page-table size change as the address space grows? As the page size grows? Why not use big pages in general?

What happens as you increase the percentage of pages that are allocated in each address space?

. Now let’s try some different random seeds, and some different (and sometimes quite crazy) address-space parameters, for variety: and change the number Of pages that are allocated to the address

space with the —u flag. For example:

-a

-a

—v

-a

—v

-P 1k

-P 1k

-P 1k

—p 1k

—a 16k

—a 16k

—a 16k

-a 16k

-a 16k

—p 32k

—p 32k

—p 32k

-p 32k

-p 32k

—v

—u 25

—v

-u 50

-v

-v -u 75

-u 100

-v

-P 8k

.p 1m

32

32k

256m

-p 1024

-p 1m

-p 512m

Vhich of these parameter combinations are unrealistic? Why?

Jse the program to try out some other problems. Can you find the




Use the program to try out some other problems. Can you

the

limits of where the program doesn’t work anymore? For example,

what happens if the address-space size is bigger than physical mem-

ory?

“ULTILEVEL PAGE TABLE

-o understand how a multi-level page table works, you will use the program

‘aging-multilevel-translate.py; see the README for details.

1. With a linear page table, you need a single register to locate the page table, assuming that hardware does the lookup upon a TLB miss. How many registers do you need to locate a two-level page table? A three-level table?

2. Use the simulator to perform translations given random seeds O,1, and 2, and check your answers using the -c flag. How many memory references are needed to perform each lookup?

3. Given your understanding of how cache memory works, how do you think memory references to the page table will behave in the cache? Will they lead to lots of cache hits (and thus fast accesses?)

Or lots of misses (and thus slow accesses)?


