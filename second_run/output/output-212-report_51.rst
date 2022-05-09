Accumulation Test ZAF - 2
=========================

============== ===================
checksum32     3_467_869_817      
date           2022-05-09T16:47:31
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
site_model              `sites2.csv <sites2.csv>`_    
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
A    38        0         0           
==== ========= ========= ============

Information about the tasks
---------------------------
================== ====== ======= ====== ========= =======
operation-duration counts mean    stddev min       max    
compute_gmfs       26     0.22604 20%    0.08802   0.27033
read_source_model  22     0.00231 36%    8.140E-04 0.00400
sample_ruptures    29     1.72631 139%   0.0       7.88054
================== ====== ======= ====== ========= =======

Data transfer
-------------
================= ================================================== =========
task              sent                                               received 
read_source_model converter=6.68 KB fname=1.7 KB                     42.19 KB 
sample_ruptures   sources=131.16 KB param=94.25 KB srcfilter=42.4 KB 350.92 KB
compute_gmfs      rupgetter=210.43 KB param=79.42 KB                 106.83 KB
================= ================================================== =========

Slowest operations
------------------
========================== ======== ========= ======
calc_51, maxmem=1.8 GB     time_sec memory_mb counts
========================== ======== ========= ======
EventBasedCalculator.run   71       8.25391   1     
total sample_ruptures      50       12        30    
total compute_gmfs         5.87692  3.46875   26    
getting ruptures           4.47500  1.92969   1_599 
importing inputs           2.86926  2.62891   1     
composite source model     2.78403  1.93359   1     
saving ruptures and events 0.17696  1.36328   1     
saving gmfs                0.08326  0.17578   26    
total read_source_model    0.05091  0.88672   22    
saving ruptures            0.03375  0.07422   10    
saving avg_gmf             0.03036  0.36719   1     
aggregating hcurves        0.00304  0.0       26    
========================== ======== ========= ======