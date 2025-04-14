Multiple Choice Exercises
-------------------------

Answer the following **Multiple Choice** questions to
assess what you have learned in this chapter.


.. mchoice:: cds_graph_ways
   :author: Cynthia Lee

     How many of the following are true?

    
    -   Adjacency list can be used for directed graphs

         - Wrong!

    -   Adjacency list can be used for undirected graphs

         + Correct!

    -   Adjacency matrix can be used for directed graphs

         - Wrong!

    -   Adjacency matrix can be used for undirected graphs

         - Wrong!

    

 .. mchoice:: cds_graph_Eulerian
   :author: Cynthia Lee

    Is this graph Eulerian?

    .. figure:: Figures/Eulerian1.jpg
        :width: 200px
        :align: center
        :alt: Harsh_Eulerian
        :figclass: align-center
    
    -   yes

        - Wrong! 

    -  no

         + Correct! 

 .. mchoice:: cds_graph_Eulerian2
   :author: Cynthia Lee

    Is this graph Eulerian?

    .. figure:: Figures/Eulerian2.jpg
        :width: 200px
        :align: center
        :alt: Harsh_Eulerian
        :figclass: align-center
    
    -   yes

        + Correct! 

    -  no
        - Wrong! 

.. mchoice:: cds_graph_search
   :author: Cynthia Lee

   You predict the next step!

    .. figure:: Figures/search.jpg
        :width: 200px
        :align: center
        :alt: Harsh_Eulerian
        :figclass: align-center
    
    -   K’s neighbors F,G,H are yellow and enqueued and their pare

        + Correct! 

    -  K’s neighbors G,H are yellow and enqueued and their parents are pointing to K

        - Wrong! 

.. mchoice:: cds_graph_eff
   :author: Cynthia Lee

   You calculated the shortest path for yourself (Yosemite to Palo Alto) and let’s just say that it took time X = O((|E| + |V|)log|V|)
   How long will it take you, in total, to calculate the shortest path for ALL of your relatives?
    
    -   O(|V|*X)

        + Correct! 

    -  O(|E|*|V|* X)

        - Wrong! 

.. mchoice:: cds_graph_spanning
   :author: Cynthia Lee

   How many distinct spanning trees are in this graph?

    .. figure:: Figures/spanning.jpg
        :width: 200px
        :align: center
        :alt: graph-trees
        :figclass: align-center
    
    -   0-1

        - Wrong!

    -  2-3

        - Wrong!

    -  4-5

        - Wrong!

    -  6-7

        - Wrong!

    -  > 7

        + Correct! 
 
.. mchoice:: cds_graph_MST
   :author: Cynthia Lee

   How many distinct MSTs are in this graph?

    .. figure:: Figures/MST.jpg
        :width: 200px
        :align: center
        :alt: graph-trees
        :figclass: align-center
    
    -   0-1

        - Wrong!

    -  2-3

        - Wrong!

    -  4-5

        + Correct! 

    -  6-7

        - Wrong!

    -  > 7

        - Wrong!        
   
.. mchoice:: cds_graph_tf
   :author: Cynthia Lee

   Having at least two edges with the same weight is SUFFICIENT for having more than one distinct minimum spanning tree.
    
    -   TRUE

        - Wrong!

    -  FALSE

        + Correct! i.e., “If at least two edges have the same weight, then there is more than one MST”

.. mchoice:: cds_graph_tf2

   Having at least two edges with the same weight is NECESSARY for having more than one distinct minimum spanning tree.
    
    -   TRUE

        + Correct! i.e., “If there is more than one MST, then at least two edges have the same weight.”

    -  FALSE

        - Wrong!
