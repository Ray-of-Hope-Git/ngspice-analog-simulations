NGspice Analog Simulations
Some analog circuit sims I've been working on in NGspice. Mostly focused on basic building blocks — filters, amplifiers, diff pairs.

What's in here
RC Low-Pass Filter
01_rc_lowpass_filter/rc_lowpass.cir
Simple 1st-order RC filter (R=1k, C=100nF), cutoff around 1.59kHz. Runs an AC sweep for the Bode plot and a transient sim to see the filtering in action.


NMOS Common-Source Amp
02_nmos_common_source/nmos_cs_amp.cir
CS amplifier with voltage divider bias and source bypass cap. Pulls the DC operating point, does AC gain analysis, and shows a 10kHz signal getting amplified in transient.


CMOS Diff Pair
03_cmos_diff_pair/cmos_diff_pair.cir
NMOS diff pair with PMOS current mirror load, 100uA tail current. Has the DC transfer curve sweep and AC gain. This one's the most interesting — you can clearly see the linear region in the DC sweep.


How to run
Drop the .cir file in your NGspice bin folder and:
source rc_lowpass.cir
Plots pop up automatically — the .control blocks handle the analysis and plotting.
