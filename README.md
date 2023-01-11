# Introduction 簡介
This repository contain important code used in my master thesis: *"Information Synergy Contributed to Anticipatory Dynamics in Retina"*. About the details of thesis, please see the abstract PDF file or check the link down below. Most of the codes herein are written by me.<br>
In my study, activities of RGC were recorded in \*.mcd files, which then were converted into MATLAB files. Some basic analysis were also done using MATLAB. I used Python (and Jupyter Notebook) to analyze the experimental data and in simulation. However, in this repository, only code in Python were included.<br>
此資料庫為我的碩論--*「資訊協同對視網膜預測能力的貢獻」*--研究中主要所使用到的程式碼。關於論文請查閱摘要PDF檔或使用下方的連結。多數程式碼皆為本人所寫。研究中，MATLAB用於訊號的處理與一些基礎的分析，Python用於分析與模擬，此資料庫僅包含python程式碼。

# Experimental Data
There are two experimental setup in my thesis, with and without spatial dependency. All data herein were pre-processed by MATLAB (and other commercial software).
## In LED_Data
In this folder, all files (\*.mat) are the recording data, comprising RGC spike trains and the stimulus series.
## In OLED_Data
* `fitNGD2LASpara.npz`: Fitting result of the temporal kernel (TK) of the model to experimental data. Obtained from the code `CalculateandFit_TK.ipynb`.
* `RF_properties.mat`: Size and center of the receptive field of RGCs, obtained from a MATLAB code that was not included herein.
* `oled_boundary_set.mat`: Some basic feature of the stimulus spatial pattern: dynamic range, size of the moving bar on the OLED display, etc.
* Other files (\*.mat): Recording data, which comprise RGC spike trains and the stimulus series.

# Code Files
## Modules
* `BROJA_2PID.py`: Adopted from Makkeh et al. (2018). https://dx.doi.org/10.3390/e20040271; for PID.
* `GenerateOUStimulus.ipynb`: Generate OU (and LPOU) series.
* `Spike_Generation.ipynb`: Nonlinear and random parts of Model. Generate model spikes.
* `time_shifted_PID.ipynb`: Function for calculate PID (MI).
## Code for Figures in the Thesis
* `MInPI.ipynb`: Calculate MI and PI (from PID of MI). Associated with Figure 3.7 and 3.8 (a) in the thesis.
* `STA.ipynb`: Calculate STA. Associated with Figure 3.11.
* `STKnSVD.ipynb`: Calculate spatial temporal kernel (STK) of retina; extract SK from STK via SVD.
* `CalculateandFit_TK.ipynb`: Calculate the TK of RGCs. Fit the analytic solution of model TK with the TK of RGC. Associated with Figure 3.1.
* `NGD1D_Model.ipynb`: This model were built by referring the STK of an mP-RGC. The model kernels are shown in the file. Furthermore, they were used to generate spikes with stimulus similar to that in the experiment. Associated with Figure 3.6 and 3.16.


# Link of My Thesis
`Information Synergy Contributed to Anticipatory Dynamics in Retina` <br>
`資訊協同對視網膜預測能力的貢獻` <br>
https://www.airitilibrary.com/Publication/alDetailedMesh1?DocID=U0001-0608202120313100 <br>
doi:10.6342/NTU202102163

# Contributor
Lin, Qi-Rong 林其融  <br>
Department of Physics, National Taiwan University, Taiwan (ROC); <br>
Institution of Physics, Academia Sinica, Taiwan (ROC)

* Apache License 2.0  @llincooi
