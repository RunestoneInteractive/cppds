Multiple Choice Exercises
-------------------------

Answer the following **Multiple Choice** questions to
assess what you have learned in this chapter.


.. mchoice:: cds_Hash_quick

     Can we do binary search on a linked list to implement a quick insert?

    
    -   It’s a great idea as long as you have a doubly-linked list

        - Wrong! 

    -   Even with a doubly-linked list the performance is not good, because linked list nodes are strewn all over the heap so you can’t jump right to a middle one

         + Correct!

    -   It’s a great idea as long as you make sure that your linked list nodes follow one another in heap memory with no gaps so you can jump to the middle one

        - Wrong! 

 
    
.. mchoice:: cds_Harsh_BSTput

        Insert: 22, 9, 34, 18, 3     
        How many of these result in the same tree structure as above?
        22, 34, 9, 18, 3
        22, 18, 9, 3, 34
        22, 9, 3, 18, 34

    
    -   None of these

        - Wrong! 

    -   1 of these

        - Wrong! 

    -   2 of these

        + Correct! 

    -   ALL of these

        - Wrong! 
    
.. mchoice:: cds_Harsh_badBST //?

     How many distinctly structured BSTs are there that exhibit the worst-case height (height equals the number of nodes) for a tree with 5 nodes?

    
    -   2-3

        - Wrong! 

    -  4-5

        -  Wrong!  

    -   6-7

        - Wrong! 

    -  8-9

        - Wrong! 

    -  more than 9

        + Correct! 2^4 = 16

.. mchoice:: cds_Harsh_bestBST //?

     What is the BEST CASE cost for doing containsKey() in BST?

    
    -   O(1)

        - Wrong! 

    -  O(log n)

         + Correct! In the best-case scenario, the binary search tree would be a balanced binary search tree. So the height of the search three becomes log(n), therefore the best case time complexity is O(log n).

    -   O(n)

        - Wrong! 

     -  O(n log n)

        - Wrong! 

     -  O(n^2)

        - Wrong!

.. mchoice:: cds_Harsh_worstBST 

     What is the WORST CASE cost for doing containsKey() in BST?

    
    -   O(1)

        - Wrong! 

    -  O(log n)

        - Wrong! 

    -   O(n)

        + Correct!  in the worst-case scenario, we can have a tree with worst-case height and the element that we have to search for maybe at the very "end" or "bottom" of the tree, so we would have to traverse through all of the nodes to search for that element. Therefore, we would have an O(n) run-time complexity in the worst-case scenario.

     -  O(n log n)

        - Wrong! 

     -  O(n^2)

        - Wrong!

.. mchoice:: cds_Harsh_worstBST 

     What is the WORST CASE cost for doing containsKey() in BST if the BST  is complete??

    
    -   O(1)

        - Wrong! 

    -  O(log n)

         + Correct! Every complete BST is balanced. Therefore, searching for a key in a complete BST would have O(log n) complexity.

    -   O(n)

        - Wrong! 

     -  O(n log n)

        - Wrong! 

     -  O(n^2)

        - Wrong!

.. mchoice:: cds_Harsh_closedaddressing

    Where does key=“Annie” value=55 go if hashkey(“Annie”)   = 3?

     -  55 overwrites 10 at 3

        - Wrong! 

     - A link list node is added at 3

         + Correct!

     - Other/none/ more than one

        - Wrong!

.. mchoice:: cds_Harsh_hashmap

    We don’t actually need to store the keys in the nodes—we only really need the key to find which index, then store the value there.TRUE or FALSE

     - TRUE

        - Wrong! 

     - FALSE

         + Correct!

 .. mchoice:: cds_Harsh_print

    What does this print?

    .. figure:: Figures/Harshprint.jpg
        :width: 200px
        :align: center
        :alt: Harsh_print
        :figclass: align-center
     ::

        void traverse(Node *node) {
          if (node != NULL) {
             cout << node->key << " ";
             traverse(node->left);
             traverse(node->right);
          }
        }

    
    -   A B C D E F

        - Wrong! 

    -  A B D E C F

         + Correct! 

    -  D B E F C A

        - Wrong! 

     -  D E B F C A

        - Wrong! 

.. mchoice:: cds_Harsh_print2

    What does this print?

    .. figure:: Figures/Harshprint.jpg
        :width: 200px
        :align: center
        :alt: Harsh_print
        :figclass: align-center
     ::

        void traverse(Node *node) {
          if (node != NULL) {
             traverse(node->left);
             cout << node->key << " ";
             traverse(node->right);
          }
        }


    
    -   A B C D E F

        - Wrong! 

    -  A B D E C F

        - Wrong!  

    -  D B E F C A

        - Wrong! 

     -  D E B F C A

        - Wrong! 

     -  D B E A C F

        + Correct! 

.. mchoice:: cds_Harsh_Pprintorder

           
       How can we get this to print our ABCs in order?

    .. figure:: Figures/Harshprint.jpg
        :width: 200px
        :align: center
        :alt: Harsh_print
        :figclass: align-center
    
    -   You can’t—we already tried moving the cout to all 3 possible places.

        - Wrong! 

    -   You can but you use a stack instead of recursion.

        - Wrong! 

    -   You can but you use a queue instead of recursion.

        + Correct! 

    -   Other/none/more

        - Wrong! 

.. mchoice:: cds_Harsh_printorder2

   That prints the ABC nodes in order, but notice that our ABC tree isn’t a BST. How do we print BST nodes in order?

    .. figure:: Figures/Harshprintorder2.jpg
        :width: 200px
        :align: center
        :alt: Harsh_print
        :figclass: align-center
     ::

        int traverse(Node *node) {
          if (node != NULL) {
             traverse(node->left);
             traverse(node->right);
          }
        }


    
    -  Use the BFS (queue instead of recursion).

        - Wrong! 

    -  Use the DFS and put cout first.

        - Wrong!  

    -  Use the DFS and put cout between.

        + Correct! 

     -  Use the DFS and put cout last.

        - Wrong! 


.. mchoice:: cds_Harsh_print3

    We can play the same game with non-alpha characters as keys: What does this print?

    .. figure:: Figures/Harshprint3.jpg
        :width: 200px
        :align: center
        :alt: Harsh_print
        :figclass: align-center
     ::

        int traverse(Node *node) {
          if (node != NULL) {
             int l = traverse(node->left);
             int r = traverse(node->right);
             return l + r
          }
        }


    
    -  * + / 3 4 8 2

        - Wrong! 

    - * + 3 4 / 2

        - Wrong!  

    -  3 + 4 * 8 / 2

        - Wrong! 

     - 3 4 + 8 2 / *

        + Correct! 

