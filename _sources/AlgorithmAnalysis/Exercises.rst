Multiple Choice Exercises
-------------------------

Answer the following **Multiple Choice** questions to
assess what you have learned in this chapter.

.. mchoice:: cds_AA_count
   :author: Cynthia Lee

   Is that right to count how many times we perform each line of code when n is the size of vector?

   .. figure:: Figures/count.jpg
        :width: 200px
        :align: center
        :alt: count
        :figclass: align-center
    
   -   Yes

       + Correct! Then we will find we really don't care about the +5 or the 3 for that matter.

   -   No

       - Wrong! 

.. mchoice:: cds_AA_bigo1
   :author: Cynthia Lee

   f2 is O(f1)?

    .. figure:: Figures/bigo-1.jpg
        :width: 200px
        :align: center
        :alt: Bigo
        :figclass: align-center
    
    -   Yes

        + Correct! f1 is above f2—an “upper bound” f2 <= O(f1).

    -   No

        - Wrong! 

.. mchoice:: cds_AA_bigo2
   :author: Cynthia Lee

   f1 is O(f2)?

   .. figure:: Figures/bigo-1.jpg
       :width: 200px
       :align: center
       :alt: Bigo
       :figclass: align-center
    
   -   Yes

       +  Correct! f(n) = O(g(n)), if there are positive constants c and n0 such that f(n) ≤ c * g(n) for all n ≥ n0. We can move f2 above f1 by multiplying by c

   -   No

       -  Wrong!

 .. mchoice:: cds_aa_bigo3
   :author: Cynthia Lee

    f3 is O(f1)?

    .. figure:: Figures/bigo-2.jpg
        :width: 200px
        :align: center
        :alt: Bigo
        :figclass: align-center
    
    -   Yes

        - Wrong! 

    -   No

        + Correct! f3 <= O(f1)

.. mchoice:: cds_AA_bigo4
   :author: Cynthia Lee

    f1 is O(f3)?

    .. figure:: Figures/bigo-2.jpg
        :width: 200px
        :align: center
        :alt: Bigo
        :figclass: align-center
    
    -   Yes

        + Correct!

    -   No

        - Wrong!

.. mchoice:: cds_AA_fomular1
   :author: Cynthia Lee

    Let f(n) = 3 log2 n  +  4 n log2 n  +  n. Which of the following is true?

    
    -   f(n) = O(log2n)

        - Wrong!

    -   f(n) = O(nlog2n)

        - Wrong!

    -   f(n) = O(n^2)

        - Wrong!

    -   f(n) = O(n)

        - Wrong!

    -   Other/none/more

        + Correct!

.. mchoice:: cds_AA_fomular2
   :author: Cynthia Lee

    Let f(n) = 546 + 34n + 2n^2. Which of the following is true?

    
    -   f(n) = O(2^n)

        - Wrong!

    -    f(n) = O(n^2)

        + Correct!

    -    f(n) = O(n)

        - Wrong!

    -    f(n) = O(n^3)

        - Wrong!

    -    Other/none/more

        - Wrong!

.. mchoice:: cds_AA_fomular3
   :author: Cynthia Lee

    Let f(n) = 2^n + 14n^2 + 4n^3. Which of the following is true?

    
    -   f(n) = O(2^n)

        + Correct!

    -    f(n) = O(n^2)

        - Wrong!

    -    f(n) = O(n)

        - Wrong!

    -    f(n) = O(n^3)

        - Wrong!

    -    Other/none/more

        - Wrong!

.. mchoice:: cds_AA_fomular4
   :author: Cynthia Lee

    Let f(n) = 100. Which of the following is true?

    
    -   f(n) = O(2^n)

        - Wrong!

    -    f(n) = O(n^2)

        - Wrong!

    -    f(n) = O(n)

        - Wrong!

    -    f(n) = O(n^100)

        - Wrong!

    -    Other/none/more

        + Correct! O(1) can work.

.. mchoice:: cds_AA_memory
   :author: Cynthia Lee

   Each memory address indexes one byte (8 bits). Can you deduce from the drawing at right how many bits are used to represent int and double, respectively?

    .. figure:: Figures/diagram.jpg
        :width: 200px
        :align: center
        :alt: diagram
        :figclass: align-center
    
    -   4bits, 8bits

        - Wrong! 

    -   32bits, 64bits

        + Correct!

    -   16bits, 16bits 

         - Wrong!

    -   16bits, 32bits

         - Wrong! 

.. mchoice:: cds_AA_pointer
   :author: Cynthia Lee

   What prints here?

    ::

        int a[4] = {91, -2, 85, 17};
        int* p = a;            
        p[1] = 5;             
        p++;                   
        cout << *p << endl;   
        *(p + 2) = 26;         
        cout << p[2] << endl; 
        cout << a[2] << endl;

    -   26, 26

        - Wrong! 

    -   26, [other]

        + Correct! [other] is 85. p = &a[0]; p = &a[1]; a[3] = 26;

    -   [other], 26

        - Wrong! 

    -   [other], [other]

        - Wrong! 

.. mchoice:: cds_AA_memory_allocation
   :author: Cynthia Lee

   What prints here?

    ::

       int * p1 = new int;//0x12
       *p1 = 5;
       int * p2 = new int;//0x4 
       *p2 = 7;
       int * p3 = new int;//0x20
       *p3 = 8675309; // important phone #
       *p1 = *p2;
       cout << p1 << “ “ << *p1 << endl;

    -   0x12, 5

        - Wrong! 

    -   0x4, 7

        - Wrong! 

    -   0x12, 7

        + Correct!

    -   0x4, 5

        - Wrong! 

.. mchoice:: cds_AA_memory_allocation1
   :author: Cynthia Lee

   What prints here?

    ::

       int * p1 = new int;//0x12
       *p1 = 5;
       int * p2 = new int;//0x4 
       *p2 = 7;
       int * p3 = new int;//0x20
       *p3 = 8675309; // important phone #
       *p1 = *p2;
       cout << p1 << “ “ << *p1 << endl;
       p1 = p2;
       cout << p1 << “ “ << *p1 << endl;

    -   0x12, 5

        - Wrong! 

    -   0x4, 7

        + Correct!

    -   0x12, 7

        - Wrong!

    -   0x4, 5

        - Wrong! 

.. mchoice:: cds_AA_memory_allocation2
   :author: Cynthia Lee

   These last three lines…

    ::

       int * p1 = new int;//0x12
       *p1 = 5;
       int * p2 = new int;//0x4 
       *p2 = 7;
       int * p3 = new int;//0x20
       *p3 = 8675309; // important phone #
       *p1 = *p2;
       cout << p1 << “ “ << *p1 << endl;
       p1 = p2;
       cout << p1 << “ “ << *p1 << endl;
       delete p1;
       delete p2;
       cout << *p3 << endl; //print important phone #

    -   Looks good!

        - Wrong! 

    -   Didn’t do enough deleting

        - Wrong!

    -   Did too much deleting

        + Correct! In line 9, we set p1 to be pointing at p2's address. Then in line 11, we "delete p1", which will delete the object that p1 is pointing to (which is also the object that p2 is pointing to). When we do "delete p2" again, then we will get an error since we are trying to delete free memory. 


    -  Accessed memory after deleting

        - Wrong! 

.. mchoice:: cds_AA_set1
   :author: Cynthia Lee

    Which are Cliques?

    .. figure:: Figures/set.jpg
        :width: 200px
        :align: center
        :alt: set
        :figclass: align-center


    -   { B, D, E, F }

        - Wrong! 

    -   { B, C, D }

        - Wrong!

    -   { B, C }

        - Wrong!

    -    Other/none/more than one

        + Correct! A & C

 .. mchoice:: cds_AA_set2
   :author: Cynthia Lee

    Which are Independent Sets?

    .. figure:: Figures/set.jpg
        :width: 200px
        :align: center
        :alt: set
        :figclass: align-center


    -   { A, C, G }

        - Wrong! 

    -   { A, C, F }

        - Wrong!

    -  { A, E }

        - Wrong!

    -    Other/none/more than one

        + Correct! A & B & C


.. mchoice:: cds_AA_vertex
   :author: Cynthia Lee

    Find a vertex cover S that uses the fewest number of vertices (|S| is minimized). What is |S|?

   
    -   1

        - Wrong! 

    -   2

        - Wrong!

    -   3

        + Correct!

    -   4

        - Wrong! 

    -   >4

        - Wrong! 

   .. mchoice:: cds_AA_possibleTrue
   :author: Cynthia Lee

    how many of the following are possibly true?
    if (!x0  && x0)
    if (!x0  && (x1 || !x2) && (x2 || x3))
    if ((!x0 || !x1) && (x0 || x2) && x1 && !x2)

   
    -   0

        - Wrong! 

    -   1

        + Correct!  

    -   2

        - Wrong! 

    -   3

        - Wrong!       
