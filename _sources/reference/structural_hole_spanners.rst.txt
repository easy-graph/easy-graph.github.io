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

ICC
---------
.. automodule:: easygraph.functions.structural_holes.ICC
.. autosummary::
    :toctree: generated/

    ICC
    BICC
    AP_BICC

HAM
---
.. automodule:: easygraph.functions.structural_holes.HAM
.. autosummary::
    :toctree: generated/

    get_structural_holes_HAM


NOBE
--------------
.. automodule:: easygraph.functions.structural_holes.NOBE
.. autosummary::
    :toctree: generated/

    NOBE_SH
    NOBE_GA_SH


WeakTie
--------------
.. automodule:: easygraph.functions.structural_holes.weakTie
.. autosummary::
    :toctree: generated/

    weakTie
    weakTieLocal

Burt's Metrics
--------------
.. automodule:: easygraph.functions.structural_holes.evaluation
.. autosummary::
    :toctree: generated/

    effective_size
    efficiency
    constraint
    hierarchy
    
