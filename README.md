# Prior-Mixer-KiMoCoNet
Magnetic Resonance Imaging (MRI) is a vital non-invasive imaging modality that is highly
sensitive to patient motion, which disrupts k-space consistency and produces structured artifacts
in reconstructed images. Most existing deep learning–based motion correction methods operate
exclusively in the image domain, implicitly discarding phase information and limiting their ability
to correct motion-induced frequency distortions. Although several recent approaches incorporate
k-space awareness, they primarily utilize k-space to detect corrupted lines or impose data-
consistency constraints. Motion correction itself remains confined to the image domain. As a
result, phase-inconsistent frequency components introduced during acquisition are not explicitly
corrected. To address this limitation, we propose Prior-Mixer KiMoCo-Net, an end-to-end
framework for MRI motion artifact correction that integrates k-space and image-domain
processing. The proposed method first detects motion-corrupted k-space lines and constructs a
prior-based mixing representation by selectively incorporating uncorrupted information from
adjacent slices. Corrupted regions in the current slice are replaced using this reliability-aware prior,
followed by a k-space correction network that restores frequency-domain consistency. Finally, an
image-domain refinement network suppresses residual artifacts and enhances structural fidelity.
The model is trained using a hybrid objective that jointly enforces k-space fidelity and image-
domain structural similarity. Experiments on simulated and real motion-corrupted brain MRI
datasets demonstrate that the proposed method achieves stable performance compared to state-of-
the-art approaches, improving SSIM from 0.765 to 0.962 and PSNR from 25 dB to 35 dB. Notably,
the method exhibits improved robustness under severe motion and reduced reconstruction
variance. These results highlight the importance of explicitly modeling k-space corruption and
selectively utilizing reliable prior information for accurate and stable MRI reconstruction. ![alt text](http://url/to/img.png)
