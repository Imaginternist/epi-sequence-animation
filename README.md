# EPI Sequence Animation

An interactive browser animation connecting a simplified single-shot
gradient-echo EPI waveform to its serpentine Cartesian k-space trajectory.

The animation follows one excitation through:

1. RF excitation at the k-space origin;
2. combined readout and phase-encoding prephasing to the lower-left corner;
3. alternating positive and negative `Gx` readout lobes;
4. ADC sampling during each readout; and
5. short positive `Gy` blips that advance to the next `ky` line.

The central k-space crossing is labeled as TE. Nine readout lines are shown so
that the sequence remains legible in a compact teaching animation.

## View

The public animation is hosted with GitHub Pages:

<https://imaginternist.github.io/epi-sequence-animation/>

## Controls

- **Play / Pause** runs or pauses the complete echo train.
- **Next event** advances one waveform event at a time.
- **Reset** returns to RF excitation.
- **Speed** changes playback speed without changing the trajectory.

## Educational boundary

This is a simplified single-shot GE-EPI readout model, not a complete MRI
scanner or pulse-sequence simulation. It does not model slice selection,
relaxation or T2* signal decay, ramp sampling, gradient slew limits, gradient
delay, eddy currents, Nyquist ghosting, off-resonance, susceptibility distortion,
parallel imaging, partial Fourier, or reconstruction.

The model is designed to show how alternating readout-gradient polarity creates
the EPI zig-zag trajectory and how phase-encoding blips move between neighboring
`ky` lines. It contains no patient data and requires no server-side processing.
