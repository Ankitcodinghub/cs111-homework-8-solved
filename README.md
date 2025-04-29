# cs111-homework-8-solved
**TO GET THIS SOLUTION VISIT:** [CS111 Homework 8 Solved](https://www.ankitcodinghub.com/product/cs111-submit-your-paper-as-one-pdf-file-and-tell-gradescope-which-pages-each-problem-is-on-if-you-worked-with-a-partner-you-must-each-turn-in-your-own-homework-paper-and-report-the-name-and-pe-7/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;115138&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CS111 Homework 8 Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (1 vote)    </div>
    </div>
1. The temperature matrix is almost but not quite a Laplacian matrix: It is symmetric, all its offdiagonal elements are either 0 or −1, and most of its row sums are 0. What’s the smallest number of nonzero elements of the 2D temperature matrix with n = 10,000 (so k = 100) that you would need to change to make it into the Laplacian matrix of some graph? Which nonzero elements would need to be changed? Describe in words what graph that is: How many vertices does it have, and what is the pattern of its edges?

2. The graph partitioning problem is: Given an undirected graph G with n vertices, divide the vertices into two groups of equal size n/2 (or, if n is odd, sizes (n + 1)/2 and (n − 1)/2), with as few edges as possible between vertices in different groups. Another way to say this is, color half the vertices red and half the vertices blue while making the number of edges with one red endpoint and one blue endpoint as small as possible. Graph partitioning is used in algorithms for parallel computers, where you might have two processors cooperating to solve a problem on a big graph; each processor gets half the graph, and the cost of communication between the processors depends on the number of edges joining the two halves. The figure below shows two ways to partition a 48-vertex graph, one cutting 20 edges and one cutting 18 edges.

Figure 1: Geometric partition of 48-vertex graph Figure 2: Spectral partition of 48-vertex graph

In this problem you will experiment with a graph called “airfoil1” that comes from a finite element mesh discretizing the space surrounding a 2-dimensional slice of an airplane wing and its flaps. Both the airfoil graph “airfoil1” and the 48-vertex graph “mesh1e1” are in the Homework/h08/ directory on GitHub. That directory also contains a Jupyter notebook with some helpful routines to read in graphs in this format and draw them. You will probably want to use a smaller value for the node size parameter with the airfoil than I did with the 48-vertex graph.

1

2.1. We can describe a partition by labeling each vertex with either a 1 or a −1, depending on which part it’s in. Define a cut vector as an n-vector x whose elements are all either 1 or −1. How many edges cross the cut? The Laplacian quadratic form xT Lx gives the answer.

Use the formula for the Laplacian quadratic form (which I’ll derive in class this week),

xT Lx = X (xi − xj)2,

(i,j)∈E

to prove (give a mathematical argument) that the number of edges that cross any cut in any graph is equal to α · xT Lx, where L is the Laplacian matrix of the graph, x is the cut vector, and α is a fixed constant independent of the graph or the cut. What is the value of α?

2.2. A coordinate cut is a partition based on a drawing of a graph in the plane, which colors vertices according to the value of one of their coordinates, depending on whether the vertex’s coordinate is less than or greater than the median coordinate. The 20-edge cut in Figure 1 is a y-coordinate cut of the 48-vertex graph.

Find a y-coordinate cut of the airfoil mesh from GitHub, make a drawing of it similar to Figure 1, and compute the number of edges that cross the cut by using the Laplacian quadratic form.

2.3. A spectral cut is a partition based on the eigenvectors of the Laplacian matrix. The 18-edge cut in Figure 2 is a spectral cut of the 48-vertex graph. We’ll see in class that the second-smallest eigenvalue λ1 is zero if the graph is not connected. If the graph is connected, it turns out that the size of λ1 is related to how many edges need to be cut to partition the graph, and that the entries in the corresponding eigenvector w1 can be used to find a good partition. (The second eigenvalue and eigenvector of a graph Laplacian, λ1 and w1, are called the Fiedler value and the Fiedler vector of the graph, after the mathematician Miroslav Fiedler.) The idea is similar to a coordinate cut: Label each vertex with the corresponding element of the Fiedler vector w1, and choose the part it’s in based on whether its label is smaller or larger than the median element of the Fiedler vector.

Compute the Fiedler value and Fiedler vector for the airfoil graph, and use them to find a spectral cut of the airfoil. Again, make a drawing of it similar to Figure 2, and compute the number of edges that cross the cut by using the Laplacian quadratic form.

2
