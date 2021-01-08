Structural Hole Spanners
========================
EasyGraph has implemented several most commonly used structural holes spanners detection methods, including HIS, MaxD, HAM, Common_Greedy,  AP_Greedy. 
Burt's evaluation metric for structural holes, Effective Size, Efficiency, Constraint and Hierarchy, are also included. 

HIS
---
.. automodule:: easygraph.functions.structural_holes.HIS
.. autosummary::
    :toctree: generated/

    get_structural_holes_HIS

MaxD
----
.. automodule:: easygraph.functions.structural_holes.MaxD
.. autosummary::
    :toctree: generated/

    get_structural_holes_MaxD

AP_Greedy
---------
.. automodule:: easygraph.functions.structural_holes.AP_Greedy
.. autosummary::
    :toctree: generated/

    common_greedy
    AP_Greedy

HAM
---
.. automodule:: easygraph.functions.structural_holes.HAM
.. autosummary::
    :toctree: generated/

    get_structural_holes_HAM


Burt's Metrics
--------------
.. automodule:: easygraph.functions.structural_holes.evaluation
.. autosummary::
    :toctree: generated/

    effective_size
    efficiency
    constraint
    hierarchy
    
