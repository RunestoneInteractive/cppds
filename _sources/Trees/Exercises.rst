Multiple Choice Exercises
-------------------------

Answer the following **Multiple Choice** questions to
assess what you have learned in this chapter.


.. mchoice:: cds_tree_remove
   :author: Cynthia Lee

    Suppose we have a pointer (current) to the node containing the item to be removed.
    What additional information do we need to successfully remove the node?


    .. figure:: Figures/remove.jpg
        :width: 200px
        :align: center
        :alt: remove
        :figclass: align-center

    -    Nothing additional.

        - Wrong! 

    -    A pointer to the node immediately prior to the to-be-deleted node.

        + Correct! 

    -    A pointer to the node immediately after the to-be-deleted node.

        - Wrong! 

    -   Both B and C.

        - Wrong! 
    
.. mchoice:: cds_tree_binarytree
   :author: Cynthia Lee

    How many of these are valid binary trees?


    .. figure:: Figures/binarytree.jpg
        :width: 200px
        :align: center
        :alt: binary-trees
        :figclass: align-center

    -    0-3

        - Wrong! 

    -   7-8

        + Correct! 1,2,3,4,5,6,8 are correct

    -    4-6

        - Wrong! 

.. mchoice:: cds_tree_binaryheap
   :author: Cynthia Lee

    How many of these are valid binary heaps?


    .. figure:: Figures/binaryheap.jpg
        :width: 200px
        :align: center
        :alt: binary-heaps
        :figclass: align-center

    -    0-1

        - Wrong! 

    -   4

        + Correct! 1,2,5,8 are correct

    -    2-3

        - Wrong!
    
.. mchoice:: cds_tree_minbinaryheap
   :author: Cynthia Lee

    How many of these are valid min-binary-heaps?


    .. figure:: Figures/minbinaryheap.jpg
        :width: 200px
        :align: center
        :alt: min-binary-heaps
        :figclass: align-center

    -    0

        - Wrong! 

    -   1

        + Correct! The 2nd one is correct

    -    2

        - Wrong!

    -    3

        - Wrong!
    
.. mchoice:: cds_tree_minbinaryheap2
   :author: Cynthia Lee

   In how many places could the smallest number in this min-binary-heap be located?


    .. figure:: Figures/minbinaryheap2.jpg
        :width: 200px
        :align: center
        :alt: min-binary-heaps
        :figclass: align-center

    -    0-2

        - Wrong! 

    -   3-4

        + Correct! The 2nd one is correct

    -    5-6

        - Wrong!

    -    7-8

        - Wrong!
   
.. mchoice:: cds_tree_arrayheap
   :author: Cynthia Lee

   For the tree of height h, the array length is 2^h-1 For a node in array index i: Parent is at array index:?


    .. figure:: Figures/arrayheap.jpg
        :width: 200px
        :align: center
        :alt: arrayheap
        :figclass: align-center

    -    i-2

        - Wrong! 

    -   (i-1)/2

         + Correct! 

    -    i/2

        - Wrong!

    -    2i

        - Wrong!

.. mchoice:: cds_tree_arraybinheap
   :author: Cynthia Lee

   For the tree of height h, the array length is 2^h-1 For a node in array index i: Left child is at array index:?


    .. figure:: Figures/arraybinheap.jpg
        :width: 200px
        :align: center
        :alt: arraybinheap
        :figclass: align-center

    -    i+1

        - Wrong! 

    -   i+2

         - Wrong!

    -    2i+1

        + Correct!

    -    2i

        - Wrong!

.. mchoice:: cds_tree_tf
   :author: Cynthia Lee

   There is only one configuration of a valid min-heap containing the elements {34, 22, 3, 9, 18} 


    -    TRUE

        - Wrong! 

    -   FALSE

        + Correct! 

 .. mchoice:: cds_tree_distict
   :author: Cynthia Lee

   How many distinct min-heaps are possible for the elements {3, 9, 18, 22, 34}?


    -    1-2

        - Wrong! 

    -   3-4

        - Wrong!

   -    5-8

        + Correct!  

   -    5!

        - Wrong! 

 .. mchoice:: cds_tree_time
   :author: Cynthia Lee

   What is the worst-case time cost for each heap operation: Add, Remove, Peek?


    -  O(n), O(1), O(1)

        - Wrong! 

    -   O(logn), O(logn), O(1)

        + Correct! 

   -    O(n), O(logn), O(logn)

        - Wrong! 

.. mchoice:: cds_tree_insert
   :author: Cynthia Lee

   What is the next configuration in this sequence?

    .. figure:: Figures/sequence.jpg
        :width: 200px
        :align: center
        :alt: sequence
        :figclass: align-center

    -  12, 8, 2, 10

        - Wrong! 

    -   12, 10, 2, 8

        + Correct! 

   -    12, 10, 8, 2

        - Wrong! 
