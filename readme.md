# [Phase Unwrapping] Phase Unwrapping in Optical Metrology through Denoising and Convolutional Separation Networks [with code attached]

Introduction: Phase measurement is of great importance in many applications such as optical metrology, medical diagnosis, and 3D imaging. However, the measured phases are typically enveloped within the range (−π, +π] through trigonometric calculations, which does not reflect the true phase values. To address this issue, numerous phase unwrapping methods have been proposed [1-11]. In the branch cutting algorithm by Goldstein [1], a discontinuity was first discovered at the residue, and it was identified based on the closed path integral that is non-zero at the residue. The quality guidance algorithm [2-4] relies on a quality map to guide the integration path, rather than identifying the residue. Method [5,6] is designed to minimize the discontinuities in the unwrapped surface. For method [7,8], the phase unwrapping problem is formulated in the generalized minimum norm sense to minimize the difference between the local derivatives of the true phase and the measured phase. A solution decomposition algorithm based on the intensity transmission equation (TIE) was proposed [9-11] to obtain an absolute phase map directly from the intensity information. The TIE decomposition method is easy to implement and independent of the path.
In recent years, deep learning has been successfully applied in fields such as image classification and restoration, with many models based on deep convolutional neural networks (CNN) achieving satisfactory results. This advanced technology has also been adopted in the field of optical metrology. A multilayer perceptron neural network [12] was proposed to identify phase discontinuities. In [13], a residual neural network was employed to solve the phase expansion problem, and the network was trained on simulated phases with steep spatial gradients. However, the expanded phase shown in [13] was incorrect for some areas. In 2018, we submitted a provisional patent application on using convolutional segmentation networks and denoising networks for phase expansion [14]. The similar method using convolutional segmentation networks was only demonstrated in 2019 using simulated data [15]. However, our work differs from [15] in that: (1) smaller filter sizes, dynamic filter numbers, and deeper layers make the network wider and nonlinearly amplify our network. (2) Since the denoising network is integrated into our phase expansion network by reconstructing expanded phases through adding integer multiples of 2π to the wrapped phase, this approach is used.
This paper proposes a new CNN-based phase expansion method that transforms the phase expansion problem into a multiclass classification problem. First, a denoising network is utilized to denoise the noisy wrapped phase. Then, it is fed into a segmentation network to generate integer multiples, and post-processing is used to correct the integer multiples. Finally, the denoised envelope phase is combined with the corrected integral multiples to obtain the dewrapped phase. Simulation data and experimental tests on actual interferometric systems have proven the effectiveness of this method.
Figure 1. Network structure for phase expansion.
See Figure 2. Simulation results of phase expansion on clean data. (a) Wrapped phase (input), (b) Output (integer multiple n), (c) Ground truth (integer multiple n), (d) Reconstructed expanded phase, (e) Ground truth (expanded phase), (f) Difference
Figure 3. Post-processing phase unwrapping results. From top to bottom: wrapped phases ((a1), (a2)), ground truth (unwrapped phases, (b1), (b2)), reconstructed unwrapped phases ((c1), (c2)), post-processed unwrapped phases ((d1), (d2)), and difference ((e) = (c) - (B), (f) = (d) - (B)).

Figure 4. Phase discontinuity extraction ((a), (c)) and connected region labeling ((b), (d)).

Figure 5. Network structure for noise-wrapped phase denoising.

Figure 6. Simulated noisy data unwrapping results (SNR = 4.0 dB). (a) Noisy wrapped phase, (B) denoised wrapped phase, (c) real ground (wrapped phase), (d) unwrapped phase, (e) real ground (unwrapped phase), (f) difference

Figure 7. Unwrapping results on more severely damaged data (SNR = 0.6 dB). (a) Noisy wrapped phase, (B) denoised wrapped phase, (c) real ground (wrapped phase), (d) unwrapped phase, (e) real ground (unwrapped phase), (f) difference

Figure 8. Results from other methods of unwrapping. The unwrapped phases (a) and (e) are produced by the branch cutting algorithm of Goldstein, the unwrapped phases (c) and (g) are obtained by a quality-guided path tracking method, and the differences (B), (D), (F), and (H) are shown.

Figure 10. Real data unwrapping results. From left to right in sequence: wrapped phases (input, (a), (e)), reconstructed unwrapped phases (reconstructed by our network ((B), (F)) and MG ((c), (g)), and differences ((d), (h)).
In conclusion, this paper proposes a phase decomposition method based on CNN. This method can effectively improve the precision of phase decomposition. The proposed method has good application prospects. We transform the phase decomposition problem into a multi-class classification problem and introduce an effective segmentation network for classification. In addition, this network can also be used to identify locations with phase discontinuities and employ post-processing operations to enhance performance. Furthermore, we integrated a noise denoising network that preprocesses noise-wrapped phases. Since our network is fully convolutional, it is also applicable to other image sizes (different from the training image size). Simulation and experimental data validate the effectiveness of this method. Our current network is trained using continuous wrapped phase images and works well, which is typical in interferometric optics metrology. We are currently studying more complex cases with discontinuously wrapped phases and will report new methods soon.
Code List

## Images

![(Phase Unwrapping)Phase unwrapping in optical metrology through denoising and convolutional segmentation networks [with code]](01.jpg)
![(Phase Unwrapping)Phase unwrapping in optical metrology through denoising and convolutional segmentation networks [with code]](02.jpg)
![(Phase Unwrapping)Phase unwrapping in optical metrology through denoising and convolutional segmentation networks [with code]](03.jpg)
![(Phase Unwrapping)Phase unwrapping in optical metrology through denoising and convolutional segmentation networks [with code]](04.jpg)
![(Phase Unwrapping)Phase unwrapping in optical metrology through denoising and convolutional segmentation networks [with code]](05.jpg)
![(Phase Unwrapping)Phase unwrapping in optical metrology through denoising and convolutional segmentation networks [with code]](06.jpg)
![(Phase Unwrapping)Phase unwrapping in optical metrology through denoising and convolutional segmentation networks [with code]](07.jpg)
![(Phase Unwrapping)Phase unwrapping in optical metrology through denoising and convolutional segmentation networks [with code]](08.jpg)
![(Phase Unwrapping)Phase unwrapping in optical metrology through denoising and convolutional segmentation networks [with code]](09.jpg)
![(Phase Unwrapping)Phase unwrapping in optical metrology through denoising and convolutional segmentation networks [with code]](10.jpg)
![(Phase Unwrapping)Phase unwrapping in optical metrology through denoising and convolutional segmentation networks [with code]](11.jpg)

<!-- PAYMENT_BLOCK -->

## Get this dataset

- Payment link (Stripe): [Buy now](https://buy.stripe.com/3cs8yP7sY87d0vu9AB)
- Payment QR code: ![Payment QR code](pay.png)

<!-- /PAYMENT_BLOCK -->
