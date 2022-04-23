# mhd-acqisition-and-processing

LabVIEW code of the data acquisition and signal processing in the multiple harmonic detection (MHD) method for continuous-wave electron paramagnetic resonance (CW-EPR) spectroscopy and imaging

We used this LabVIEW code for the study published in journal X (to be announced).
DOI: to be announced

This code was developed in the following environment:

Intel Core i7, 3.2 GHz, memory 16 GB; 
Windows 10 Pro;
National Instruments (NI) LabVIEW Professional Development 2020;
NI PXIe-6386 (PXI Multifunction I/O module)

This code works with NI’s data acquisition board. We used PXIe-6386 (8 analog inputs, sampling rate 14M sampling/s per channel, and 16 bits). The initial setting of the data acquisition uses analog input port ai0 of PXIe-6386 for the output voltage signal of the operational amplifier in the EPR receiver system.

The following signal connections are default settings in our code.

Sampling clock PXI Slot 3/PFI12;
Trigger PXI Slot 3/PFI0;
Input signal PXI Slot 3/ai0

In our case, we installed the PXIe-6386 board in Slot 3 of the PXI chassis. The user should modify the signal connections and the slot setting to meet the user’s environment.

The data acquisition and signal processing code consists of three vi programs.

(1) main vi program: EPR_acquisition_imaging_Eng.vi;
(2) Filter sub vi: Filter2.vi;
(3) MHD spectral lineshape reconstruction sub vi: MHD_reconstruction_Eng.vi

This code was written by Ririko Nakaoka, Ph.D., at Magnetic Resonance Engineering Laboratory, Hokkaido University, Sapporo, Japan.
