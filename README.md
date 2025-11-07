<h1 align="center">Physical Layer Security Simulation Framework</h1>


![MATLAB](https://img.shields.io/badge/MATLAB-R2024a-blue)
![License](https://img.shields.io/badge/License-MIT-green)
![Status](https://img.shields.io/badge/Type-Research_Project-red)



```mermaid
flowchart LR

    A["Message Source / Entropy Analysis"] --> B["CRC-24 Encoding"]
    B --> C["Hamming 12-8 Encoding"]
    C --> D["64-QAM Modulation"]

    D --> E["Bob Channel (AWGN)"]
    D --> F["Eve Channel (AWGN - 4 dB)"]

    E --> G["QAM Demodulation"]
    F --> H["QAM Demodulation"]

    G --> I["Hamming Decoding"]
    H --> J["Hamming Decoding"]

    I --> K["CRC Verification"]
    J --> L["CRC Verification"]

    K --> M["Recovered Message (Bob)"]
    L --> N["Recovered Message (Eve)"]

    D --> O["MIMO 3x3 Channel + Beamforming"]
    O --> P["Equalization + Demodulation"]

```



```
physical-layer-security/
│
├── source_modeling/
│   ├── entropy_analysis.m
│   ├── mutual_information.m
│   └── README.md
│
├── coding/
│   ├── computeCRC24.m
│   ├── computeHamming.m
│   ├── hamming_decode.m
│   └── README.md
│
├── modulation/
│   ├── custom_qamdemod.m
│   ├── estimate_message.m
│   ├── decodeQAM.m
│   ├── superposition_coding_demo.m
│   └── README.md
│
├── channel/
│   ├── awgn_channel.m
│   ├── mimo_channel.m
│   ├── snr_analysis.m
│   ├── snr_analysis_beamforming.m
│   └── README.md
│
├── secrecy/
│   ├── secrecy_capacity.m
│   ├── secrecy_threshold_demo.m
│   └── README.md
│
├── utils/
│   └── plots.m
│
├── figures/
│   ├── qam_constellation.png
│   ├── beamforming_diagram.png
│   ├── entropy_flowchart.png
│   ├── secrecy_curve.png
│   └── etc.
│
└── README.md
```
