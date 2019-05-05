# Sepia (SuscEptibility mapping PIpeline tool for phAse images)

![sepia logo](https://github.com/kschan0214/sepia/blob/master/logo/sepia.png?raw=true)

## Introduction  

**Sepia** is a tool providing a graphical user interface to build data processing pipeline of quantitative susceptibility mapping (QSM) in Matlab.

This GUI is built based on three toolboxes including [MEDI](http://weill.cornell.edu/mri/pages/qsm.html), [STI Suite](https://people.eecs.berkeley.edu/~chunlei.liu/software.html) and [FANSI](https://gitlab.com/cmilovic/FANSI-toolbox).

**Sepia** provides two key features for QSM processing:  
1. mix-and-match methods from different toolboxes to build your own QSM processing pipeline,
2. graphical user interface to easily adjust parameters of different algorithms.

The objective of **Sepia** is to provide a platform for easy access of different QSM processing methods in the field. To achieve this, most of the codes were written for data flow and algorithm parameter control. Through **Sepia**, I hope researchers who are not expert in QSM would also be able to use QSM for their research. The instruction of this toolbox can be found in the [wiki page](https://github.com/kschan0214/sepia/wiki)

Please report to me if you encounter any bug when using the tool.

## Terms of use
All the codes and methods developed by me in **Sepia** are under MIT license. You can check [the license file](https://github.com/kschan0214/Sepia/blob/master/LICENSE) for more information. For the terms of use of the toolboxes related to this work, their own license applied and please check the corresponding license file(s) in each toolbox for more information. 

When you use **Sepia** in your research, please cite the related papers of the methods in your processing pipeline. 

If you have any question or you would like to provide suggestion to improve this toolbox/report bug(s) please feel free to contact me k.chan@donders.ru.nl (Kwok-Shing Chan) directly or raise an issue in the [github page](https://github.com/kschan0214/sepia/issues).

Kwok  
2018-09-01


## Update notes  

### Future release
* Incorporating new version of MEDI toolbox (updated April 9, 2019)

### 0.7.1 (20190416)
* Support simple susceptibility weighted imaging (SWI) and susceptibility map weighted imaging (SMWI) as part of the GUI
* resolved loading/saving NIfTI issue related to 0.7.0 update
* DICOM input is deprecated: the only possible input is NIfTI data
* fixed bug when running MEDI with CSF regularisation
* fixed bug for single echo SWI
* now support automatic magnitude and phase images detection with name containing string "mag" for magnitude image and "ph" for phase image  

### 0.7.0 (20190412)
* redesigned log file format; the algorithms and parameters being used are much clearer adn neat than before (previous log file cannot work in this version)
* resolved '.nii.nii' issue when using STI suite algorithms
* resolved no. of iterations with FANSI does not change issue
* resolved problematic QSM results with FANSI when the input matrix is odd number
* resolved excluded unreliable voxels issue when 3D best path algorithm doesn't work
* improved build-in VSHARP results when there is masked voxels on the image edges
* added image erosion function for background field removal algorithms
* get header function is now compartible with the JSON files generated by dcm2niix and dicm2nii

### 0.6.0 (20180901)  
* updated diretcory structure
* added options to select individual files  


