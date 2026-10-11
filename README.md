# Chambadal–Novikov–Curzon–Ahlborn engine

An interactive web page on the "endoreversible" Carnot engine, which delivers finite power by exchanging heat with its reservoirs at a finite rate. It was prepared as supplementary material for the Statistical Physics 1 lecture on heat engines, going beyond the quasi-static Carnot engine. The page is available in English (`index.html`) and Korean (`ko.html`); each has a button that links to the other.

The engine's efficiency at maximum power,

```math
\eta_{\rm CA} = 1 - \sqrt{\frac{T_c}{T_h}},
```

is widely known as the Curzon–Ahlborn efficiency after their 1975 paper in the *American Journal of Physics*. The same result had already appeared in 1957 in work by P. Chambadal and I. I. Novikov on nuclear power stations, so this project uses the name Chambadal–Novikov–Curzon–Ahlborn.

## What's on the page

- **Interactive engine.** Drag the hot-side working temperature $`T_{hw}`$ and set the reservoir temperatures $`T_h`$ and $`T_c`$.
  - An energy-flow diagram and a temperature ladder update live as you drag.
  - Plots show power versus $`T_{hw}`$ and power versus efficiency.
  - A heat budget splits the incoming heat into work, lost work $`T_c\dot S`$, and reversible rejection $`(T_c/T_h)\,\dot Q_h`$.
  - Buttons jump to the maximum-power point and to the quasi-static and short-circuit limits.
- **Step-by-step derivation.** It covers the entropy balance, the power expression, the maximization, and the efficiency at maximum power, following the setup of Problem 4.6 in Schroeder's textbook. The numerical evaluation is for a coal-fired turbine (600 °C / 25 °C): $`\eta_{\rm CA} \approx 41.6\%`$ versus $`\eta_C \approx 65.9\%`$.
- **Entropy production and the two limits.** This section discusses the quasi-static and short-circuit limits and the Gouy–Stodola relation $`W = \eta_C Q_h - T_c\,\Delta S_{\rm tot}`$.
- **P–V diagram of the working cycle.** The Carnot cycle that the working substance actually runs between $`T_{hw}`$ and $`T_{cw}`$ is drawn live for a monatomic ideal gas. With the stroke time $`\Delta t`$ fixed, the enclosed area is proportional to the power, $`P = W/2\Delta t`$, so the loop is largest at maximum power and collapses in both limits.
- **Comparison with real power plants.** The values from Table I of Curzon and Ahlborn are recomputed.
- **Unequal conductances.** A widget shows that the efficiency at maximum power stays $`1 - \sqrt{T_c/T_h}`$ when the conductances differ. This holds whether the stroke times are free or forced to be equal; only the power changes.
- **Remarks on a quantum-dot heat engine.** These follow Lee, Um, and Park, *Phys. Rev. E* **98**, 052137 (2018). A live numerical plot of efficiency at maximum power shows the $`\tfrac{1}{2}`$-universality ($`\eta_{\rm op} \approx \eta_C/2`$) and its breakdown when the gate voltage is tuned at fixed bias.
- **Light/dark mode.** The page follows the system setting by default. A toggle button overrides it, and the choice is remembered in the browser.

## Usage

Each language version is a single self-contained file: `index.html` (English) and `ko.html` (Korean). Open either one in any modern browser, or serve them with GitHub Pages:

1. Go to **Settings → Pages** in this repository.
2. Under **Build and deployment**, choose **Deploy from a branch** and select the branch and the root folder.
3. The English page will be available at `https://lshlj82.github.io/Chambadal-Novikov-Curzon-Ahlborn-engine/`, and the Korean page at `.../ko.html`.

There is no build step. The page loads two things from the network:

- [MathJax 3.2.2](https://www.mathjax.org/) from cdnjs, for equation rendering;
- the Source Serif 4 and IBM Plex Sans fonts from Google Fonts, plus Noto Serif KR and IBM Plex Sans KR for the Korean page. Without a connection the page falls back to system fonts.

All plots and numerical optimizations are plain JavaScript and SVG, with no other libraries.

## Credits

The page, its derivations, and its interactive figures were created by **Claude Opus 5.5** (Anthropic). It was prompted with the lecture materials, the Curzon–Ahlborn paper, the course note on entropy in the endoreversible engine, and the quantum-dot paper listed below. The content should be read alongside those sources.

## 한국어 안내

통계물리 1 강의에서 다룬 카르노 엔진을 넘어, 유한한 시간 동안 일률을 내는 내부가역(endoreversible) 엔진을 다루는 인터랙티브 보충 자료입니다. 한국어 페이지는 `ko.html`입니다. 주요 내용은 다음과 같습니다.

- 작동 온도를 조절하는 데모
- 최대 일률에서의 효율 $`\eta_{\rm CA} = 1 - \sqrt{T_c/T_h}`$ 유도
- 실제 작동 순환의 P–V 도표
- 엔트로피 생성과 준정적·단락 두 극한
- 실제 발전소와의 비교
- 양자점 열기관 연구(Lee, Um, Park, PRE 2018)에 대한 덧붙임

이 페이지는 Claude Opus 5.5(Anthropic)가 제작했습니다.

## References

1. P. Chambadal, *Les centrales nucléaires* (Armand Colin, Paris, 1957), pp. 41–58.
2. I. I. Novikov, "Efficiency of atomic energy installation," *Atomnaya Energiya* **3**(11), 409–412 (1957).
3. I. I. Novikov, "The efficiency of atomic power stations (a review)," *Journal of Nuclear Energy* **7**(1–2), 125–128 (1958). [doi:10.1016/0891-3919(58)90244-4](https://doi.org/10.1016/0891-3919(58)90244-4)
4. D. V. Schroeder, *An Introduction to Thermal Physics* (Addison-Wesley, 2000), Problem 4.6.
5. F. L. Curzon and B. Ahlborn, "Efficiency of a Carnot engine at maximum power output," *American Journal of Physics* **43**, 22–24 (1975). The textbook footnote lists volume 41; the article appears in volume 43.
6. S. H. Lee, J. Um, and H. Park, "Nonuniversality of heat-engine efficiency at maximum power," *Physical Review E* **98**, 052137 (2018). [doi:10.1103/PhysRevE.98.052137](https://doi.org/10.1103/PhysRevE.98.052137)
7. C. Van den Broeck, "Thermodynamic efficiency at maximum power," *Physical Review Letters* **95**, 190602 (2005).
8. M. Josefsson *et al.*, "A quantum-dot heat engine operating close to the thermodynamic efficiency limits," *Nature Nanotechnology* **13**, 920 (2018).
