
# EXP 4 A: Design-of-FIR-Digital-Filter-using-Rectangular-Window

# AIM 1:  To perform Design-of-LOWPASS FIR-Digital-Filter-using-Rectangular-Window using SCILAB.

# APPARATUS REQUIRED: 
PC installed with SCILAB. 

# PROGRAM: 
```
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
# CALCULATION:

<img width="1200" height="1600" alt="image" src="https://github.com/user-attachments/assets/f37e463f-9796-47d5-8c9f-716ab87511f1" />

# OUTPUT: 

<img width="533" height="492" alt="image" src="https://github.com/user-attachments/assets/1f2255ef-4ac9-48ab-9092-35bcbb3ba188" />

<img width="762" height="717" alt="image" src="https://github.com/user-attachments/assets/4fd0ffd1-c5e3-4fe4-ac8e-63513c212624" />

# RESULT: 

Thus design of low pass FIR digital filter using-Rectangular-Window waveforms were plotted and output was verified.

# AIM 2: To perform DESIGN OF HIGH PASS FIR DIGITAL FILTERS using SCILAB.

# APPARATUS REQUIRED: 
PC installed with SCILAB. 

# PROGRAM: 
```
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
# CALCULATION:

<img width="1200" height="1600" alt="image" src="https://github.com/user-attachments/assets/25c72ffd-d040-40aa-8a88-8c76498a7749" />


# OUTPUT: 

<img width="762" height="721" alt="image" src="https://github.com/user-attachments/assets/75dce006-74ba-4147-be74-17f3a752dbd0" />

<img width="514" height="474" alt="image" src="https://github.com/user-attachments/assets/41482ad5-e876-4c9c-bf47-ae86fa265211" />

# RESULT: 
Thus design of HIGH pass FIR digital filter using-Rectangular-Window waveforms were plotted and output was verified.

# AIM 3: To perform DESIGN OF BAND PASS FIR DIGITAL FILTERS using SCILAB.

# APPARATUS REQUIRED: 
PC installed with SCILAB. 

# PROGRAM: 
```
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
# CALCULATION:

<img width="1200" height="1600" alt="image" src="https://github.com/user-attachments/assets/a160f105-9185-462a-80d3-e03318fb252f" />

# OUTPUT: 

<img width="760" height="720" alt="image" src="https://github.com/user-attachments/assets/baba688a-df76-4693-b5db-08f9c6048ffe" />
<img width="549" height="455" alt="image" src="https://github.com/user-attachments/assets/e559bd3f-0e4f-4450-b0a3-9e12b5eca0fd" />


# RESULT: 
Thus design of BAND pass FIR digital filter using-Rectangular-Window waveforms were plotted and output was verified.

# AIM 4: To perform DESIGN OF BAND STOP FIR DIGITAL FILTER using SCILAB.

# APPARATUS REQUIRED: 
PC installed with SCILAB. 

# PROGRAM: 
```
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
# CALCULATION:

<img width="1200" height="1600" alt="image" src="https://github.com/user-attachments/assets/5eec2741-0afb-4726-a86c-1e0268ea2397" />


# OUTPUT: 
<img width="756" height="718" alt="image" src="https://github.com/user-attachments/assets/7947da26-cc61-4320-9059-0fd940c6108d" />
<img width="558" height="511" alt="image" src="https://github.com/user-attachments/assets/98225cf5-19bd-42f0-99dc-1cad975a8e71" />

# RESULT: 
Thus design of BAND STOP FIR digital filter using-Rectangular-Window waveforms were plotted and output was verified.
