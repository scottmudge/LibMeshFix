## MeshFIX - Version 2.1 (libMeshFix refactored by Scott Mudge)                                                         

by Marco Attene
                                                                    
Consiglio Nazionale delle Ricerche                                        
Istituto di Matematica Applicata e Tecnologie Informatiche                
Sezione di Genova                                                         
IMATI-GE / CNR                                                            
                                                                         
This software takes as input a polygon mesh and produces a copy of the input where all the occurrences of a specific set of "defects" are corrected. MeshFix has been designed to correct typical flaws present in RAW DIGITIZED mesh models, thus it might fail or produce coarse results if run on other sorts of input meshes (e.g. tessellated CAD models). When the software fails, it appends a textual description to the file "meshfix.log".

### Algorithm and Citation Policy

To better understand how the algorithm works, please refer to the following paper:

   M. Attene.
   A lightweight approach to repairing digitized polygon meshes.
   The Visual Computer, 2010. (c) Springer. DOI: 10.1007/s00371-010-0416-3

This software is based on ideas published therein. If you use MeshFix for research purposes you should cite the above paper in your published results. MeshFix cannot be used for commercial purposes without a proper licensing contract.

### Parameters
The user may want to force the software to join the connected components [-a] whose boundary loops are closer to each other. Otherwise, only the largest component is kept while the others are considered as "noise". By default, the output file is in OFF format. The user may change this to STL [-j]. If the software is run as part of a script that processes all the files in a directory, the parameter [-x] may be useful to avoid to re-run the repairing of a mesh if its result already exists as a file.

### Source Code

From version 2.0 MeshFix is self-contained, that is, it does not depend on any other software.
To compile the source code on Windows you need Microsoft Visual C++ 2013 or newer.
Just click on vc12/MeshFix_All.sln and hit F7.
The executable will be saved in bin/.

Both 32bit and 64bit versions can be produced.

The source code is standard ANSI C++ and should be portable.
To compile on other configurations you may use CMake (thanks to Jeremie Dumas for having created the CMakeLists!).

### Copyright

MeshFix is

Copyright(C) 2010: IMATI-GE / CNR                                       

All rights reserved.                                                      
                                                                  
This program is dual-licensed as follows:

(1) You may use MeshFix as free software; you can redistribute it and/or
modify it under the terms of the GNU General Public License as published 
by the Free Software Foundation; either version 3 of the License, or     
(at your option) any later version.                                      
In this case the program is distributed in the hope that it will be      
useful, but WITHOUT ANY WARRANTY; without even the implied warranty of   
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the            
GNU General Public License (http://www.gnu.org/licenses/gpl.txt)         
for more details.                                                        
                                                                         
(2) You may use MeshFix as part of a commercial software. In this case a
proper agreement must be reached with the Authors and with IMATI-GE/CNR  
based on a proper licensing contract.
