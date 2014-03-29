## DFT in synchronization testing ##

	Huang MingEn (13126083) mingenhuang@gmail.com

### About Data Flow Testing (DFT） ###

DFT contains much detail in its models and uses it in testing. Typically such detailed information can only be obtained based on program code and detailed design, making them more likely to be used as white-box testing techniques. In this respect, DFT is more likely to be used as a black-box testing technique for various situations, including object-level testing for object-oriented systems. DFT can also be enhanced to support usage-based statistical testing.

### DFT application in synchronization testing ###

For situations like y<—f(xl,x2,.. . ,xn),that is, when data items x1,x2,.., xn, are used and processed to define the value for y, we can draw links from them to y. When we interpret these xi’s as parallel tasks carried out before our next task y, these links represent the synchlronization situation: All the xi tasks must finish before y can be completed. That is, if some of the xi’s finish early, we still have to wait for the other to finish before we can finish y. Because of the dynamic nature of such individual tasks executed in parallel, the testing of the correct handling of such synchronizations involves two elements：

- Correct (computational) result (y value) is obtained or appropriate processing (y processing) is applied for given input xi’s. One special case for this is that no result should be produced or no processing should be applied if we do not have all the xi’s available.
- Synchronization of arrivals among xi’s in all possible orders, including time ordered arrivals as well as the possibility of one or more xi’s arriving at exactly the same time.

In synchronization testing, we would combine the above two conditions to test the arrivals of 5,’s in all different arriving orders, and to check for the correct outcome. For example, with two way synchronization of input A and B to produce C, we can run the following synchronization testing cases：

- Nothing arrives => no output.
- One arrives (2 cases: A alone or B alone) => no output.
- Both arrive (3 cases: A then B, B then A, or A and B together) => verify that correct C is obtained.

As we can see, even for such a simple situation, we have 6 synchronization test cases. When the number of xi’s goes up, we need significantly more synchronization test cases due to the combinatorial explosion of possible arriving orders. One way to simplify such testing is through hierarchical models to form groups among the xi and then synchronize the grouped results. For example, for a 4-way synchronization, if we can group them into two groups of 2-way synchronizations, we can then use 6 test cases for each group and then 6 additional test cases to synchronize the two groups by treating each group as a single input in the higher-level model, resulting in 18 total synchronization test cases. The raw 4-way synchronization would involve substantially more test cases.

