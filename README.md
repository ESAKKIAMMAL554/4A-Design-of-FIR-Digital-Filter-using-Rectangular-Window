# FIR-FILTER-DESIGN
# EXP 4 A: Design-of-FIR-Digital-Filter-using-Rectangular-Window

# AIM 1:  To perform Design-of-LOWPASS FIR-Digital-Filter-using-Rectangular-Window using SCILAB.

# APPARATUS REQUIRED: 
PC installed with SCILAB. 

# PROGRAM: 
```asm
clc ; 
close ; 
M=input('Enter the Odd Filter Length ='); 
Wc=input('Enter the Digital Cut off frequency ='); 
alpha= (M -1)/2 // Center Value 
for n = 1:M 
if (n ==alpha+1) 
hd(n) = Wc/ %pi ; 
else 
hd(n) = sin(Wc *((n -1)-alpha)) /(((n -1)-alpha)*%pi); 
end 
end 
// Rectangular Window 
for n = 1:M 
W(n) = 1; 
end 
//Windowing filter coefficients 
h = hd.*W; 
disp(h,'Filter Coefficients are') 
[hzm,fr]= frmag (h,256) ; 
subplot(2 ,1 ,1) 
plot(2*fr, hzm) 
xlabel( ' Normalized Digital Frequency w'); 
ylabel( 'Magnitude '); 
title( ' Frequency Response of  FIR LPF using Rectangular Window ') 
hzm_dB = 20* log10 (hzm); 
subplot (2 ,1 ,2); 
plot(2*fr , hzm_dB); 
xlabel( ' Normalized Digital Frequency W' ); 
ylabel( 'Magnitude in dB'); 
title('Frequency Response of FIR LPF using Rectangular Window'); 
```

# OUTPUT: 
<img width="899" height="1599" alt="image" src="https://github.com/user-attachments/assets/f25f46df-1c52-48e3-892d-cc3995b16842" />
<img width="899" height="1599" alt="image" src="https://github.com/user-attachments/assets/d7be672d-561e-4cff-98fe-203c5e095587" />

<img width="533" height="492" alt="image" src="https://github.com/user-attachments/assets/43ea4204-e345-4443-ad25-42064b200049" />
<img width="762" height="717" alt="image" src="https://github.com/user-attachments/assets/4fd0ffd1-c5e3-4fe4-ac8e-63513c212624" />


# RESULT: 

Thus design of low pass FIR digital filter using-Rectangular-Window waveforms were plotted and output was verified.

# AIM 2: To perform DESIGN OF HIGH PASS FIR DIGITAL FILTERS using SCILAB.

# APPARATUS REQUIRED: 
PC installed with SCILAB. 

# PROGRAM: 
```asm
clc ; 
close ; 
M=input('Enter the Odd Filter Length ='); 
Wc=input('Enter the Digital Cut off frequency ='); 
alpha= (M -1)/2 // Center Value 
for n = 1:M 
if (n ==alpha+1) 
hd(n)=1-Wc/ %pi ; 
else 
hd(n) =-sin(Wc *((n -1)-alpha)) /(((n -1)-alpha)*%pi); 
end 
end 
// Rectangular Window 
for n = 1:M 
W(n) =1; 
end 
//Windowing filter coefficients 
h = hd.*W; 
disp(h,'Filter Coefficients are') 
[hzm,fr]= frmag (h,256) ; 
subplot(2 ,1 ,1) 
plot(2*fr, hzm) 
xlabel( ' Normalized Digital Frequency w'); 
ylabel( 'Magnitude '); 
title( ' Frequency Response of  FIR LPF using Rectangular Window ') 
hzm_dB = 20* log10 (hzm); 
subplot (2 ,1 ,2); 
plot(2*fr , hzm_dB); 
xlabel( ' Normalized Digital Frequency W' ); 
ylabel( 'Magnitude in dB'); 
title('Frequency Response of FIR HPF using Rectangular Window'); 
```

# OUTPUT: 
<img width="899" height="1599" alt="image" src="https://github.com/user-attachments/assets/08ed8dd9-aeba-4ca9-9091-0a58aea6bf99" />

<img width="514" height="474" alt="image" src="https://github.com/user-attachments/assets/8cc8e05e-696e-4ca4-b714-2fe987c53896" />
<img width="514" height="474" alt="image" src="https://github.com/user-attachments/assets/2720fa38-ed7f-404c-b59d-94ab001442a4" />


# RESULT: 
Thus design of HIGH pass FIR digital filter using-Rectangular-Window waveforms were plotted and output was verified.

# AIM 3: To perform DESIGN OF BAND PASS FIR DIGITAL FILTERS using SCILAB.

# APPARATUS REQUIRED: 
PC installed with SCILAB. 

# PROGRAM: 
```asm
clc ; 
close ; 
M=input('Enter the Odd Filter Length ='); 
Wc=input('Enter the Digital Cut off frequency ='); 
Wc2=Wc(2); 
Wc1=Wc(1); 
alpha= (M -1)/2 // Center Value 
for n = 1:M 
if (n ==alpha+1) 
hd(n) =(Wc2-Wc1)/%pi ; 
else 
hd(n) =((sin(Wc2 *((n -1)-alpha)))-(sin(Wc1 *((n -1)-alpha))))/(((n -1)-alpha)*%pi); 
end 
end 
// Rectangular Window 
for n = 1:M 
W(n) =1;  
end 
//Windowing filter coefficients 
h = hd.*W; 
disp(h,'Filter Coefficients are') 
[hzm,fr]= frmag (h,256) ; 
subplot(2 ,1 ,1) 
plot(2*fr, hzm) 
xlabel( ' Normalized Digital Frequency w'); 
ylabel( 'Magnitude '); 
title( ' Frequency Response of FIR BPF using Rectangular Window ') 
hzm_dB = 20* log10 (hzm); 
subplot (2 ,1 ,2); 
plot(2*fr , hzm_dB); 
xlabel( ' Normalized Digital Frequency W' ); 
ylabel( 'Magnitude in dB'); 
title('Frequency Response of FIR BPF using Rectangular Window'); 
```
# OUTPUT: 
<img width="899" height="1599" alt="image" src="https://github.com/user-attachments/assets/a4d212ec-c99f-4099-bd1f-ef2cac1671da" />
<img width="899" height="1599" alt="image" src="https://github.com/user-attachments/assets/95b2f0b5-4bc5-4f4d-81cc-dd02a2ff4103" />

<img width="760" height="720" alt="image" src="https://github.com/user-attachments/assets/962561d3-3e82-4ec4-9e6f-370b679808b6" />
<img width="549" height="455" alt="image" src="https://github.com/user-attachments/assets/7f1b80cf-1c15-4a00-bbd8-4ad9d857ae3c" />


# RESULT: 
Thus design of BAND pass FIR digital filter using-Rectangular-Window waveforms were plotted and output was verified.

# AIM 4: To perform DESIGN OF BAND STOP FIR DIGITAL FILTER using SCILAB.

# APPARATUS REQUIRED: 
PC installed with SCILAB. 

# PROGRAM: 
```asm
clc ; 
close ; 
M=input('Enter the Odd Filter Length ='); 
Wc=input('Enter the Digital Cut off frequency ='); 
Wc2=Wc(2); 
Wc1=Wc(1); 
alpha= (M -1)/2 // Center Value 
for n = 1:M 
if (n ==alpha+1) 
hd(n) =1-((Wc2-Wc1)/%pi) ; 
else 
hd(n) =((sin(Wc1 *((n -1)-alpha)))-(sin(Wc2 *((n -1)-alpha))))/(((n -1)-alpha)*%pi); 
end 
end 
// Rectangular Window 
for n = 1:M 
W(n) =1; 
end 
//Windowing filter coefficients 
h = hd.*W; 
disp(h,'Filter Coefficients are') 
[hzm,fr]= frmag (h,256) ; 
subplot(2 ,1 ,1) 
plot(2*fr, hzm) 
xlabel( ' Normalized Digital Frequency w'); 
ylabel( 'Magnitude '); 
title( ' Frequency Response of  FIR BSF using Rectangular Window ') 
hzm_dB = 20* log10 (hzm); 
subplot (2 ,1 ,2); 
plot(2*fr , hzm_dB); 
xlabel( ' Normalized Digital Frequency W' ); 
ylabel( 'Magnitude in dB'); 
title('Frequency Response of FIR BSF using Rectangular Window'); 
```

# OUTPUT: 
<img width="899" height="1599" alt="image" src="https://github.com/user-attachments/assets/1561bf8e-23c3-47cd-8b29-168388de6a0e" />
<img width="899" height="1599" alt="image" src="https://github.com/user-attachments/assets/a886094f-1839-4ece-86f9-85ba408d1497" />
<img width="756" height="718" alt="image" src="https://github.com/user-attachments/assets/ec1e8a9a-5556-4988-9b7a-508b1b1fa2ed" />
<img width="558" height="511" alt="image" src="https://github.com/user-attachments/assets/a70e8020-495b-4de5-8b92-ac79b5e077c8" />

# RESULT: 
Thus design of BAND STOP FIR digital filter using-Rectangular-Window waveforms were plotted and output was verified.
