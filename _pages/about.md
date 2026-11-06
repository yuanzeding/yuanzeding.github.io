---
permalink: /
excerpt: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

{% include base_path %}

<div class="hero">
  <p class="hero__kicker">Ph.D. candidate &middot; Caltech Physics</p>
  <h2 class="hero__title">Black holes, their host galaxies, and the gas around them</h2>
  <p>I am a fifth-year Ph.D. candidate in Physics at Caltech, co-advised by <b>Prof. Charles Steidel</b> and <b>Prof. Fiona Harrison</b>. I use X-ray, optical and near-infrared spectroscopy to study how accreting supermassive black holes shape their environments, from the inner accretion disk out to the circumgalactic medium (CGM).</p>
  <div class="tag-row">
    <span class="tag">AGN &amp; CGM at z ~ 2&ndash;3</span>
    <span class="tag">Keck / KCWI &amp; MOSFIRE</span>
    <span class="tag">Galaxy mergers</span>
    <span class="tag">X-ray reflection</span>
    <span class="tag">AGN outflows</span>
  </div>
</div>

My current work centers on the **CGM of AGN at cosmic noon**. I use deep Keck/KCWI integral-field and Keck/MOSFIRE spectroscopy from the Keck Baryonic Structure Survey (KBSS) to map extended Ly&alpha; nebulae around 55 AGN, from hyperluminous QSOs to optically faint broad-line AGN and type-2 AGN. The goal is to see how much of the gas around a galaxy is set by its black hole and how much by the galaxy itself.

<!-- My latest work demonstrates that at redshift 2–4, the CGM is more closely correlated with the host galaxies' stellar mass rather than direct supermassive black hole (SMBH) activity, leading to new investigations into whether black hole feedback is more effective at higher redshifts. -->

I have also put substantial work into **KCWI data reduction**, building on the foundations laid by the original developers. My additions to the [KCWI DRP](https://github.com/Keck-DataReductionPipelines/KCWI_DRP), [KcwiKit](https://github.com/yuguangchen1/KcwiKit) and [KSkyWizard](https://github.com/zhuyunz/KSkyWizard) include better cosmic-ray rejection, wavelength corrections, automated sky and source masks, joint frame-to-frame and blue/red alignment to ~0.01&ndash;0.02&Prime; without a point source, and post-DRP sky matching. I have also adapted the [GIST](https://arxiv.org/abs/1906.04746) pipeline to fit combined blue+red KCWI cubes ([details and reduction guide]({{ base_path }}/code_data/)). I am also involved in developing GalfitS, a code that fits multi-band images and SEDs together.

## Current work

<a class="feature card" href="{{ base_path }}/research/#cgm">
  <div class="feature__img"><img src="{{ base_path }}/images/research/cgm_hlqso_nebulae.jpg" alt="Lyman-alpha nebulae around hyperluminous QSOs" loading="lazy"></div>
  <div class="card__body">
    <div class="card__label"><span class="status prelim">Preliminary</span> &nbsp;About to be submitted</div>
    <div class="card__title">The nature of the extended Ly&alpha; nebulae around AGN at z ~ 2&ndash;3</div>
    <p class="card__text">KCWI finds extended Ly&alpha; around nearly every AGN in the sample, yet nebular luminosity rises only ~15&times; while AGN ionizing output rises 1000&times;. In faint AGN, Ly&alpha; is broader and redder than the Balmer lines, pointing to resonant scattering by dense neutral clumps. Type-2 AGN have brighter, more compact nebulae, which favors a gas-rich evolutionary phase over orientation alone. <i>These results are preliminary.</i></p>
  </div>
</a>

## Research highlights

<div class="card-grid card-grid--2">
  <a class="card card__link" href="{{ base_path }}/research/#mergers">
    <div class="card__img dark" style="background-image:url('{{ base_path }}/images/research/ugc2369s_hst.jpg')"></div>
    <div class="card__body">
      <div class="card__label">Galaxy mergers &middot; 2026</div>
      <div class="card__title">A kpc-scale triple merger in UGC 2369S</div>
      <p class="card__text">Multiwavelength study of three nuclei about 3 kpc apart, one of which may host a heavily obscured AGN.</p>
    </div>
  </a>
  <a class="card card__link" href="{{ base_path }}/research/#reflection">
    <div class="card__img" style="background-image:url('{{ base_path }}/images/research/xillver_highdensity.jpg')"></div>
    <div class="card__body">
      <div class="card__label">Accretion physics &middot; 2024</div>
      <div class="card__title">High-density X-ray reflection models</div>
      <p class="card__text">Plasma effects in XSTAR/XILLVER strengthen Fe K and O resonance features from dense disks.</p>
    </div>
  </a>
  <a class="card card__link" href="{{ base_path }}/research/#outflows">
    <div class="card__img" style="background-image:url('{{ base_path }}/images/research/izw1_outflows.jpg')"></div>
    <div class="card__body">
      <div class="card__label">AGN feedback &middot; 2022</div>
      <div class="card__title">Super-Eddington winds in I Zw 1</div>
      <p class="card__text">Variable ultrafast outflows launched during an X-ray flare follow &xi; &prop; v<sup>3.24</sup>.</p>
    </div>
  </a>
  <a class="card card__link" href="{{ base_path }}/research/#smbhb">
    <div class="card__img" style="background-image:url('{{ base_path }}/images/research/pks2131_sinusoid.jpg')"></div>
    <div class="card__body">
      <div class="card__label">Black hole binaries &middot; 2025</div>
      <div class="card__title">Sinusoidal blazars as SMBH binaries</div>
      <p class="card__text">Coherent radio-to-optical periodicity in PKS 2131&minus;021 points to a supermassive black hole binary.</p>
    </div>
  </a>
</div>

## News

<ul class="news">
  <li><span class="news__date">Nov 2026</span> Paper I on the extended Ly&alpha; nebulae around 55 KBSS AGN (Keck/KCWI + MOSFIRE) is nearly ready for submission. <a href="{{ base_path }}/research/#cgm">Preliminary results &rarr;</a></li>
  <li><span class="news__date">May 2026</span> <a href="https://doi.org/10.3847/1538-4357/ae5643">UGC 2369S triple-merger paper</a> published in ApJ.</li>
  <li><span class="news__date">Jul 2025</span> Two co-authored papers out: <a href="https://doi.org/10.3847/1538-4357/addec8">BLR vs. accretion-disk inclination</a> and the <a href="https://doi.org/10.3847/1538-4357/addc60">sinusoidal blazar PKS J0805&minus;0111</a>.</li>
  <li><span class="news__date">May 2025</span> <a href="https://doi.org/10.3847/1538-4357/adc567">PKS 2131&minus;021</a>: coherent sinusoidal variations from radio to optical, strong evidence for a blazar SMBH binary.</li>
  <li><span class="news__date">Oct 2024</span> <a href="https://doi.org/10.3847/1538-4357/ad76a1">High-density XILLVER reflection model</a> published in ApJ.</li>
</ul>

<p><a class="btn-pill" href="{{ base_path }}/publications/">All publications</a> <a class="btn-pill alt" href="{{ base_path }}/research/">Research details</a> <a class="btn-pill" href="{{ base_path }}/files/cv-yzding.pdf">CV (PDF)</a></p>

## Contact

<i class="fas fa-envelope"></i> [yding@caltech.edu](mailto:yding@caltech.edu) &nbsp;&middot;&nbsp; Cahill Center for Astronomy &amp; Astrophysics, Caltech, Pasadena, CA
