Accumulation Test ZAF - 1
=========================

============== ===================
checksum32     3_467_869_817      
date           2022-05-08T14:37:27
engine_version 3.11.4             
============== ===================

num_sites = 1, num_levels = 20, num_rlzs = 4

Parameters
----------
=============================== ======================================
calculation_mode                'event_based'                         
number_of_logic_tree_samples    4                                     
maximum_distance                {'default': [(1.0, 300), (10.0, 300)]}
investigation_time              1.0                                   
ses_per_logic_tree_path         10000                                 
truncation_level                3.0                                   
rupture_mesh_spacing            5.0                                   
complex_fault_mesh_spacing      10.0                                  
width_of_mfd_bin                0.1                                   
area_source_discretization      5.0                                   
pointsource_distance            None                                  
ground_motion_correlation_model None                                  
minimum_intensity               {}                                    
random_seed                     1                                     
master_seed                     0                                     
ses_seed                        42                                    
=============================== ======================================

Input files
-----------
======================= ==============================
Name                    File                          
======================= ==============================
gsim_logic_tree         `gmmLT.xml <gmmLT.xml>`_      
job_ini                 `job_vs30.ini <job_vs30.ini>`_
site_model              `sites1.csv <sites1.csv>`_    
source_model_logic_tree `ssmLT.xml <ssmLT.xml>`_      
======================= ==============================

Composite source model
----------------------
====== ==================== =========
grp_id gsim                 rlzs     
====== ==================== =========
0      '[AkkarEtAlRjb2014]' [0]      
1      '[AkkarEtAlRjb2014]' [0, 1]   
2      '[AkkarEtAlRjb2014]' [0, 1, 2]
3      '[AkkarEtAlRjb2014]' [0, 1, 3]
4      '[AkkarEtAlRjb2014]' [0, 2, 3]
5      '[AkkarEtAlRjb2014]' [0, 3]   
6      '[AkkarEtAlRjb2014]' [1]      
7      '[AkkarEtAlRjb2014]' [2]      
8      '[AkkarEtAlRjb2014]' [2, 3]   
9      '[AkkarEtAlRjb2014]' [3]      
====== ==================== =========

Required parameters per tectonic region type
--------------------------------------------
===== ========================================== ========= ========== ==========
et_id gsims                                      distances siteparams ruptparams
===== ========================================== ========= ========== ==========
0     '[AkkarEtAlRjb2014]' '[BooreAtkinson2008]' rjb       vs30       mag rake  
1     '[AkkarEtAlRjb2014]' '[BooreAtkinson2008]' rjb       vs30       mag rake  
2     '[AkkarEtAlRjb2014]' '[BooreAtkinson2008]' rjb       vs30       mag rake  
3     '[AkkarEtAlRjb2014]' '[BooreAtkinson2008]' rjb       vs30       mag rake  
===== ========================================== ========= ========== ==========

Slowest sources
---------------
========= ==== ========= ========= ============
source_id code calc_time num_sites eff_ruptures
========= ==== ========= ========= ============
========= ==== ========= ========= ============

Computation times by source typology
------------------------------------
==== ========= ========= ============
code calc_time num_sites eff_ruptures
==== ========= ========= ============
A    41        0         0           
==== ========= ========= ============

Information about the tasks
---------------------------
================== ====== ======= ====== ========= =======
operation-duration counts mean    stddev min       max    
compute_gmfs       26     0.23423 20%    0.11200   0.28704
read_source_model  22     0.00250 35%    9.928E-04 0.00499
sample_ruptures    29     1.88138 134%   0.0       7.74799
================== ====== ======= ====== ========= =======

Data transfer
-------------
================= ================================================== =========
task              sent                                               received 
read_source_model converter=6.68 KB fname=1.92 KB                    42.41 KB 
sample_ruptures   sources=131.16 KB param=95.67 KB srcfilter=42.4 KB 342.19 KB
compute_gmfs      rupgetter=205.95 KB param=80.69 KB                 104.68 KB
================= ================================================== =========

Slowest operations
------------------
========================== ======== ========= ======
calc_49, maxmem=1.8 GB     time_sec memory_mb counts
========================== ======== ========= ======
EventBasedCalculator.run   73       8.14844   1     
total sample_ruptures      54       13        30    
total compute_gmfs         6.09002  3.58203   26    
getting ruptures           4.64102  2.49219   1_558 
importing inputs           3.28786  2.11719   1     
composite source model     3.17263  1.69141   1     
saving ruptures and events 0.16697  1.46875   1     
saving gmfs                0.08703  0.13281   26    
saving avg_gmf             0.07929  0.30469   1     
total read_source_model    0.05497  1.44922   22    
saving ruptures            0.03600  0.07422   10    
aggregating hcurves        0.00200  0.0       26    
========================== ======== ========= ======