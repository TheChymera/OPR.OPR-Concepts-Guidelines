:author: Horea Christian
:email: r.chr@mail.ru
:institution: Heidelberg University Interdisciplinary Center for Neurosciences 


----
Concepts and Guidelines for an “Open Publication Revision” System
----

.. class:: abstract

   Currently, journals use peer review of context-data-evaluation-discussion monoliths to make a go/no-go choice regarding publication. We propose a non-binary model which harnesses the power of open collaboration, immediate publication, and transparent revision. We name this model, accordingly, Open Publication Revision (OPR). We believe that the worthiness of findings is never static, and can only be interpreted in light of their ability to support further developments. The delineated system is tailored to add value even to the least promising publications, rather than derive value for itself from the most promising ones. We believe our system would provide an immediate service to the scientific community by making otherwise lost findings viable.

.. class:: keywords

   publishing, github, open revision, open peer review

Background
----

Peer review is a widely acclaimed procedure for quality control, the principle of which has circulated in human societies for millennia [Spi02]_.
Its rationale is both solid and simple: Only people familiar with a certain part of the knowledge network can decide whether and how a new part fits in. 

The exact implementation of peer review in the context of publishing has changed in accordance with the technological possibilities of the time \cite{Spier2002}, the most recent notable changes including online publishing and review, and the more controversial open access publishing\cite{VanNoorden2013,Parker2013} and open peer review.
While open access seems to have gained a foothold in the scientific community (notably demonstrated by the recent success of the Public Library of Science journals), the same cannot be said of open peer review.

Many opinion and research articles concern themselves with the benefits\cite{Leek2011,Mainguy2005} and the applicability\cite{vanRooyen1999,vanRooyen2010} of open peer review. 
It should be noted, however, that this is but the most prominent of many incentives to change peer review.
A landmark of the discussion of modern publishing was \textit{Nature}'s 2006 series on the trial and debate of peer review \cite{Nature-debate2006}.
The debate illustrates that the scientific community is bursting with ideas regarding the future of publishing. 
Some of the articles also show how novel systems have already been implemented \cite{Riley2006,Sandewall2006,Koop2006}, and how one in particular, arXiv\cite{arXiv}, has even become a standard in a number of fields.

The article series shows that seasoned members of the scientific publishing community are vividly aware of a great many shortcomings of current knowledge mediation in general and peer review in particular.
Such disappointments, complemented by many others, are also shared by less established authors \cite{Mainguy2005}.


Of course, no paper would be complete without some source code.  Without
highlighting, it would look like this::

   def sum(a, b):
       """Sum two numbers."""

       return a + b

With code-highlighting:

.. code-block:: python

   def sum(a, b):
       """Sum two numbers."""

       return a + b

Maybe also in another language, and with line numbers:

.. code-block:: c
   :linenos:

   int main() {
       for (int i = 0; i < 10; i++) {
           /* do something */
       }
       return 0;
   }

Or a snippet from the above code, starting at the correct line number:

.. code-block:: c
   :linenos:
   :linenostart: 2

   for (int i = 0; i < 10; i++) {
       /* do something */
   }
 
Important Part
--------------

It is well known [Atr03]_ that Spice grows on the planet Dune.  Test
some maths, for example :math:`e^{\pi i} + 3 \delta`.  Or maybe an
equation on a separate line:

.. math::

   g(x) = \int_0^\infty f(x) dx

or on multiple, aligned lines:

.. math::
   :type: eqnarray

   g(x) &=& \int_0^\infty f(x) dx \\
        &=& \ldots


The area of a circle and volume of a sphere are given as

.. math::
   :label: circarea

   A(r) = \pi r^2.

.. math::
   :label: spherevol

   V(r) = \frac{4}{3} \pi r^3

We can then refer back to Equation (:ref:`circarea`) or
(:ref:`spherevol`) later.

Mauris purus enim, volutpat non dapibus et, gravida sit amet sapien. In at
consectetur lacus. Praesent orci nulla, blandit eu egestas nec, facilisis vel
lacus. Fusce non ante vitae justo faucibus facilisis. Nam venenatis lacinia
turpis. Donec eu ultrices mauris. Ut pulvinar viverra rhoncus. Vivamus
adipiscing faucibus ligula, in porta orci vehicula in. Suspendisse quis augue
arcu, sit amet accumsan diam. Vestibulum lacinia luctus dui. Aliquam odio arcu,
faucibus non laoreet ac, condimentum eu quam. Quisque et nunc non diam
consequat iaculis ut quis leo. Integer suscipit accumsan ligula. Sed nec eros a
orci aliquam dictum sed ac felis. Suspendisse sit amet dui ut ligula iaculis
sollicitudin vel id velit. Pellentesque hendrerit sapien ac ante facilisis
lacinia. Nunc sit amet sem sem. In tellus metus, elementum vitae tincidunt ac,
volutpat sit amet mauris. Maecenas diam turpis, placerat at adipiscing ac,
pulvinar id metus.

.. figure:: figure1.png

   This is the caption. :label:`egfig`

.. figure:: figure1.png
   :align: center
   :figclass: w

   This is a wide figure, specified by adding "w" to the figclass.  It is also
   center aligned, by setting the align keyword (can be left, right or center).

.. figure:: figure1.png
   :scale: 20%
   :figclass: bht

   This is the caption on a smaller figure that will be placed by default at the
   bottom of the page, and failing that it will be placed inline or at the top.
   Note that for now, scale is relative to a completely arbitrary original
   reference size which might be the original size of your image - you probably
   have to play with it. :label:`egfig2`

As you can see in Figures :ref:`egfig` and :ref:`egfig2`, this is how you reference auto-numbered
figures.

.. table:: This is the caption for the materials table. :label:`mtable`

   +------------+----------------+
   | Material   | Units          |
   +------------+----------------+
   | Stone      | 3              |
   +------------+----------------+
   | Water      | 12             |
   +------------+----------------+
   | Cement     | :math:`\alpha` |
   +------------+----------------+


We show the different quantities of materials required in Table
:ref:`mtable`.


.. The statement below shows how to adjust the width of a table.

.. raw:: latex

   \setlength{\tablewidth}{0.8\linewidth}


.. table:: This is the caption for the wide table.
   :class: w

   +--------+----+------+------+------+------+--------+
   | This   | is |  a   | very | very | wide | table  |
   +--------+----+------+------+------+------+--------+


Perhaps we want to end off with a quote by Lao Tse:

  *Muddy water, let stand, becomes clear.*


.. Customised LaTeX packages
.. -------------------------

.. Please avoid using this feature, unless agreed upon with the
.. proceedings editors.

.. ::

..   .. latex::
..      :usepackage: somepackage

..      Some custom LaTeX source here.

References
----------
.. [Atr03] P. Atreides. *How to catch a sandworm*,
           Transactions on Terraforming, 21(3):261-300, August 2003.


.. [Spi02] R. Spier. *The History of the Peer Review Process*,
           Trends Biotechnol, 20(8):357-358, August 2002.
