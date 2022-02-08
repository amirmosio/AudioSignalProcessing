# AudioSignalProcessing

## Problem 2:
In this problem, we will take a practical approach toward the subject of Fourier transform. What we have 
discussed so far is the Fourier transform of continuous-time signals, which is only available in analog devices, 
and when it comes to computers, there is no way to truly define continuous-time signals as everything in 
computers is digitized (considering you are not using symbolic programming, which is another thing and its 
computational power is limited). In light of this, python and other libraries in other languages implement 
something called the Discrete Fourier Transform (DFT). Consider a vector x[n] with length N, then its DFT is 
another vector, X[K] with the same length N and is defined as:


$𝑋[𝑘] = \sum_{n=0}^{N-1} 𝑥[𝑛]𝑒^{-𝑗(\frac{2𝜋}{𝑁})𝑘n}$


Now, answer/implement the following questions:
1. With respect to the given equation for DFT, find the equation for IDFT (Inverse DFT).
2. Implement a function called fft that takes a vector as input and produces its DFT vector as output.
3. Implement the function for IDFT called ifft.
4. Consider the signal $x(t) = cos (\pi t)$. Construct the vector $x[n] = x(nT)$ with length N. Plot this 
vector for $T = \frac{1}{2}$
and N = 1000 for n ranging from -500 to 500.
• Obviously, when trying to reference the vector’s elements, x[n], one should use a valid index 
ranging from 0 to N - 1 (for python).
5. Compute Fourier transform of x(t). 
6. Use fft to compute DFT of x[n], X[k]. Plot X[k]. Compare the result with 5.
7. Use ifft on X[k]. Is the resulting vector equal to x[n]?
8. Show the effects of changing N and T on the DFT of x[n], in different plots.


## Problem 3:
In this question, we want to cancel unwanted effect of a system on a sound. This action 
is called channel equalization. For such purpose, we have clean1.wav and distorted1.wav as input 
and output signals of this system. Clean1 is a signal without any distortion and distorted1 is the 
output of the system which has been distorted by the system. distortd2.wav is another signal that 
has been the output of this system. The problem is that we do not have access to the clean2 signal. 
Using clean1.wav and distorted1.wav signals, first calculate the frequency response of the system. 
Then try to recover clean2 signal using system’s inverse response. Discuss your methodology and 
attach the recovered signal named recovered2.wav

## Problem 4:
In this question we want to recover a noisy signal by applying a suitable filter (signal de-noising). 
Consider the noisy1.wav signal which is made from a clear sound added with some noise. You 
should design an appropriate filter and apply it to the noisy signal. In order to find the frequency 
of the noise and attenuate it in the filter, you should first examine the signal’s spectrum and detect 
the speech gaps. In these gaps you can find the noise frequency. Then, design a filter which 
attenuates these frequencies. Explain your methodology and attach the final de-noised signal named 
denoise1.wav to your report.
