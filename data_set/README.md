## Creating a dataset to improve the sound quality of throat microphones

## Overview
A sound source and evaluation numerical data set on throat microphones (pharyngeal microphones and bone conduction microphones)<br>

In the SARS-CoV-2 virus, which caused a worldwide pandemic in 2020, the spread of fine droplets produced by vocalization to the outside of the mouth is considered important as a route of infection. Droplet infection occurs when the virus leaves the mouth through vocalization. Therefore, prohibiting speech in dense conditions may efficiently block the transmission route of the virus in question. It has also been reported that the amount of droplets outside the mouth can be reduced by reducing the volume of speech. However, it is unrealistic to prohibit speech in social life. Therefore, we focused on the possibility of minimizing the spread of infectious viruses to the environment by using throat microphones (laryngeal microphones) that can capture even the slightest vocalization.
To improve the sound quality of the throat microphone, we conducted a preliminary experiment to generate control data through simultaneous recording with a high quality condenser microphone. As a result of quantitative comparisons of waveform data, frequencies and humming window values between the two using these control data and qualitative evaluations using subjects, we identified 'noises associated with neck movements' and 'swallowing sounds' as well as 'bilabial sounds' and 'silent friction sounds' as obstacles in conversations via a throat microphone. In the human evaluation of 50 sounds, those pronounced with bilabial sounds and voiceless friction sounds were difficult to understand, and the correct response rate was as low as 25%, mainly for "ma-yo", "ha-yo" and "sa-yo". By constructing a data set for filter learning based on the findings obtained in this study, it is expected to realize various conversation support technologies using a throat microphone at low sound levels. We are also convinced that this will be one of the reasons for the convergence of the current coronavirus epidemic along with the utilization of the training data.

### Contents of sound source data
Sound source data set for simultaneous recording with a throat microphone and a high quality microphone (condenser microphone in this experiment).
### Numerical data contents
- Numerical data (.csv) of each window for the above sound sources.
- Human relative voice evaluation of each line in 50 tones by voice call.
<BR><BR>
## Experimental environment
### Experimental equipment
| Outline of Equipment |  Equipment |
| ------- | -------- |
| Condenser Microphone | SHURE BETA87A Ultra Unidirectional Condenser Microphone for Vocals |
| Throat Microphone | SONONIA Headset Headphones Neckband Throat Microphone<br>・HoneyBB Mobile Phone Throat Microphone Earphone Bone Conduction Vocal Cord Microphone Tube Type |
| Audio Interface - TASCAM | SERIES 102i |
| Headphones for monitoring | Sony Stereo Headphones MDR-7506<br>Pioneer SE-M521 Headphones |
| Recording and waveform editing software | Cubase Elements 11<br>Audacity |

<img src="https://github.com/jin237/jaxtaphony_project_english/blob/main/images/ThroatMIC_Black.png" height=150px>
Figure 1 HoneyBB Mobile Phone Pharyngeal Microphone Earphone Bone Conduction Vocal Cord Microphone Tube Type
<br>
<img src="https://images-na.ssl-images-amazon.com/images/I/61Hzs8tXaQL._AC_SL1317_.jpg" height=150px>
Figure 2 SHURE BETA87A Ultra Unidirectional Vocal Condenser Microphone
<br><br><br>

### Noise Environment
Since it has been reported that the noise associated with a throat microphone is unlikely to include external factors (e.g., air conditioning, voices other than the subject's), the noise associated with a throat microphone is assumed to be that described in "Source data content - speech source - noise only source.
<br>Noise from condenser microphones will be extracted, labeled and published as air-conditioned noise.


### Program Environment
Program environment for the extraction of graphs and numbers using programs such as graph_of_wavefile.ipynb, mix_spectrum_dft.ipynb, mix_wave.ipynb
- Python 3.8.3
  - wave
  - numpy
  - matplotlib
- Jupyternotebook 6.0.3


# Sound source data content
Sound source data set for simultaneous recording with throat microphone (throat microphone, bone conduction microphone) and high quality microphone (condenser microphone in this experiment).
<br>
## Speech source
### Phrase "This is a demo sound source(Kore wa demo ongen desu)"
Six males (in their twenties) speaking the phrase "This is a demo sound source.
For each sound source data, the sound source (TM and CM) and Hamming Window were simultaneously sequenced and converted into data by each person.
<br>
### Japanese syllabary utterance
A male (in his 20s) pronounces the Japanese words in the Japanese syllabary on CosCom.
https://www.coscom.co.jp/hiragana-katakana/kanatable-j.html
<br>
### Noise-only sound sources
In this data, the following are considered to be noise<br> 
### Noise-only sources
In this data, the following noises are defined as noises only:<br> <br> <br> 
### Noises only
Noises caused by swallowing saliva or liquid<br> 
- Noises caused by connecting devices<br> 
- Noises caused by connecting devices
Sounds produced by the connection of devices<br>
The noise is labeled as follows. For each of these, the noise is labeled.
<br><br><br><br>

### Numerical data contents
### Numerical data for each window (.csv/.txt) for the above noise sources.
Data is output in the following
<br>
https://github.com/jin237/juxtaphony_throatmicrophone/blob/master/demo_github/conde_demo_spectrum.txt
<br>
https://github.com/jin237/juxtaphony_throatmicrophone/blob/master/demo_github/throat_demo_spectrum.txt
<br>
Graphical representation of these data is output in the following.
Release of numerical data for Hamming Window etc. in csv or txt files
![Spectrum graph of throat microphone](https://github.com/jin237/juxtaphony_throatmicrophone/blob/master/demo_github/throat_demo_spectrum.png)<br>
Fig. 3 Spectrum graph of a throat microphone
<br><br>
![Spectrogram of a condenser microphone](https://github.com/jin237/juxtaphony_throatmicrophone/blob/master/demo_github/conde_demo_spectrum.png)<br>
Figure 4: Spectrum graph of a condenser microphone
<br><br>
![Superimposed waveforms of throat and condenser microphones](https://github.com/jin237/juxtaphony_throatmicrophone/blob/master/demo_github/mix_wave.png)<br>
Figure 5 Superimposed waveforms of throat and condenser microphones
<br><br>
![Superimposed spectrum graphs of throat and condenser microphones](https://github.com/jin237/juxtaphony_throatmicrophone/blob/master/demo_github/mix_demo.png)<br >
Fig. 6 Superimposed spectrum graphs of a throat microphone and a condenser microphone
<br><br>

### Human relative voice evaluation of each line in 50 tones by voice call.
- The following experiments were conducted on four people, two by Skype and two by LINE, with Iino as the speaker.
- In this experiment, Iino taught the pronunciation of "a", "i", "u", "e", and "o" first, and then randomly pronounced lines such as "sa", "ma", and "ka" using communication applications (LINE and Skype) in a noisy environment.
<br> 

### Results and Discussion

- Recognition rate of "ma" line, "sa" line, "wa" and "ya": 25%
- Recognition rate for "ha" and "ka" lines: 50%
- The sound made by swallowing spit is louder than whispering.
  - Although it is sudden, it is a special sound, so it may be easy to filter.
<br><br>

# References
### Sound processing
  - [July 2018, 情報処理学会研究報告, Vol.2018-SLP-123 No.8, “深層学習に基づく特徴量変換を用いた咽喉マイクの音声認識”](https://ipsj.ixsq.nii.ac.jp/ej/?action=repository_action_common_download&item_id=190621&item_no=1&attribute_id=1&file_no=1)
  - [September 2019, INTERSPEECH 2019, "Knowledge Distillation for Throat Microphone Speech Recognition"](https://www.researchgate.net/publication/335829265_Knowledge_Distillation_for_Throat_Microphone_Speech_Recognition)
  - [Deep Learningにおける知識の蒸留](http://codecrafthouse.jp/p/2018/01/knowledge-distillation/)
  - [Proceedings, APSIPA Annual Summit and Conference 2018 12-15 November 2018, Hawaii, "Bottleneck feature-mediated DNN-based feature mapping for throat microphone speech recognition"](http://www.apsipa.org/proceedings/2018/pdfs/0001738.pdf)
  - [August, 2013, Koc University, A Thesis Submitted to the
Graduate School of Sciences and Engineering in Partial Fulfillment of the Requirements for the Degree of Master of Science in Electrical and Electronics Engineering, "Enhancement of Throat Microphone Recordings Using Gaussian Mixture Model Probabilistic Estimator"](https://arxiv.org/abs/1804.05937)
  - [January 2004, COST278 and ISCA Tutorial and Research Workshop (ITRW) on Robustness Issues in Conversational Interaction, "Combined Use of Close-Talk and Throat Microphones for Improved Speech Recognition under Non-Stationary Background Noise"](https://www.researchgate.net/publication/228889100_Combined_use_of_close-talk_and_throat_microphones_for_improved_speech_recognition_under_non-stationary_background_noise)
  - [学会誌「EICA」第 19 巻 第 2・3 合併号（2014）, p182-186, "高雑音下での声帯マイクを用いた音声認識"](http://eica.jp/search/browse.php?file=a_19_2_182.pdf&id=1202)
<br><br>
### NMF
  - [半教師あり非負値行列因子分解における音源分離性能向上のための効果的な基底学習法](https://www.slideshare.net/DaichiKitamura/ss-66384298)<br>
  - [Daniel D.Lee & H.Sebastian Seung, "Learning the parts of objects by non-negative matrix factorization"](http://www.columbia.edu/~jwp2128/Teaching/E4903/papers/nmf_nature.pdf)
  - [IBIS2018 企画セッション 招待講演, "音声分野における敵対的学習の可能性と展望"](http://ibisml.org/ibis2018/files/2018/11/takamichi.pdf)

<br><br>
### Speech Relationship
  - [June 2018, 情報処理学会研究報告, Vol.2018-SLP-122 No.33, "雑音下異常検知における前処理としてのNMF音源抽出手法の検討"](https://ipsj.ixsq.nii.ac.jp/ej/index.php?active_action=repository_view_main_item_detail&page_id=13&block_id=8&item_id=189961&item_no=1)
  - [岡山県立大学保健福祉学部紀要, 第21巻１号2014年, 45~55頁, "音声分析によるマスク着用時のコミュニケーション方法についての検討"](https://core.ac.uk/download/pdf/51452429.pdf)
  - [January 2020, Journal of Sifnal Processing, Vol.24, No.1, pp.19-29, "複数の装着型マイクを用いた多人数会話の音声認識"](https://www.jstage.jst.go.jp/article/jsp/24/1/24_19/_article/-char/ja/)

### COVID-19 etc.
  - [April 2020, New England Journal of Medicine 382(21), “Visualizing Speech-Generated Oral Fluid Droplets with Laser Light Scattering”](https://www.researchgate.net/publication/340674849_Visualizing_Speech-Generated_Oral_Fluid_Droplets_with_Laser_Light_Scattering)

