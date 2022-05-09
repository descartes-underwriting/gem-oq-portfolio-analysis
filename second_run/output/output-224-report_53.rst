Accumulation Test ZAF - 2
=========================

============== ===================
checksum32     3_467_869_817      
date           2022-05-09T19:01:48
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
ses_seed                        2                                     
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
A    40        0         0           
==== ========= ========= ============

Information about the tasks
---------------------------
================== ====== ======= ====== ========= =======
operation-duration counts mean    stddev min       max    
compute_gmfs       27     0.24731 32%    0.01337   0.31063
read_source_model  22     0.00252 56%    7.789E-04 0.00799
sample_ruptures    29     1.84703 138%   0.0       8.18779
================== ====== ======= ====== ========= =======

Data transfer
-------------
================= ================================================== =========
task              sent                                               received 
read_source_model converter=6.68 KB fname=1.83 KB                    42.32 KB 
sample_ruptures   sources=131.16 KB param=95.21 KB srcfilter=42.4 KB 368.39 KB
compute_gmfs      rupgetter=220.87 KB param=83.37 KB                 111.61 KB
================= ================================================== =========

Slowest operations
------------------
========================== ======== ========= ======
calc_53, maxmem=1.8 GB     time_sec memory_mb counts
========================== ======== ========= ======
EventBasedCalculator.run   74       9.03125   1     
total sample_ruptures      53       11        30    
total compute_gmfs         6.67744  3.12500   27    
getting ruptures           5.12200  2.05859   1_682 
importing inputs           2.94650  2.67578   1     
composite source model     2.85954  1.89062   1     
saving ruptures and events 0.17710  2.12500   1     
saving gmfs                0.09868  0.11328   27    
total read_source_model    0.05544  1.33203   22    
saving avg_gmf             0.03432  0.30078   1     
saving ruptures            0.03428  0.08594   10    
aggregating hcurves        0.00145  0.0       27    
========================== ======== ========= ======