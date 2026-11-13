# Universal Basic Inc

**Dylan Holdren**, founder and sole engineer. I make scientific and AI software run correctly on hardware beyond the usual NVIDIA path, and I run a private, solar first AI that is available on the Android and Microsoft apps store, called NoFootprint. After losing my father to lung cancer in 2019, my focus has been medical simulation software, molecular dynamics and open source projects that empower labs of any size to help find the next best treatments for disease.

## Protein structure prediction on Intel GPUs: Boltz-2

<p>
  <a href="https://github.com/UniversalBasicInc/boltz2-intel-arc"><img src="https://raw.githubusercontent.com/UniversalBasicInc/boltz2-intel-arc/main/img/egfr_osimertinib.png" width="48%" alt="EGFR kinase with osimertinib, predicted by Boltz-2 on an Intel Arc Pro B70"></a>
  <a href="https://github.com/UniversalBasicInc/boltz2-intel-arc"><img src="https://raw.githubusercontent.com/UniversalBasicInc/boltz2-intel-arc/main/img/kras_g12c_sotorasib.png" width="48%" alt="KRAS G12C with sotorasib, predicted by Boltz-2 on an Intel Arc Pro B70"></a>
</p>

I added Intel GPU support to Boltz-2, validated it on three GPUs, and got it merged upstream: [boltz-community #20](https://github.com/Novel-Therapeutics/boltz-community/pull/20), shipped in release 2.13.0. The experiments behind it, including the two lung-cancer drug targets above, are in **[boltz2-intel-arc](https://github.com/UniversalBasicInc/boltz2-intel-arc)**.

## Machine-learned force fields in molecular dynamics: MACE and GROMACS

<a href="https://github.com/UniversalBasicInc/mace-arc"><img src="https://raw.githubusercontent.com/UniversalBasicInc/mace-arc/master/docs/img/water64_300K.gif" width="60%" alt="64 water molecules simulated with MACE-MP-0 on an Intel Arc Pro B70"></a>

**[mace-arc](https://github.com/UniversalBasicInc/mace-arc)** runs the MACE interatomic potential on Intel Arc GPUs, validated against CPU and NVIDIA results. To use it inside real simulations I got three changes merged into GROMACS:

- [!6372](https://gitlab.com/gromacs/gromacs/-/merge_requests/6372): run neural-network potentials on Intel GPUs
- [!6370](https://gitlab.com/gromacs/gromacs/-/merge_requests/6370): a pair-list fix for those potentials
- [!6417](https://gitlab.com/gromacs/gromacs/-/merge_requests/6417): build the LibTorch sources with the C++ standard they need

GROMACS is developed on GitLab, so these do not appear in the contribution graph here.

## NoFootprint

**[NoFootprint](https://nofootprint.chat)** is a private, solar first AI chat subscription, live on the web, Google Play and the Microsoft Store. It runs on my own solar-first hardware, with grid use matched by renewable energy certificates. I wrote the app, the back end and the inference stack, and I operate it.

## MYTH.OS

An operating system for everyone, as an alternative to Windows 11 and macOS, with NoFootprint built in. In development; not yet released. Based on Debian 13, and built with tech savvy folks and your grandma in Nebraska both in mind such that anyone can have a private, secure operating system with all the modern features, a crisp and responsive UI, and excellent compatibility features for older and newer hardware as well, no TPM modules required and no expensive hardware upgrades for businesses. 

## Also

- **[xeon-phi-knc-codegen-revival](https://github.com/UniversalBasicInc/xeon-phi-knc-codegen-revival)**: a 2013 Xeon Phi brought back to run validated disease-model simulations, with a compiler-backend patch and measurements.
- **[mythd](https://github.com/UniversalBasicInc/mythd)**: a Rust security perimeter around local LLM inference, with post-quantum key exchange and a signed audit log.
- **SUSE AI charts** [#40](https://github.com/SUSE/suse-ai-charts/pull/40) (merged): OIDC settings never reached Dex and oauth2-proxy.
- **BOINC** [#7376](https://github.com/BOINC/boinc/pull/7376) (merged): client packages broken on openSUSE Leap 16.

## How I work

I validate before I claim: bit-exact where that is possible, a stated tolerance where it is not, and the limits written down. I use AI coding agents every day, review every change, and disclose that in contributions where projects ask for it. I love finding bugs, and hunting down a problem until it is fixed. I believe in the age of AI and new tools, there is no excuse for bad software; I make good software that is verified on multiple architectures and environments. I have RISC-V, Intel and AMD EPYC machines, Nvidia workstation and Intel Arc Pro GPUs and I am always happy to partner with labs who want to collaborate using my hardware and software expertise. 
