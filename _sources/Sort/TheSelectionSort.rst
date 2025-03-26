..  Copyright (C)  Brad Miller, David Ranum, and Jan Pearce
    This work is licensed under the Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License. To view a copy of this license, visit http://creativecommons.org/licenses/by-nc-sa/4.0/.


The Selection Sort
~~~~~~~~~~~~~~~~~~

The **selection sort** improves on the bubble sort by making only one
exchange for every pass through the first part of the vector.
We will call this a step.
In order to do this, a
selection sort looks for the largest value as it makes a partial pass and, after
completing the partial pass, places it in the proper location, ending the step.
As with a bubble
sort, after the first step, the largest item is in the correct place.
After the second step, the next largest is in place. This process
continues and requires :math:`n-1` steps to sort *n* items, since the
final item must be in place after the :math:`(n-1)` step.

On each step,
the largest remaining item is selected and then placed in its proper
location. The first pass places 93, the second pass places 77, the third
places 55, and so on. The function is shown in :ref:`ActiveCode 1 <lst_selectionsortcode_cpp>` .

.. tabbed:: lst_selection_sort

  .. tab:: C++

    .. activecode:: lst_selectionsortcode_cpp
      :caption: The Selection Sort
      :language: cpp

      #include <iostream>
      #include <vector>
      using namespace std;
      //function that sorts through values in vector through selection sort
      vector<int> selectionSort(vector<int> avector) {
          for (int fillslot = (avector.size() - 1); fillslot >= 0; fillslot--) {
              int positionOfMax = 0;
              for (int location = 1; location < fillslot + 1; location++) {
                  if (avector[location] > avector[positionOfMax]) {
                      positionOfMax = location;
                  }
              }

              int temp = avector[fillslot];
              avector[fillslot] = avector[positionOfMax];
              avector[positionOfMax] = temp;
          }
          return avector;
      }

      int main() {
          // Vector initialized using a static array
          static const int arr[] = {54, 26, 93, 17, 77, 31, 44, 55, 20};
          vector<int> avector (arr, arr + sizeof(arr) / sizeof(arr[0]) );

          // Call to the selectionSort function
          vector<int> updatedAvector = selectionSort(avector);

          // print the vector
          for (unsigned int i = 0; i < updatedAvector.size(); i++) {
              cout << updatedAvector[i] << " ";
          }
          cout << endl;

          return 0;
      }


  .. tab:: Python

    .. activecode:: lst_selectionsortcode
        :caption: Selection Sort
        :optional:
        
        #function sorts through values in list using selection sort
        def selectionSort(alist):
           for fillslot in range(len(alist)-1,0,-1):
               positionOfMax=0
               for location in range(1,fillslot+1):
                   if alist[location]>alist[positionOfMax]:
                       positionOfMax = location

               temp = alist[fillslot]
               alist[fillslot] = alist[positionOfMax]
               alist[positionOfMax] = temp

        def main():
            alist = [54,26,93,17,77,31,44,55,20]
            selectionSort(alist)
            print(alist)
        main()

.. animation:: selection_anim
   :modelfile: sortmodels.js
   :viewerfile: sortviewers.js
   :model: SelectionSortModel
   :viewer: BarViewer


..
..
.. .. codelens:: selectionsortcodetrace
..     :caption: Tracing the Selection Sort
..
..     def selectionSort(alist):
..        for fillslot in range(len(alist)-1,0,-1):
..            positionOfMax=0
..            for location in range(1,fillslot+1):
..                if alist[location]>alist[positionOfMax]:
..                    positionOfMax = location
..
..            temp = alist[fillslot]
..            alist[fillslot] = alist[positionOfMax]
..            alist[positionOfMax] = temp
..
..     alist = [54,26,93,17,77,31,44,55,20]
..     selectionSort(alist)
..     print(alist)

This visualization allows you to step through the algorithm. Yellow bars
represent the current element, red represents the element being looked at,
and blue represents the last element to look at during a step.

The following visualization shows selection sort in action. Each pass compares the bars 
in sequential order. The smallest bar is selected on each pass and is set as the minimum, 
represented in orange. Every remaining bar is then compared to the minimum. If the bar is 
larger, it is represented in blue, if it is smaller, it becomes the new orange bar. 
After each pass, a counter will increment which bar in our container will start with. 
This increment is representedby a thin black line falling before the bar to be started at.


.. video:: vis_selection_sort
    :controls:
    :thumb: ../_static/vis_selection_sort_thumb.png

    ../_static/vis_selection_sort.webm


You may see that the selection sort makes the same number of comparisons
as the bubble sort and is therefore also :math:`O(n^{2})`. However,
due to the reduction in the number of exchanges, the selection sort
typically executes faster in benchmark studies.

.. admonition:: Self Check

   .. mchoice:: question_sort_2
      :correct: d
      :answer_a: [7, 11, 12, 1, 6, 14, 8, 18, 19, 20]
      :answer_b: [7, 11, 12, 14, 19, 1, 6, 18, 8, 20]
      :answer_c: [11, 7, 12, 14, 1, 6, 8, 18, 19, 20]
      :answer_d: [1, 6, 7, 14, 19, 11, 12, 18, 8, 20]
      :feedback_a: Selection sort is similar to bubble sort (which you appear to have done) but uses fewer swaps
      :feedback_b: This looks like an insertion sort.
      :feedback_c: This one looks similar to the correct answer, however, it is not how selection sort works. With this answer, instead of swapping values through each sweep, the values have been shifted to the left to make room for the correct numbers.
      :feedback_d: Selection sort improves upon bubble sort by making fewer swaps.

      Suppose you have the following vector of numbers to sort:
      [11, 7, 12, 14, 19, 1, 6, 18, 8, 20] which vector represents the partially sorted (ascending) vector after three steps of selection sort?
