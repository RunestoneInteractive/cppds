Multiple Choice Exercises
-------------------------

Answer the following **Multiple Choice** questions to
assess what you have learned in this chapter.

.. mchoice:: cds_intro_bug

    Can you find the bug here?

    ::

        // (includes omitted)
        static void clearBoard(Grid<bool> board);

        int main(){
            Grid<bool> board(8,8);
            /* note that clearing here is not 
             * strictly necessary */
            clearBoard(board);  
            // …more code to come…
        return 0;
        }

        static void clearBoard(Grid<bool> board){
            for (int i=0; i<board.numRows(); i++){
                for (int j=0; j<board.numCols(); j++){
                    board[i][j] = false;
               }
            }
        }

    -   The for loops have an off-by-one error on the edges of the grid.

        - Wrong!

    -   Board is declared but not instantiated.

        - Wrong!

    -   The board in main() is not updated.

        + Correct! You should add '&' here: static void clearBoard(Grid<bool>& board)

    -   The code is inefficient.

        - Wrong!




.. mchoice:: cds_intro_betterone

    Which one is better?

    ::

        // The first one
        static void printBoard(Grid<bool>& board){
            for (int i=0; i<board.numRows(); i++){
                for (int j=0; j<board.numCols(); j++){
                    cout << board[i][j];
                }
                cout << endl;
            }
        }
        // The second one
        static void printBoard(Grid<bool> board){
            for (int i=0; i<board.numRows(); i++){
                for (int j=0; j<board.numCols(); j++){
                    cout << board[i][j];
                }
                cout << endl;
            }
        }

    -   The first one.

        - The first one is more efficient. But The second one is safer.

    -   The second one.

        - The second one is safer. But The first one is more efficient.

    -   Hard to say

        + Efficiency vs. safety is a classic tension in CS.


.. mchoice:: cds_intro_reference1

    What is the outcome of code?

    ::

        Map<string,Vector<int>> mymap; 

        Vector<int> numbers; 
        numbers.add(1); 
        numbers.add(2); 
        numbers.add(3); 

        mymap["123"] = numbers; 

        mymap["123"].add(4);  
        cout << “New size: " << mymap["123"].size() << endl;

    -   3

        - Wrong! Take notice of it, it is returning a reference

    -   4

        + Correct! Returning a reference

    -   Error

        - Wrong! 

    -   Other

        - Wrong! 


.. mchoice:: cds_intro_reference2

    What is the outcome of code?

    ::

        Map<string,Vector<int>> mymap; 

        Vector<int> numbers; 
        numbers.add(1); 
        numbers.add(2); 
        numbers.add(3); 

        mymap["123"] = numbers; 

        Vector<int> plainTest = mymap["123"]; 
        plainTest.add(4);

        cout << “New size: " << mymap["123"].size() << endl;

    -   3

        + Correct! 

    -   4

        - Wrong! The outcome is about mymap but not plainTest.

    -   Error

        - Wrong! 

    -   Other

        - Wrong! 


.. mchoice:: cds_intro_reference3

    What is the outcome of code?

    ::

        Map<string,Vector<int>> mymap; 

        Vector<int> numbers; 
        numbers.add(1); 
        numbers.add(2); 
        numbers.add(3); 

        mymap["123"] = numbers; 

        Vector<int> plainTest = mymap["123"]; 
        referenceTest.add(4);

        cout << “New size: " << mymap["123"].size() << endl;

    -   3

        - Wrong! 

    -   4

        + Correct! 

    -   Error

        - Wrong! 

    -   Other

        - Wrong! 

.. mchoice:: cds_intro_pointer

    What is the correct picture?

    ::

        head->next->next = new ListNode;

        head->next->next->data = 40;

       .. figure:: Figures/pointer-before.jpg
           :width: 200px
           :align: pointer-before
           :figclass: align-center
       
    -   .. figure:: Figures/pointer-after1.jpg
           :width: 200px
           :align: pointer-before
           :figclass: align-center

        - Wrong! 

    -   .. figure:: Figures/pointer-after2.jpg
           :width: 200px
           :align: pointer-before
           :figclass: align-center

        + Correct! 

    -   Using “next” that is NULL gives an error 

        - Wrong! 

.. mchoice:: cds_intro_reference1

    What is the outcome of code?

    ::

        Map<string,Vector<int>> mymap; 

        Vector<int> numbers; 
        numbers.add(1); 
        numbers.add(2); 
        numbers.add(3); 

        mymap["123"] = numbers; 

        mymap["123"].add(4);  
        cout << “New size: " << mymap["123"].size() << endl;

    -   3

        - Wrong! Take notice of it, it is returning a reference

    -   4

        + Correct! Returning a reference

    -   Error

        - Wrong! 

    -   Other

        - Wrong! 

.. mchoice:: cds_intro_inherMammel

    What is printed?
    Siamese * s = new Siamese; 
    cout << s->toString();   

    ::

        class Mammal {
        public:
          virtual void makeSound() = 0;           string toString() { return “Mammal”; }         };
        class Cat : public Mammal {          public:            virtual void makeSound() { cout << “rawr” << endl; }
          string toString() { return “Cat”; }         };         class Siamese : public Cat {
        public:
          virtual void makeSound() { cout << “meow” << endl; }
          string toString() { return “Siamese”; }         };

    -   “Mammal”

        - Wrong! 

    -   “Cat”

        - Wrong! 

    -   “Siamese”

        + Correct!

    -   Gives an error

        -  Wrong! 

.. mchoice:: cds_intro_inherMammel2

    What is printed?
    Cat * c = new Siamese; 
    cout << c->toString();  

    ::

        class Mammal {
        public:
          virtual void makeSound() = 0;           string toString() { return “Mammal”; }         };
        class Cat : public Mammal {          public:            virtual void makeSound() { cout << “rawr” << endl; }
          string toString() { return “Cat”; }         };         class Siamese : public Cat {
        public:
          virtual void makeSound() { cout << “meow” << endl; }
          string toString() { return “Siamese”; }         };

    -   “Mammal”

        - Wrong! 

    -   “Cat”

        + Correct!

    -   “Siamese”

        - Wrong! 

    -   Gives an error

        -  Wrong! 

.. mchoice:: cds_intro_inherMammel3

    What is printed?
    Cat * c = new Siamese; 
    c->makeSound();  

    ::

        class Mammal {
        public:
          virtual void makeSound() = 0;           string toString() { return “Mammal”; }         };
        class Cat : public Mammal {          public:            virtual void makeSound() { cout << “rawr” << endl; }
          string toString() { return “Cat”; }         };         class Siamese : public Cat {
        public:
          virtual void makeSound() { cout << “meow” << endl; }
          string toString() { return “Siamese”; }         };

    -   “rawr”

        - Wrong! 

    -   “meow”

        + Correct!

    -   “Siamese”

        - Wrong! 

    -   Gives an error

        - Wrong! 

  .. mchoice:: cds_intro_design

    Which best explains good design of destructors in polymorphic classes?  


    -   Destructors are specific to each class, so we don’t need to apply virtual to them

        -  Wrong!

    -   Destructors should be virtual or we will cause a memory leak in cases like this: “DerivedType obj = new DerivedType(); delete obj;”

        -  Wrong!

    -   Destructors should be virtual or we will cause a memory leak in cases like this: “BaseType obj = new DerivedType(); delete obj;”

        + Correct! C++ style rule always make destructor virtual.

    -   Both B and C

        -  Wrong!