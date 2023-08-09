Multiple Choice Exercises
-------------------------

Answer the following **Multiple Choice** questions to
assess what you have learned in this chapter.


.. mchoice:: cds_Recursive_secondout
   :author: Cynthia Lee

    What is the second thing printed when we call factorial(10)?

    ::

        long factorial (int n) {
        cout << n << endl; 
        long result;
        if (n == 1) result = 1;
        else result = n * factorial(n – 1);
        return result;
}
    -   1

        - Wrong! 

    -   2

         + Correct! 2 * 1

    -   10

        - Wrong! 

    -   90

        - Wrong! 
    

.. mchoice:: cds_Recursive_third
   :author: Cynthia Lee

    What is the third thing printed when we call factorial(10)?

    ::

        long factorial (int n) {
        cout << n << endl; 
        long result;
        if (n == 1) result = 1;
        else result = n * factorial(n – 1);
        return result;
}

    -   2

        - Wrong! 

    -   3

        - Wrong! It starts from 10 to 1 not from 1 to 10.

    -   8

        + Correct! 

    -   6

        - Wrong! returned or printed?

.. mchoice:: cds_Recursive_fourth
   :author: Cynthia Lee

    What is the fourth thing printed when we call factorial(10)?

    ::

        long factorial (int n) {
        cout << n << endl; 
        long result;
        if (n == 1) result = 1;
        else result = n * factorial(n – 1);
        return result;
}

    -   4

        - Wrong! returned or printed?

    -   8

        - Wrong!

    -   24

        + Correct! 2 * 1 -> 3 * 2 * 1 -> 4 * 3 * 2 * 1;

    -   90

        - Wrong! 

.. mchoice:: cds_Recursive_memory
   :author: Cynthia Lee

    How does this look in memory?

    ::

        long factorial ( int n ) {
            cout << n << endl; 
            long result;
            if (n==1) result = 1;
            else result = n*factorial(n–1);
            return result;
        }

        void myfunction(){
	    int x = 10;
	    long xfac = 0;
	    xfac = factorial(x);
        }

    //!REMINDER!

 .. mchoice:: cds_Recursive_fourth
   :author: Cynthia Lee

    What is the fourth thing printed when we call factorial(10)?

    -   Only three items remain: save yourself an unnecessary function call that would trivially divide them into halves of size 1, and just check all three.

        - Wrong! 

    -   Only two items remain: can’t divide into two halves with a middle, so just check the two.

        - Wrong!  

    -   Only one item remains: just check it.

        + Correct! Arm's length recursion writes more code than necessary by having special cases rather than letting recursions do the work.

    -   No items remain: obviously we didn’t find it.

        - Wrong! 

.. mchoice:: cds_Recursive_binary
   :author: Cynthia Lee

    Which line should be coded here?

    ::

        bool binarySearch(Vector<int>& data, int key){
          return binarySearch(data, key, 0, data.size()-1);
        }

        bool binarySearch(Vector<int>& data, int key, int start, int end){
  	 // Write code to handle the base case “No items remain: 
 	 // obviously we didn’t find it by returning false
 	 //to be continued…
	}

    -   if (data.size() <= 0) return false;

        - Wrong! 

    -    if (end < start) return false;

         + Correct! 

    -   if (end == start) return false;

         - Wrong! 

 .. mchoice:: cds_Recursive_snow
   :author: Cynthia Lee

    Where should this line of code be inserted to produce the pattern shown?
    drawFilledBox(window, cx, cy, dim, "Gray", "Black");

    .. figure:: Figures/snowflake.jpg
        :width: 200px
        :align: center
        :alt: Boxy Snowflake
        :figclass: align-center

    ::
        static const double SCALE = 0.45;

        static void drawFractal(GWindow& window, double cx, double cy, double dim, int order) { 
         
        if (order >= 0) { 

           drawFractal(window, cx-dim/2, cy+dim/2, SCALE*dim, order-1);
         
           drawFractal(window, cx+dim/2, cy-dim/2, SCALE*dim, order-1); 

           drawFractal(window, cx-dim/2, cy-dim/2, SCALE*dim, order-1); 

           drawFractal(window, cx+dim/2, cy+dim/2, SCALE*dim, order-1); 

         } 

        } 

    -   drawFractal(window, cx-dim/2, cy+dim/2, SCALE*dim, order-1);

        - Wrong! 

    -    drawFractal(window, cx+dim/2, cy-dim/2, SCALE*dim, order-1);

         - Wrong! 

    -   drawFractal(window, cx-dim/2, cy-dim/2, SCALE*dim, order-1); 

         - Wrong! 

    -    drawFractal(window, cx+dim/2, cy+dim/2, SCALE*dim, order-1); 

         - Wrong!
'
    -    None of the above

         + Correct! 

.. mchoice:: cds_Recursive_realsnow
   :author: Cynthia Lee

    Can these be made by changing the order of lines and/or deleting lines in the draw function?

    .. figure:: Figures/snowflake1.jpg
        :width: 200px
        :align: center
        :alt: Boxy Snowflake - 1
        :figclass: align-center

    .. figure:: Figures/snowflake2.jpg
        :width: 200px
        :align: center
        :alt: Boxy Snowflake - 2
        :figclass: align-center

    
    -   1 is real

        - Wrong! 

    -    2 is real

         - Wrong! 

    -   Both are shopped

         + Correct! 

    -    Both are real

         - Wrong!

.. mchoice:: cds_Recursive_maze
   :author: Cynthia Lee

   In what order do we visit these spaces?

    .. figure:: Figures/Maze-solving.jpg
        :width: 200px
        :align: center
        :alt: Maze-solving
        :figclass: align-center
    
    -   x1, x2, x3

        - Wrong! 

    -    x2, x3, x1

         - Wrong! 

    -   x1, x3, x2

         - Wrong!

    -    We don’t visit all three

         + Correct! We can't visit x2.


.. mchoice:: cds_Recursive_stack
   :author: Cynthia Lee

   What is the deepest the Stack gets during the solving of this maze?

    .. figure:: Figures/stack.jpg
        :width: 200px
        :align: center
        :alt: The stack
        :figclass: align-center
    
    -   Less than 5

        - Wrong! 

    -    5-10

         - Wrong! 

    -   11-20

         - Wrong!

    -    More than 20

         + Correct! 

.. mchoice:: cds_Recursive_fibonacci
   :author: Cynthia Lee

   How many times would we calculate Fib(2) while calculating Fib(6)? See if you can just “read” it off the chart above.

    .. figure:: Figures/fibonacci.jpg
        :width: 200px
        :align: center
        :alt: fibonacci
        :figclass: align-center
    
    -   4 times

        - Wrong! 

    -   5 times

        + Correct!  

    -   6 times

         - Wrong!

.. mchoice:: cds_Recursive_fibonacci-2
   :author: Cynthia Lee

   Assume we have to calculate each unique function call once, but never again. And We “remember” the answer from the first time.
   How many rectangles remain in the above chart for n=5?

    .. figure:: Figures/fibonacci.jpg
        :width: 200px
        :align: center
        :alt: fibonacci
        :figclass: align-center
    
    -   3

        - Wrong! 

    -   6 

        - Wrong! Are there any other possibilities? 

    -   7 

         - Wrong!

    -   9 

         - Wrong! Are there any other possibilities? 

    -   More than one.

        + Correct! 6 or 9

.. mchoice:: cds_Recursive_fibonacci-3
   :author: Cynthia Lee

   Assume we have to calculate each unique function call once, but never again. And We “remember” the answer from the first time.
   For some integer n>2, what is the largest number of function calls that can be triggered by the calculation of F(n) in this new “remember” system?

    .. figure:: Figures/fibonacci.jpg
        :width: 200px
        :align: center
        :alt: fibonacci
        :figclass: align-center
    
    -   Approx. log(n)

        - Wrong! 

    -   Approx. n 

        + Correct!

    -   Approx. n^2 

         - Wrong!

    -   Approx. 2^n

         - Wrong! 

.. mchoice:: cds_Recursive_memory
   :author: Cynthia Lee

        How does this look in memory?

    ::

        long factorial (int n) {
        cout << n << endl; 
        long result;
        if (n == 1) result = 1;
        else result = n * factorial(n – 1);
        return result;
        }
        void myfunction(){
	        int x = 10;
	        long xfac = 0;
	        xfac = factorial(x);
        }

     .. figure:: Figures/memory1.jpg
            :width: 200px
            :align: center
            :alt: memory
            :figclass: align-center

    - .. figure:: Figures/memory2.jpg
            :width: 200px
            :align: center
            :alt: memory
            :figclass: align-center

        - Wrong! 

    - .. figure:: Figures/memory3.jpg
            :width: 200px
            :align: center
            :alt: memory
            :figclass: align-center

        + Correct! 

    -  .. figure:: Figures/memory4.jpg
            :width: 200px
            :align: center
            :alt: memory
            :figclass: align-center

        - Wrong!  

  
