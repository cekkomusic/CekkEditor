# Chiavi delle ricette

Generato dagli editor: chiave, parametro, valori ammessi e, per le liste, il significato dei valori.

## Take 5 (chiave = numero NRPN)

| Chiave | Parametro | Valori | Opzioni |
|---|---|---|---|
| `0` | Clock · Arpeggiator › BPM | 30–249 |  |
| `167` | Clock · Arpeggiator › Clk Divide | 0–7 | 0=1/2, 1=1/4, 2=1/8, 3=1/8 T, 4=1/16, 5=1/16 T, 6=1/32, 7=1/64 |
| `163` | Clock · Arpeggiator › Arp On | 0/1 |  |
| `164` | Clock · Arpeggiator › Arp Mode | 0–4 | 0=Up, 1=Down, 2=Up+Down, 3=Random, 4=Assign |
| `165` | Clock · Arpeggiator › Octave | 0–2 |  |
| `166` | Clock · Arpeggiator › Repeat | 0–3 |  |
| `168` | Clock · Arpeggiator › Relatch | 0/1 |  |
| `8` | Oscillators › Osc 1 › Octave | 0–4 |  |
| `9` | Oscillators › Osc 1 › Pitch | 0–1400 |  |
| `10` | Oscillators › Osc 1 › Shape | 0–127 |  |
| `6` | Oscillators › Osc 1 › Sync 2-1 | 0/1 |  |
| `7` | Oscillators › Osc 1 › Key Follow | 0/1 |  |
| `13` | Oscillators › Osc 2 › Octave | 0–4 |  |
| `14` | Oscillators › Osc 2 › Pitch | 0–1400 |  |
| `15` | Oscillators › Osc 2 › Shape | 0–127 |  |
| `12` | Oscillators › Osc 2 › Key Follow | 0/1 |  |
| `4` | Oscillators › Glide › Glide | 0/1 |  |
| `2` | Oscillators › Glide › Osc1 Rate | 0–127 |  |
| `3` | Oscillators › Glide › Osc2 Rate | 0–127 |  |
| `5` | Oscillators › Glide › Glide Mode | 0–4 | 0=Fixed Rate, 1=Fixed Rate A, 2=Fixed Time, 3=Fixed Time A, 4=Modo 5 |
| `36` | Mixer › Osc 1 | 0–127 |  |
| `38` | Mixer › Osc1 Sub | 0–127 |  |
| `37` | Mixer › Osc 2 | 0–127 |  |
| `11` | Mixer › FM 2-1 | 0/1 |  |
| `39` | Mixer › Noise | 0–127 (centro 64) |  |
| `29` | Filter › Cutoff | 0–1023 |  |
| `31` | Filter › Resonance | 0–127 |  |
| `32` | Filter › Drive | 0–127 |  |
| `33` | Filter › Key Amt | 0–127 |  |
| `41` | Envelopes › Env 1 › Delay | 0–127 |  |
| `42` | Envelopes › Env 1 › Attack | 0–127 |  |
| `43` | Envelopes › Env 1 › Decay | 0–127 |  |
| `44` | Envelopes › Env 1 › Sustain | 0–127 |  |
| `45` | Envelopes › Env 1 › Release | 0–127 |  |
| `46` | Envelopes › Env 1 › Amount | 0–255 (centro 127) |  |
| `47` | Envelopes › Env 1 › Velocity | 0/1 |  |
| `40` | Envelopes › Env 1 › Aux Dest | 0–57 | 0=Nessuna, 1=Osc1 Octave, 2=Osc2 Octave, 3=Osc1 Fine, 4=Osc2 Fine, 5=Osc All Fine, 6=Osc1 Shape, 7=Osc2 Shape, 8=Osc All Shape, 9=Osc1 Level, 10=Osc2 Level, 11=Osc FM Level, 12=Sub Level, 13=Noise, 14=Drive, 15=Cutoff, 16=Resonance, 17=Overdrive, 18=Panning, 19=FX Mix, 20=FX Time, 21=FX Misc, 22=Reverb Mix, 23=Reverb Size, 24=Reverb PreDelay, 25=Reverb Decay, 26=Reverb Tone, 27=LFO1 Freq, 28=LFO2 Freq, 29=LFO All Freq, 30=LFO1 Amt, 31=LFO2 Amt, 32=LFO All Amt, 33=Env1 Amt, 34=Env2 Amt, 35=Env1 Attack, 36=Env2 Attack, 37=Env1 Decay, 38=Env2 Decay, 39=Env1 Release, 40=Env2 Release, 41=Mod1 Amt, 42=Mod2 Amt, 43=Mod3 Amt, 44=Mod4 Amt, 45=Mod5 Amt, 46=Mod6 Amt, 47=Mod7 Amt, 48=Mod8 Amt, 49=Mod9 Amt, 50=Mod10 Amt, 51=Mod11 Amt, 52=Mod12 Amt, 53=Mod13 Amt, 54=Mod14 Amt, 55=Mod15 Amt, 56=Mod16 Amt, 57=Vintage Amt |
| `48` | Envelopes › Env 2 › Delay | 0–127 |  |
| `49` | Envelopes › Env 2 › Attack | 0–127 |  |
| `50` | Envelopes › Env 2 › Decay | 0–127 |  |
| `51` | Envelopes › Env 2 › Sustain | 0–127 |  |
| `52` | Envelopes › Env 2 › Release | 0–127 |  |
| `53` | Envelopes › Env 2 › Amount | 0–255 (centro 127) |  |
| `54` | Envelopes › Env 2 › Velocity | 0/1 |  |
| `55` | Envelopes › Env 2 › Env Routing | 0–2 | 0=E1 Filter · E2 Amp, 1=E1 Aux · E2 Filt+Amp, 2=E1 Aux · E2 Filt+Gate |
| `61` | LFO 1: Global › Freq | 0–127 |  |
| `62` | LFO 1: Global › Amount | 0–255 (centro 127) |  |
| `63` | LFO 1: Global › Shape | 0–4 | 0=Triangolo, 1=Dente sega, 2=Sega inv., 3=Quadra, 4=S&H |
| `64` | LFO 1: Global › Clk Sync | 0/1 |  |
| `65` | LFO 1: Global › Sync Rate | 0–15 |  |
| `66` | LFO 1: Global › Reset | 0/1 |  |
| `67` | LFO 1: Global › Dest * | 0–57 | 0=Nessuna, 1=Osc1 Octave, 2=Osc2 Octave, 3=Osc1 Fine, 4=Osc2 Fine, 5=Osc All Fine, 6=Osc1 Shape, 7=Osc2 Shape, 8=Osc All Shape, 9=Osc1 Level, 10=Osc2 Level, 11=Osc FM Level, 12=Sub Level, 13=Noise, 14=Drive, 15=Cutoff, 16=Resonance, 17=Overdrive, 18=Panning, 19=FX Mix, 20=FX Time, 21=FX Misc, 22=Reverb Mix, 23=Reverb Size, 24=Reverb PreDelay, 25=Reverb Decay, 26=Reverb Tone, 27=LFO1 Freq, 28=LFO2 Freq, 29=LFO All Freq, 30=LFO1 Amt, 31=LFO2 Amt, 32=LFO All Amt, 33=Env1 Amt, 34=Env2 Amt, 35=Env1 Attack, 36=Env2 Attack, 37=Env1 Decay, 38=Env2 Decay, 39=Env1 Release, 40=Env2 Release, 41=Mod1 Amt, 42=Mod2 Amt, 43=Mod3 Amt, 44=Mod4 Amt, 45=Mod5 Amt, 46=Mod6 Amt, 47=Mod7 Amt, 48=Mod8 Amt, 49=Mod9 Amt, 50=Mod10 Amt, 51=Mod11 Amt, 52=Mod12 Amt, 53=Mod13 Amt, 54=Mod14 Amt, 55=Mod15 Amt, 56=Mod16 Amt, 57=Vintage Amt |
| `68` | LFO 2: Per Voice › Freq | 0–127 |  |
| `69` | LFO 2: Per Voice › Amount | 0–255 (centro 127) |  |
| `70` | LFO 2: Per Voice › Shape | 0–4 | 0=Triangolo, 1=Dente sega, 2=Sega inv., 3=Quadra, 4=S&H |
| `71` | LFO 2: Per Voice › Clk Sync | 0/1 |  |
| `72` | LFO 2: Per Voice › Sync Rate | 0–15 |  |
| `73` | LFO 2: Per Voice › Reset | 0/1 |  |
| `74` | LFO 2: Per Voice › Dest * | 0–57 | 0=Nessuna, 1=Osc1 Octave, 2=Osc2 Octave, 3=Osc1 Fine, 4=Osc2 Fine, 5=Osc All Fine, 6=Osc1 Shape, 7=Osc2 Shape, 8=Osc All Shape, 9=Osc1 Level, 10=Osc2 Level, 11=Osc FM Level, 12=Sub Level, 13=Noise, 14=Drive, 15=Cutoff, 16=Resonance, 17=Overdrive, 18=Panning, 19=FX Mix, 20=FX Time, 21=FX Misc, 22=Reverb Mix, 23=Reverb Size, 24=Reverb PreDelay, 25=Reverb Decay, 26=Reverb Tone, 27=LFO1 Freq, 28=LFO2 Freq, 29=LFO All Freq, 30=LFO1 Amt, 31=LFO2 Amt, 32=LFO All Amt, 33=Env1 Amt, 34=Env2 Amt, 35=Env1 Attack, 36=Env2 Attack, 37=Env1 Decay, 38=Env2 Decay, 39=Env1 Release, 40=Env2 Release, 41=Mod1 Amt, 42=Mod2 Amt, 43=Mod3 Amt, 44=Mod4 Amt, 45=Mod5 Amt, 46=Mod6 Amt, 47=Mod7 Amt, 48=Mod8 Amt, 49=Mod9 Amt, 50=Mod10 Amt, 51=Mod11 Amt, 52=Mod12 Amt, 53=Mod13 Amt, 54=Mod14 Amt, 55=Mod15 Amt, 56=Mod16 Amt, 57=Vintage Amt |
| `16` | Effect › FX On | 0/1 |  |
| `17` | Effect › Type | 0–11 | 0=Stereo Delay, 1=BBD, 2=Tape Delay 1, 3=Tape Delay 2, 4=Chorus, 5=Flanger, 6=Phaser, 7=HP Filter, 8=Distortion, 9=Ring Mod, 10=Rotating Speaker, 11=Lo-Fi |
| `19` | Effect › Time | 0–127 |  |
| `18` | Effect › Mix | 0–127 |  |
| `20` | Effect › Feedback | 0–127 |  |
| `21` | Effect › Clk Sync | 0/1 |  |
| `22` | Effect › Sync Rate | 0–10 |  |
| `23` | Effect › Reverb › Reverb On | 0/1 |  |
| `24` | Effect › Reverb › Mix | 0–127 |  |
| `25` | Effect › Reverb › Size | 0–127 |  |
| `26` | Effect › Reverb › Predelay | 0–127 |  |
| `27` | Effect › Reverb › Decay | 0–127 |  |
| `28` | Effect › Reverb › Tone | 0–127 |  |
| `34` | Voice · Program › Vintage | 0–127 |  |
| `35` | Voice · Program › Overdrive | 0–127 |  |
| `1` | Voice · Program › Prog Vol | 0–127 |  |
| `56` | Voice · Program › Unison › Unison | 0/1 |  |
| `57` | Voice · Program › Unison › Voices | 0–5 |  |
| `58` | Voice · Program › Unison › Detune | 0–7 |  |
| `59` | Voice · Program › Unison › Key Mode | 0–2 | 0=Low, 1=High, 2=Last |
| `60` | Voice · Program › Unison › Env Retrig | 0/1 |  |
| `75` | Voice · Program › Tastiera › Bend Up | 0–12 |  |
| `76` | Voice · Program › Tastiera › Bend Down | 0–24 |  |
| `169` | Voice · Program › Tastiera › -1 Oct | 0/1 |  |
| `171` | Voice · Program › Tastiera › -2 Oct | 0/1 |  |
| `170` | Voice · Program › Tastiera › Split | 0–44 |  |
| `4198` | Step Seq › Play | 0/1 |  |
| `4199` | Step Seq › Record | 0/1 |  |
| `77` | Mod Matrix › Src 1 | 0–19 |  |
| `93` | Mod Matrix › Amt 1 | 0–255 (centro 127) |  |
| `109` | Mod Matrix › Dst 1 | 0–57 |  |
| `78` | Mod Matrix › Src 2 | 0–19 |  |
| `94` | Mod Matrix › Amt 2 | 0–255 (centro 127) |  |
| `110` | Mod Matrix › Dst 2 | 0–57 |  |
| `79` | Mod Matrix › Src 3 | 0–19 |  |
| `95` | Mod Matrix › Amt 3 | 0–255 (centro 127) |  |
| `111` | Mod Matrix › Dst 3 | 0–57 |  |
| `80` | Mod Matrix › Src 4 | 0–19 |  |
| `96` | Mod Matrix › Amt 4 | 0–255 (centro 127) |  |
| `112` | Mod Matrix › Dst 4 | 0–57 |  |
| `81` | Mod Matrix › Src 5 | 0–19 |  |
| `97` | Mod Matrix › Amt 5 | 0–255 (centro 127) |  |
| `113` | Mod Matrix › Dst 5 | 0–57 |  |
| `82` | Mod Matrix › Src 6 | 0–19 |  |
| `98` | Mod Matrix › Amt 6 | 0–255 (centro 127) |  |
| `114` | Mod Matrix › Dst 6 | 0–57 |  |
| `83` | Mod Matrix › Src 7 | 0–19 |  |
| `99` | Mod Matrix › Amt 7 | 0–255 (centro 127) |  |
| `115` | Mod Matrix › Dst 7 | 0–57 |  |
| `84` | Mod Matrix › Src 8 | 0–19 |  |
| `100` | Mod Matrix › Amt 8 | 0–255 (centro 127) |  |
| `116` | Mod Matrix › Dst 8 | 0–57 |  |
| `85` | Mod Matrix › Src 9 | 0–19 |  |
| `101` | Mod Matrix › Amt 9 | 0–255 (centro 127) |  |
| `117` | Mod Matrix › Dst 9 | 0–57 |  |
| `86` | Mod Matrix › Src 10 | 0–19 |  |
| `102` | Mod Matrix › Amt 10 | 0–255 (centro 127) |  |
| `118` | Mod Matrix › Dst 10 | 0–57 |  |
| `87` | Mod Matrix › Src 11 | 0–19 |  |
| `103` | Mod Matrix › Amt 11 | 0–255 (centro 127) |  |
| `119` | Mod Matrix › Dst 11 | 0–57 |  |
| `88` | Mod Matrix › Src 12 | 0–19 |  |
| `104` | Mod Matrix › Amt 12 | 0–255 (centro 127) |  |
| `120` | Mod Matrix › Dst 12 | 0–57 |  |
| `89` | Mod Matrix › Src 13 | 0–19 |  |
| `105` | Mod Matrix › Amt 13 | 0–255 (centro 127) |  |
| `121` | Mod Matrix › Dst 13 | 0–57 |  |
| `90` | Mod Matrix › Src 14 | 0–19 |  |
| `106` | Mod Matrix › Amt 14 | 0–255 (centro 127) |  |
| `122` | Mod Matrix › Dst 14 | 0–57 |  |
| `91` | Mod Matrix › Src 15 | 0–19 |  |
| `107` | Mod Matrix › Amt 15 | 0–255 (centro 127) |  |
| `123` | Mod Matrix › Dst 15 | 0–57 |  |
| `92` | Mod Matrix › Src 16 | 0–19 |  |
| `108` | Mod Matrix › Amt 16 | 0–255 (centro 127) |  |
| `124` | Mod Matrix › Dst 16 | 0–57 |  |

## microKORG XL (chiave = nome del parametro; t0 = Timbre 1, t1 = Timbre 2)

| Chiave | Parametro | Valori | Opzioni |
|---|---|---|---|
| `t0.kn1` | T1 Knob Assign › Knob 1 | 0–54 | 0=Off, 1=Portamento, 2=OSC1 Ctrl1, 3=OSC1 Ctrl2, 4=Semitone, 5=OSC2 Tune, 6=OSC1 Level, 7=OSC2 Level, 8=Noise Level, 9=Cutoff1, 10=Reso1, 11=Filt Bal1, 12=EG1 Int1, 13=Cutoff2, 14=Reso2, 15=EG1 Int2, 16=Level, 17=Pan, 18=WS Depth, 19=EG1 Attack, 20=EG1 Decay, 21=EG1 Sustain, 22=EG1 Release, 23=EG2 Attack, 24=EG2 Decay, 25=EG2 Sustain, 26=EG2 Release, 27=LFO1 Freq, 28=LFO2 Freq, 29=VPatch1 Int, 30=VPatch2 Int, 31=VPatch3 Int, 32=VPatch4 Int, 33=VPatch5 Int, 34=VPatch6 Int, 35=Hi EQ Gain, 36=Lo EQ Gain, 37=FX1 Dry/Wet, 38=FX1 Ctrl1, 39=FX1 Ctrl2, 40=FX2 Dry/Wet, 41=FX2 Ctrl1, 42=FX2 Ctrl2, 43=Arp Gate, 44=Arp Oct Range, 45=Arp Swing, 46=Vc Tmb1 Lvl, 47=Vc Tmb2 Lvl, 48=Vc HPF Lvl, 49=Vc Fc Offset, 50=Vc Resonance, 51=Vc EF Sens, 52=Vc FcMod Int, 53=Vc Direct Lvl, 54=Vc Level |
| `t0.kn2` | T1 Knob Assign › Knob 2 | 0–54 | 0=Off, 1=Portamento, 2=OSC1 Ctrl1, 3=OSC1 Ctrl2, 4=Semitone, 5=OSC2 Tune, 6=OSC1 Level, 7=OSC2 Level, 8=Noise Level, 9=Cutoff1, 10=Reso1, 11=Filt Bal1, 12=EG1 Int1, 13=Cutoff2, 14=Reso2, 15=EG1 Int2, 16=Level, 17=Pan, 18=WS Depth, 19=EG1 Attack, 20=EG1 Decay, 21=EG1 Sustain, 22=EG1 Release, 23=EG2 Attack, 24=EG2 Decay, 25=EG2 Sustain, 26=EG2 Release, 27=LFO1 Freq, 28=LFO2 Freq, 29=VPatch1 Int, 30=VPatch2 Int, 31=VPatch3 Int, 32=VPatch4 Int, 33=VPatch5 Int, 34=VPatch6 Int, 35=Hi EQ Gain, 36=Lo EQ Gain, 37=FX1 Dry/Wet, 38=FX1 Ctrl1, 39=FX1 Ctrl2, 40=FX2 Dry/Wet, 41=FX2 Ctrl1, 42=FX2 Ctrl2, 43=Arp Gate, 44=Arp Oct Range, 45=Arp Swing, 46=Vc Tmb1 Lvl, 47=Vc Tmb2 Lvl, 48=Vc HPF Lvl, 49=Vc Fc Offset, 50=Vc Resonance, 51=Vc EF Sens, 52=Vc FcMod Int, 53=Vc Direct Lvl, 54=Vc Level |
| `t0.kn3` | T1 Knob Assign › Knob 3 | 0–54 | 0=Off, 1=Portamento, 2=OSC1 Ctrl1, 3=OSC1 Ctrl2, 4=Semitone, 5=OSC2 Tune, 6=OSC1 Level, 7=OSC2 Level, 8=Noise Level, 9=Cutoff1, 10=Reso1, 11=Filt Bal1, 12=EG1 Int1, 13=Cutoff2, 14=Reso2, 15=EG1 Int2, 16=Level, 17=Pan, 18=WS Depth, 19=EG1 Attack, 20=EG1 Decay, 21=EG1 Sustain, 22=EG1 Release, 23=EG2 Attack, 24=EG2 Decay, 25=EG2 Sustain, 26=EG2 Release, 27=LFO1 Freq, 28=LFO2 Freq, 29=VPatch1 Int, 30=VPatch2 Int, 31=VPatch3 Int, 32=VPatch4 Int, 33=VPatch5 Int, 34=VPatch6 Int, 35=Hi EQ Gain, 36=Lo EQ Gain, 37=FX1 Dry/Wet, 38=FX1 Ctrl1, 39=FX1 Ctrl2, 40=FX2 Dry/Wet, 41=FX2 Ctrl1, 42=FX2 Ctrl2, 43=Arp Gate, 44=Arp Oct Range, 45=Arp Swing, 46=Vc Tmb1 Lvl, 47=Vc Tmb2 Lvl, 48=Vc HPF Lvl, 49=Vc Fc Offset, 50=Vc Resonance, 51=Vc EF Sens, 52=Vc FcMod Int, 53=Vc Direct Lvl, 54=Vc Level |
| `t0.vAssign` | T1 Voice · Pitch › Voice › Voice Assign | 0–2 | 0=Mono 1, 1=Mono 2, 2=Poly |
| `t0.unison` | T1 Voice · Pitch › Voice › Unison | 0–3 | 0=Off, 1=2 Voice, 2=3 Voice, 3=4 Voice |
| `t0.unDet` | T1 Voice · Pitch › Voice › Detune | 0–99 |  |
| `t0.unSpr` | T1 Voice · Pitch › Voice › Spread | 0–127 |  |
| `t0.aTune` | T1 Voice · Pitch › Voice › Analog Tune | 0–127 |  |
| `t0.transp` | T1 Voice · Pitch › Pitch › Transpose | 16–112 (centro 64) |  |
| `t0.detune` | T1 Voice · Pitch › Pitch › Detune | 14–114 (centro 64) |  |
| `t0.vib` | T1 Voice · Pitch › Pitch › Vibrato | 1–127 (centro 64) |  |
| `t0.bend` | T1 Voice · Pitch › Pitch › Bend Range | 52–76 (centro 64) |  |
| `t0.porta` | T1 Voice · Pitch › Pitch › Portamento | 0–127 |  |
| `t0.o1wave` | T1 Oscillator 1 › Wave | 0–7 | 0=Saw, 1=Pulse, 2=Triangle, 3=Sine, 4=Formant, 5=Noise, 6=PCM/DWGS, 7=Audio In |
| `t0.o1mod` | T1 Oscillator 1 › Osc Mod | 0–3 | 0=Waveform, 1=Cross, 2=Unison, 3=VPM |
| `t0.o1c1` | T1 Oscillator 1 › Ctrl 1 | 0–127 |  |
| `t0.o1c2` | T1 Oscillator 1 › Ctrl 2 | 0–127 |  |
| `t0.o1pcm` | T1 Oscillator 1 › PCM/DWGS | 0–64 |  |
| `t0.o2wave` | T1 Oscillator 2 › Wave | 0–3 | 0=Saw, 1=Pulse, 2=Triangle, 3=Sine |
| `t0.o2mod` | T1 Oscillator 2 › Osc Mod | 0–3 | 0=Off, 1=Ring, 2=Sync, 3=Ring+Sync |
| `t0.o2semi` | T1 Oscillator 2 › Semitone | 40–88 (centro 64) |  |
| `t0.o2tune` | T1 Oscillator 2 › Tune | 1–127 (centro 64) |  |
| `t0.o1lvl` | T1 Mixer › Osc 1 | 0–127 |  |
| `t0.o2lvl` | T1 Mixer › Osc 2 | 0–127 |  |
| `t0.noise` | T1 Mixer › Noise | 0–127 |  |
| `t0.route` | T1 Filter › Routing | 0–3 | 0=Single, 1=Serial, 2=Parallel, 3=Individual |
| `t0.f1bal` | T1 Filter › Filter 1 › Type Bal | 0–127 |  |
| `t0.f1cut` | T1 Filter › Filter 1 › Cutoff | 0–127 |  |
| `t0.f1res` | T1 Filter › Filter 1 › Resonance | 0–127 |  |
| `t0.f1eg` | T1 Filter › Filter 1 › EG1 Int | 1–127 (centro 64) |  |
| `t0.f1kt` | T1 Filter › Filter 1 › Key Track | 1–127 (centro 64) |  |
| `t0.f1vel` | T1 Filter › Filter 1 › Velocity | 1–127 (centro 64) |  |
| `t0.f2type` | T1 Filter › Filter 2 › Type | 0–2 | 0=LPF, 1=HPF, 2=BPF |
| `t0.f2cut` | T1 Filter › Filter 2 › Cutoff | 0–127 |  |
| `t0.f2res` | T1 Filter › Filter 2 › Resonance | 0–127 |  |
| `t0.f2eg` | T1 Filter › Filter 2 › EG1 Int | 1–127 (centro 64) |  |
| `t0.f2kt` | T1 Filter › Filter 2 › Key Track | 1–127 (centro 64) |  |
| `t0.f2vel` | T1 Filter › Filter 2 › Velocity | 1–127 (centro 64) |  |
| `t0.level` | T1 Amp · Drive › Amp › Level | 0–127 |  |
| `t0.pan` | T1 Amp · Drive › Amp › Panpot | 0–127 (centro 64) |  |
| `t0.ampKT` | T1 Amp · Drive › Amp › Key Track | 1–127 (centro 64) |  |
| `t0.punch` | T1 Amp · Drive › Amp › Punch | 0–127 |  |
| `t0.wsType` | T1 Amp · Drive › Drive / Wave Shape › WS Type | 0–11 | 0=Off, 1=Drive, 2=Decimator, 3=Hard Clip, 4=Oct Saw, 5=Multi Tri, 6=Multi Sin, 7=SubOSC Saw, 8=SubOSC Squ, 9=SubOSC Tri, 10=SubOSC Sin, 11=Level Boost |
| `t0.wsPos` | T1 Amp · Drive › Drive / Wave Shape › Position | 0–1 | 0=Pre Filter1, 1=Pre Amp |
| `t0.wsDepth` | T1 Amp · Drive › Drive / Wave Shape › Depth | 0–127 |  |
| `t0.eg0a` | T1 Envelopes › EG1 · Filter › Attack | 0–127 |  |
| `t0.eg0d` | T1 Envelopes › EG1 · Filter › Decay | 0–127 |  |
| `t0.eg0s` | T1 Envelopes › EG1 · Filter › Sustain | 0–127 |  |
| `t0.eg0r` | T1 Envelopes › EG1 · Filter › Release | 0–127 |  |
| `t0.eg0v` | T1 Envelopes › EG1 · Filter › Velocity | 1–127 (centro 64) |  |
| `t0.eg1a` | T1 Envelopes › EG2 · Amp › Attack | 0–127 |  |
| `t0.eg1d` | T1 Envelopes › EG2 · Amp › Decay | 0–127 |  |
| `t0.eg1s` | T1 Envelopes › EG2 · Amp › Sustain | 0–127 |  |
| `t0.eg1r` | T1 Envelopes › EG2 · Amp › Release | 0–127 |  |
| `t0.eg1v` | T1 Envelopes › EG2 · Amp › Velocity | 1–127 (centro 64) |  |
| `t0.eg2a` | T1 Envelopes › EG3 › Attack | 0–127 |  |
| `t0.eg2d` | T1 Envelopes › EG3 › Decay | 0–127 |  |
| `t0.eg2s` | T1 Envelopes › EG3 › Sustain | 0–127 |  |
| `t0.eg2r` | T1 Envelopes › EG3 › Release | 0–127 |  |
| `t0.eg2v` | T1 Envelopes › EG3 › Velocity | 1–127 (centro 64) |  |
| `t0.lfo1w` | T1 LFO › LFO 1 › Wave | 0–4 | 0=Saw, 1=Square, 2=Triangle, 3=S/H, 4=Random |
| `t0.lfo1f` | T1 LFO › LFO 1 › Freq | 0–127 |  |
| `t0.lfo1bpm` | T1 LFO › LFO 1 › BPM Sync | 0/1 |  |
| `t0.lfo1key` | T1 LFO › LFO 1 › Key Sync | 0–2 | 0=Off, 1=Timbre, 2=Voice |
| `t0.lfo1n` | T1 LFO › LFO 1 › Sync Note | 0–16 | 0=8/1, 1=4/1, 2=2/1, 3=1/1, 4=3/4, 5=1/2, 6=3/8, 7=1/3, 8=1/4, 9=3/16, 10=1/6, 11=1/8, 12=1/12, 13=1/16, 14=1/24, 15=1/32, 16=1/64 |
| `t0.lfo2w` | T1 LFO › LFO 2 › Wave | 0–4 | 0=Saw, 1=Square+, 2=Sine, 3=S/H, 4=Random |
| `t0.lfo2f` | T1 LFO › LFO 2 › Freq | 0–127 |  |
| `t0.lfo2bpm` | T1 LFO › LFO 2 › BPM Sync | 0/1 |  |
| `t0.lfo2key` | T1 LFO › LFO 2 › Key Sync | 0–2 | 0=Off, 1=Timbre, 2=Voice |
| `t0.lfo2n` | T1 LFO › LFO 2 › Sync Note | 0–16 | 0=8/1, 1=4/1, 2=2/1, 3=1/1, 4=3/4, 5=1/2, 6=3/8, 7=1/3, 8=1/4, 9=3/16, 10=1/6, 11=1/8, 12=1/12, 13=1/16, 14=1/24, 15=1/32, 16=1/64 |
| `t0.pt0s` | T1 Virtual Patch › Source | 0–11 | 0=EG1, 1=EG2, 2=EG3, 3=LFO1, 4=LFO2, 5=Velocity, 6=Pitch Bend, 7=Mod Wheel, 8=Key Track, 9=MIDI1, 10=MIDI2, 11=MIDI3 |
| `t0.pt0d` | T1 Virtual Patch › Dest | 0–39 | 0=Pitch, 1=OSC2 Tune, 2=OSC1 Ctrl1, 3=OSC1 Level, 4=OSC2 Level, 5=Noise Level, 6=Filt1 Balance, 7=Filt1 Cutoff, 8=Filt1 Reso, 9=Filt2 Cutoff, 10=Drive/WS Depth, 11=Amp Level, 12=Panpot, 13=LFO1 Freq, 14=LFO2 Freq, 15=Portamento, 16=OSC1 Ctrl2, 17=Filt1 EG1, 18=Filt1 KeyTrack, 19=Filt2 Reso, 20=Filt2 EG1, 21=Filt2 KeyTrack, 22=EG1 Attack, 23=EG1 Decay, 24=EG1 Sustain, 25=EG1 Release, 26=EG2 Attack, 27=EG2 Decay, 28=EG2 Sustain, 29=EG2 Release, 30=EG3 Attack, 31=EG3 Decay, 32=EG3 Sustain, 33=EG3 Release, 34=Patch1 Int, 35=Patch2 Int, 36=Patch3 Int, 37=Patch4 Int, 38=Patch5 Int, 39=Patch6 Int |
| `t0.pt0i` | T1 Virtual Patch › Int | 1–127 (centro 64) |  |
| `t0.pt1s` | T1 Virtual Patch › Source | 0–11 | 0=EG1, 1=EG2, 2=EG3, 3=LFO1, 4=LFO2, 5=Velocity, 6=Pitch Bend, 7=Mod Wheel, 8=Key Track, 9=MIDI1, 10=MIDI2, 11=MIDI3 |
| `t0.pt1d` | T1 Virtual Patch › Dest | 0–39 | 0=Pitch, 1=OSC2 Tune, 2=OSC1 Ctrl1, 3=OSC1 Level, 4=OSC2 Level, 5=Noise Level, 6=Filt1 Balance, 7=Filt1 Cutoff, 8=Filt1 Reso, 9=Filt2 Cutoff, 10=Drive/WS Depth, 11=Amp Level, 12=Panpot, 13=LFO1 Freq, 14=LFO2 Freq, 15=Portamento, 16=OSC1 Ctrl2, 17=Filt1 EG1, 18=Filt1 KeyTrack, 19=Filt2 Reso, 20=Filt2 EG1, 21=Filt2 KeyTrack, 22=EG1 Attack, 23=EG1 Decay, 24=EG1 Sustain, 25=EG1 Release, 26=EG2 Attack, 27=EG2 Decay, 28=EG2 Sustain, 29=EG2 Release, 30=EG3 Attack, 31=EG3 Decay, 32=EG3 Sustain, 33=EG3 Release, 34=Patch1 Int, 35=Patch2 Int, 36=Patch3 Int, 37=Patch4 Int, 38=Patch5 Int, 39=Patch6 Int |
| `t0.pt1i` | T1 Virtual Patch › Int | 1–127 (centro 64) |  |
| `t0.pt2s` | T1 Virtual Patch › Source | 0–11 | 0=EG1, 1=EG2, 2=EG3, 3=LFO1, 4=LFO2, 5=Velocity, 6=Pitch Bend, 7=Mod Wheel, 8=Key Track, 9=MIDI1, 10=MIDI2, 11=MIDI3 |
| `t0.pt2d` | T1 Virtual Patch › Dest | 0–39 | 0=Pitch, 1=OSC2 Tune, 2=OSC1 Ctrl1, 3=OSC1 Level, 4=OSC2 Level, 5=Noise Level, 6=Filt1 Balance, 7=Filt1 Cutoff, 8=Filt1 Reso, 9=Filt2 Cutoff, 10=Drive/WS Depth, 11=Amp Level, 12=Panpot, 13=LFO1 Freq, 14=LFO2 Freq, 15=Portamento, 16=OSC1 Ctrl2, 17=Filt1 EG1, 18=Filt1 KeyTrack, 19=Filt2 Reso, 20=Filt2 EG1, 21=Filt2 KeyTrack, 22=EG1 Attack, 23=EG1 Decay, 24=EG1 Sustain, 25=EG1 Release, 26=EG2 Attack, 27=EG2 Decay, 28=EG2 Sustain, 29=EG2 Release, 30=EG3 Attack, 31=EG3 Decay, 32=EG3 Sustain, 33=EG3 Release, 34=Patch1 Int, 35=Patch2 Int, 36=Patch3 Int, 37=Patch4 Int, 38=Patch5 Int, 39=Patch6 Int |
| `t0.pt2i` | T1 Virtual Patch › Int | 1–127 (centro 64) |  |
| `t0.pt3s` | T1 Virtual Patch › Source | 0–11 | 0=EG1, 1=EG2, 2=EG3, 3=LFO1, 4=LFO2, 5=Velocity, 6=Pitch Bend, 7=Mod Wheel, 8=Key Track, 9=MIDI1, 10=MIDI2, 11=MIDI3 |
| `t0.pt3d` | T1 Virtual Patch › Dest | 0–39 | 0=Pitch, 1=OSC2 Tune, 2=OSC1 Ctrl1, 3=OSC1 Level, 4=OSC2 Level, 5=Noise Level, 6=Filt1 Balance, 7=Filt1 Cutoff, 8=Filt1 Reso, 9=Filt2 Cutoff, 10=Drive/WS Depth, 11=Amp Level, 12=Panpot, 13=LFO1 Freq, 14=LFO2 Freq, 15=Portamento, 16=OSC1 Ctrl2, 17=Filt1 EG1, 18=Filt1 KeyTrack, 19=Filt2 Reso, 20=Filt2 EG1, 21=Filt2 KeyTrack, 22=EG1 Attack, 23=EG1 Decay, 24=EG1 Sustain, 25=EG1 Release, 26=EG2 Attack, 27=EG2 Decay, 28=EG2 Sustain, 29=EG2 Release, 30=EG3 Attack, 31=EG3 Decay, 32=EG3 Sustain, 33=EG3 Release, 34=Patch1 Int, 35=Patch2 Int, 36=Patch3 Int, 37=Patch4 Int, 38=Patch5 Int, 39=Patch6 Int |
| `t0.pt3i` | T1 Virtual Patch › Int | 1–127 (centro 64) |  |
| `t0.pt4s` | T1 Virtual Patch › Source | 0–11 | 0=EG1, 1=EG2, 2=EG3, 3=LFO1, 4=LFO2, 5=Velocity, 6=Pitch Bend, 7=Mod Wheel, 8=Key Track, 9=MIDI1, 10=MIDI2, 11=MIDI3 |
| `t0.pt4d` | T1 Virtual Patch › Dest | 0–39 | 0=Pitch, 1=OSC2 Tune, 2=OSC1 Ctrl1, 3=OSC1 Level, 4=OSC2 Level, 5=Noise Level, 6=Filt1 Balance, 7=Filt1 Cutoff, 8=Filt1 Reso, 9=Filt2 Cutoff, 10=Drive/WS Depth, 11=Amp Level, 12=Panpot, 13=LFO1 Freq, 14=LFO2 Freq, 15=Portamento, 16=OSC1 Ctrl2, 17=Filt1 EG1, 18=Filt1 KeyTrack, 19=Filt2 Reso, 20=Filt2 EG1, 21=Filt2 KeyTrack, 22=EG1 Attack, 23=EG1 Decay, 24=EG1 Sustain, 25=EG1 Release, 26=EG2 Attack, 27=EG2 Decay, 28=EG2 Sustain, 29=EG2 Release, 30=EG3 Attack, 31=EG3 Decay, 32=EG3 Sustain, 33=EG3 Release, 34=Patch1 Int, 35=Patch2 Int, 36=Patch3 Int, 37=Patch4 Int, 38=Patch5 Int, 39=Patch6 Int |
| `t0.pt4i` | T1 Virtual Patch › Int | 1–127 (centro 64) |  |
| `t0.pt5s` | T1 Virtual Patch › Source | 0–11 | 0=EG1, 1=EG2, 2=EG3, 3=LFO1, 4=LFO2, 5=Velocity, 6=Pitch Bend, 7=Mod Wheel, 8=Key Track, 9=MIDI1, 10=MIDI2, 11=MIDI3 |
| `t0.pt5d` | T1 Virtual Patch › Dest | 0–39 | 0=Pitch, 1=OSC2 Tune, 2=OSC1 Ctrl1, 3=OSC1 Level, 4=OSC2 Level, 5=Noise Level, 6=Filt1 Balance, 7=Filt1 Cutoff, 8=Filt1 Reso, 9=Filt2 Cutoff, 10=Drive/WS Depth, 11=Amp Level, 12=Panpot, 13=LFO1 Freq, 14=LFO2 Freq, 15=Portamento, 16=OSC1 Ctrl2, 17=Filt1 EG1, 18=Filt1 KeyTrack, 19=Filt2 Reso, 20=Filt2 EG1, 21=Filt2 KeyTrack, 22=EG1 Attack, 23=EG1 Decay, 24=EG1 Sustain, 25=EG1 Release, 26=EG2 Attack, 27=EG2 Decay, 28=EG2 Sustain, 29=EG2 Release, 30=EG3 Attack, 31=EG3 Decay, 32=EG3 Sustain, 33=EG3 Release, 34=Patch1 Int, 35=Patch2 Int, 36=Patch3 Int, 37=Patch4 Int, 38=Patch5 Int, 39=Patch6 Int |
| `t0.pt5i` | T1 Virtual Patch › Int | 1–127 (centro 64) |  |
| `t0.eqLf` | T1 EQ › Low Freq | 0–33 |  |
| `t0.eqLg` | T1 EQ › Low Gain | 34–94 (centro 64) |  |
| `t0.eqHf` | T1 EQ › Hi Freq | 0–25 |  |
| `t0.eqHg` | T1 EQ › Hi Gain | 34–94 (centro 64) |  |
| `t1.kn1` | T2 Knob Assign › Knob 1 | 0–54 | 0=Off, 1=Portamento, 2=OSC1 Ctrl1, 3=OSC1 Ctrl2, 4=Semitone, 5=OSC2 Tune, 6=OSC1 Level, 7=OSC2 Level, 8=Noise Level, 9=Cutoff1, 10=Reso1, 11=Filt Bal1, 12=EG1 Int1, 13=Cutoff2, 14=Reso2, 15=EG1 Int2, 16=Level, 17=Pan, 18=WS Depth, 19=EG1 Attack, 20=EG1 Decay, 21=EG1 Sustain, 22=EG1 Release, 23=EG2 Attack, 24=EG2 Decay, 25=EG2 Sustain, 26=EG2 Release, 27=LFO1 Freq, 28=LFO2 Freq, 29=VPatch1 Int, 30=VPatch2 Int, 31=VPatch3 Int, 32=VPatch4 Int, 33=VPatch5 Int, 34=VPatch6 Int, 35=Hi EQ Gain, 36=Lo EQ Gain, 37=FX1 Dry/Wet, 38=FX1 Ctrl1, 39=FX1 Ctrl2, 40=FX2 Dry/Wet, 41=FX2 Ctrl1, 42=FX2 Ctrl2, 43=Arp Gate, 44=Arp Oct Range, 45=Arp Swing, 46=Vc Tmb1 Lvl, 47=Vc Tmb2 Lvl, 48=Vc HPF Lvl, 49=Vc Fc Offset, 50=Vc Resonance, 51=Vc EF Sens, 52=Vc FcMod Int, 53=Vc Direct Lvl, 54=Vc Level |
| `t1.kn2` | T2 Knob Assign › Knob 2 | 0–54 | 0=Off, 1=Portamento, 2=OSC1 Ctrl1, 3=OSC1 Ctrl2, 4=Semitone, 5=OSC2 Tune, 6=OSC1 Level, 7=OSC2 Level, 8=Noise Level, 9=Cutoff1, 10=Reso1, 11=Filt Bal1, 12=EG1 Int1, 13=Cutoff2, 14=Reso2, 15=EG1 Int2, 16=Level, 17=Pan, 18=WS Depth, 19=EG1 Attack, 20=EG1 Decay, 21=EG1 Sustain, 22=EG1 Release, 23=EG2 Attack, 24=EG2 Decay, 25=EG2 Sustain, 26=EG2 Release, 27=LFO1 Freq, 28=LFO2 Freq, 29=VPatch1 Int, 30=VPatch2 Int, 31=VPatch3 Int, 32=VPatch4 Int, 33=VPatch5 Int, 34=VPatch6 Int, 35=Hi EQ Gain, 36=Lo EQ Gain, 37=FX1 Dry/Wet, 38=FX1 Ctrl1, 39=FX1 Ctrl2, 40=FX2 Dry/Wet, 41=FX2 Ctrl1, 42=FX2 Ctrl2, 43=Arp Gate, 44=Arp Oct Range, 45=Arp Swing, 46=Vc Tmb1 Lvl, 47=Vc Tmb2 Lvl, 48=Vc HPF Lvl, 49=Vc Fc Offset, 50=Vc Resonance, 51=Vc EF Sens, 52=Vc FcMod Int, 53=Vc Direct Lvl, 54=Vc Level |
| `t1.kn3` | T2 Knob Assign › Knob 3 | 0–54 | 0=Off, 1=Portamento, 2=OSC1 Ctrl1, 3=OSC1 Ctrl2, 4=Semitone, 5=OSC2 Tune, 6=OSC1 Level, 7=OSC2 Level, 8=Noise Level, 9=Cutoff1, 10=Reso1, 11=Filt Bal1, 12=EG1 Int1, 13=Cutoff2, 14=Reso2, 15=EG1 Int2, 16=Level, 17=Pan, 18=WS Depth, 19=EG1 Attack, 20=EG1 Decay, 21=EG1 Sustain, 22=EG1 Release, 23=EG2 Attack, 24=EG2 Decay, 25=EG2 Sustain, 26=EG2 Release, 27=LFO1 Freq, 28=LFO2 Freq, 29=VPatch1 Int, 30=VPatch2 Int, 31=VPatch3 Int, 32=VPatch4 Int, 33=VPatch5 Int, 34=VPatch6 Int, 35=Hi EQ Gain, 36=Lo EQ Gain, 37=FX1 Dry/Wet, 38=FX1 Ctrl1, 39=FX1 Ctrl2, 40=FX2 Dry/Wet, 41=FX2 Ctrl1, 42=FX2 Ctrl2, 43=Arp Gate, 44=Arp Oct Range, 45=Arp Swing, 46=Vc Tmb1 Lvl, 47=Vc Tmb2 Lvl, 48=Vc HPF Lvl, 49=Vc Fc Offset, 50=Vc Resonance, 51=Vc EF Sens, 52=Vc FcMod Int, 53=Vc Direct Lvl, 54=Vc Level |
| `t1.vAssign` | T2 Voice · Pitch › Voice › Voice Assign | 0–2 | 0=Mono 1, 1=Mono 2, 2=Poly |
| `t1.unison` | T2 Voice · Pitch › Voice › Unison | 0–3 | 0=Off, 1=2 Voice, 2=3 Voice, 3=4 Voice |
| `t1.unDet` | T2 Voice · Pitch › Voice › Detune | 0–99 |  |
| `t1.unSpr` | T2 Voice · Pitch › Voice › Spread | 0–127 |  |
| `t1.aTune` | T2 Voice · Pitch › Voice › Analog Tune | 0–127 |  |
| `t1.transp` | T2 Voice · Pitch › Pitch › Transpose | 16–112 (centro 64) |  |
| `t1.detune` | T2 Voice · Pitch › Pitch › Detune | 14–114 (centro 64) |  |
| `t1.vib` | T2 Voice · Pitch › Pitch › Vibrato | 1–127 (centro 64) |  |
| `t1.bend` | T2 Voice · Pitch › Pitch › Bend Range | 52–76 (centro 64) |  |
| `t1.porta` | T2 Voice · Pitch › Pitch › Portamento | 0–127 |  |
| `t1.o1wave` | T2 Oscillator 1 › Wave | 0–7 | 0=Saw, 1=Pulse, 2=Triangle, 3=Sine, 4=Formant, 5=Noise, 6=PCM/DWGS, 7=Audio In |
| `t1.o1mod` | T2 Oscillator 1 › Osc Mod | 0–3 | 0=Waveform, 1=Cross, 2=Unison, 3=VPM |
| `t1.o1c1` | T2 Oscillator 1 › Ctrl 1 | 0–127 |  |
| `t1.o1c2` | T2 Oscillator 1 › Ctrl 2 | 0–127 |  |
| `t1.o1pcm` | T2 Oscillator 1 › PCM/DWGS | 0–64 |  |
| `t1.o2wave` | T2 Oscillator 2 › Wave | 0–3 | 0=Saw, 1=Pulse, 2=Triangle, 3=Sine |
| `t1.o2mod` | T2 Oscillator 2 › Osc Mod | 0–3 | 0=Off, 1=Ring, 2=Sync, 3=Ring+Sync |
| `t1.o2semi` | T2 Oscillator 2 › Semitone | 40–88 (centro 64) |  |
| `t1.o2tune` | T2 Oscillator 2 › Tune | 1–127 (centro 64) |  |
| `t1.o1lvl` | T2 Mixer › Osc 1 | 0–127 |  |
| `t1.o2lvl` | T2 Mixer › Osc 2 | 0–127 |  |
| `t1.noise` | T2 Mixer › Noise | 0–127 |  |
| `t1.route` | T2 Filter › Routing | 0–3 | 0=Single, 1=Serial, 2=Parallel, 3=Individual |
| `t1.f1bal` | T2 Filter › Filter 1 › Type Bal | 0–127 |  |
| `t1.f1cut` | T2 Filter › Filter 1 › Cutoff | 0–127 |  |
| `t1.f1res` | T2 Filter › Filter 1 › Resonance | 0–127 |  |
| `t1.f1eg` | T2 Filter › Filter 1 › EG1 Int | 1–127 (centro 64) |  |
| `t1.f1kt` | T2 Filter › Filter 1 › Key Track | 1–127 (centro 64) |  |
| `t1.f1vel` | T2 Filter › Filter 1 › Velocity | 1–127 (centro 64) |  |
| `t1.f2type` | T2 Filter › Filter 2 › Type | 0–2 | 0=LPF, 1=HPF, 2=BPF |
| `t1.f2cut` | T2 Filter › Filter 2 › Cutoff | 0–127 |  |
| `t1.f2res` | T2 Filter › Filter 2 › Resonance | 0–127 |  |
| `t1.f2eg` | T2 Filter › Filter 2 › EG1 Int | 1–127 (centro 64) |  |
| `t1.f2kt` | T2 Filter › Filter 2 › Key Track | 1–127 (centro 64) |  |
| `t1.f2vel` | T2 Filter › Filter 2 › Velocity | 1–127 (centro 64) |  |
| `t1.level` | T2 Amp · Drive › Amp › Level | 0–127 |  |
| `t1.pan` | T2 Amp · Drive › Amp › Panpot | 0–127 (centro 64) |  |
| `t1.ampKT` | T2 Amp · Drive › Amp › Key Track | 1–127 (centro 64) |  |
| `t1.punch` | T2 Amp · Drive › Amp › Punch | 0–127 |  |
| `t1.wsType` | T2 Amp · Drive › Drive / Wave Shape › WS Type | 0–11 | 0=Off, 1=Drive, 2=Decimator, 3=Hard Clip, 4=Oct Saw, 5=Multi Tri, 6=Multi Sin, 7=SubOSC Saw, 8=SubOSC Squ, 9=SubOSC Tri, 10=SubOSC Sin, 11=Level Boost |
| `t1.wsPos` | T2 Amp · Drive › Drive / Wave Shape › Position | 0–1 | 0=Pre Filter1, 1=Pre Amp |
| `t1.wsDepth` | T2 Amp · Drive › Drive / Wave Shape › Depth | 0–127 |  |
| `t1.eg0a` | T2 Envelopes › EG1 · Filter › Attack | 0–127 |  |
| `t1.eg0d` | T2 Envelopes › EG1 · Filter › Decay | 0–127 |  |
| `t1.eg0s` | T2 Envelopes › EG1 · Filter › Sustain | 0–127 |  |
| `t1.eg0r` | T2 Envelopes › EG1 · Filter › Release | 0–127 |  |
| `t1.eg0v` | T2 Envelopes › EG1 · Filter › Velocity | 1–127 (centro 64) |  |
| `t1.eg1a` | T2 Envelopes › EG2 · Amp › Attack | 0–127 |  |
| `t1.eg1d` | T2 Envelopes › EG2 · Amp › Decay | 0–127 |  |
| `t1.eg1s` | T2 Envelopes › EG2 · Amp › Sustain | 0–127 |  |
| `t1.eg1r` | T2 Envelopes › EG2 · Amp › Release | 0–127 |  |
| `t1.eg1v` | T2 Envelopes › EG2 · Amp › Velocity | 1–127 (centro 64) |  |
| `t1.eg2a` | T2 Envelopes › EG3 › Attack | 0–127 |  |
| `t1.eg2d` | T2 Envelopes › EG3 › Decay | 0–127 |  |
| `t1.eg2s` | T2 Envelopes › EG3 › Sustain | 0–127 |  |
| `t1.eg2r` | T2 Envelopes › EG3 › Release | 0–127 |  |
| `t1.eg2v` | T2 Envelopes › EG3 › Velocity | 1–127 (centro 64) |  |
| `t1.lfo1w` | T2 LFO › LFO 1 › Wave | 0–4 | 0=Saw, 1=Square, 2=Triangle, 3=S/H, 4=Random |
| `t1.lfo1f` | T2 LFO › LFO 1 › Freq | 0–127 |  |
| `t1.lfo1bpm` | T2 LFO › LFO 1 › BPM Sync | 0/1 |  |
| `t1.lfo1key` | T2 LFO › LFO 1 › Key Sync | 0–2 | 0=Off, 1=Timbre, 2=Voice |
| `t1.lfo1n` | T2 LFO › LFO 1 › Sync Note | 0–16 | 0=8/1, 1=4/1, 2=2/1, 3=1/1, 4=3/4, 5=1/2, 6=3/8, 7=1/3, 8=1/4, 9=3/16, 10=1/6, 11=1/8, 12=1/12, 13=1/16, 14=1/24, 15=1/32, 16=1/64 |
| `t1.lfo2w` | T2 LFO › LFO 2 › Wave | 0–4 | 0=Saw, 1=Square+, 2=Sine, 3=S/H, 4=Random |
| `t1.lfo2f` | T2 LFO › LFO 2 › Freq | 0–127 |  |
| `t1.lfo2bpm` | T2 LFO › LFO 2 › BPM Sync | 0/1 |  |
| `t1.lfo2key` | T2 LFO › LFO 2 › Key Sync | 0–2 | 0=Off, 1=Timbre, 2=Voice |
| `t1.lfo2n` | T2 LFO › LFO 2 › Sync Note | 0–16 | 0=8/1, 1=4/1, 2=2/1, 3=1/1, 4=3/4, 5=1/2, 6=3/8, 7=1/3, 8=1/4, 9=3/16, 10=1/6, 11=1/8, 12=1/12, 13=1/16, 14=1/24, 15=1/32, 16=1/64 |
| `t1.pt0s` | T2 Virtual Patch › Source | 0–11 | 0=EG1, 1=EG2, 2=EG3, 3=LFO1, 4=LFO2, 5=Velocity, 6=Pitch Bend, 7=Mod Wheel, 8=Key Track, 9=MIDI1, 10=MIDI2, 11=MIDI3 |
| `t1.pt0d` | T2 Virtual Patch › Dest | 0–39 | 0=Pitch, 1=OSC2 Tune, 2=OSC1 Ctrl1, 3=OSC1 Level, 4=OSC2 Level, 5=Noise Level, 6=Filt1 Balance, 7=Filt1 Cutoff, 8=Filt1 Reso, 9=Filt2 Cutoff, 10=Drive/WS Depth, 11=Amp Level, 12=Panpot, 13=LFO1 Freq, 14=LFO2 Freq, 15=Portamento, 16=OSC1 Ctrl2, 17=Filt1 EG1, 18=Filt1 KeyTrack, 19=Filt2 Reso, 20=Filt2 EG1, 21=Filt2 KeyTrack, 22=EG1 Attack, 23=EG1 Decay, 24=EG1 Sustain, 25=EG1 Release, 26=EG2 Attack, 27=EG2 Decay, 28=EG2 Sustain, 29=EG2 Release, 30=EG3 Attack, 31=EG3 Decay, 32=EG3 Sustain, 33=EG3 Release, 34=Patch1 Int, 35=Patch2 Int, 36=Patch3 Int, 37=Patch4 Int, 38=Patch5 Int, 39=Patch6 Int |
| `t1.pt0i` | T2 Virtual Patch › Int | 1–127 (centro 64) |  |
| `t1.pt1s` | T2 Virtual Patch › Source | 0–11 | 0=EG1, 1=EG2, 2=EG3, 3=LFO1, 4=LFO2, 5=Velocity, 6=Pitch Bend, 7=Mod Wheel, 8=Key Track, 9=MIDI1, 10=MIDI2, 11=MIDI3 |
| `t1.pt1d` | T2 Virtual Patch › Dest | 0–39 | 0=Pitch, 1=OSC2 Tune, 2=OSC1 Ctrl1, 3=OSC1 Level, 4=OSC2 Level, 5=Noise Level, 6=Filt1 Balance, 7=Filt1 Cutoff, 8=Filt1 Reso, 9=Filt2 Cutoff, 10=Drive/WS Depth, 11=Amp Level, 12=Panpot, 13=LFO1 Freq, 14=LFO2 Freq, 15=Portamento, 16=OSC1 Ctrl2, 17=Filt1 EG1, 18=Filt1 KeyTrack, 19=Filt2 Reso, 20=Filt2 EG1, 21=Filt2 KeyTrack, 22=EG1 Attack, 23=EG1 Decay, 24=EG1 Sustain, 25=EG1 Release, 26=EG2 Attack, 27=EG2 Decay, 28=EG2 Sustain, 29=EG2 Release, 30=EG3 Attack, 31=EG3 Decay, 32=EG3 Sustain, 33=EG3 Release, 34=Patch1 Int, 35=Patch2 Int, 36=Patch3 Int, 37=Patch4 Int, 38=Patch5 Int, 39=Patch6 Int |
| `t1.pt1i` | T2 Virtual Patch › Int | 1–127 (centro 64) |  |
| `t1.pt2s` | T2 Virtual Patch › Source | 0–11 | 0=EG1, 1=EG2, 2=EG3, 3=LFO1, 4=LFO2, 5=Velocity, 6=Pitch Bend, 7=Mod Wheel, 8=Key Track, 9=MIDI1, 10=MIDI2, 11=MIDI3 |
| `t1.pt2d` | T2 Virtual Patch › Dest | 0–39 | 0=Pitch, 1=OSC2 Tune, 2=OSC1 Ctrl1, 3=OSC1 Level, 4=OSC2 Level, 5=Noise Level, 6=Filt1 Balance, 7=Filt1 Cutoff, 8=Filt1 Reso, 9=Filt2 Cutoff, 10=Drive/WS Depth, 11=Amp Level, 12=Panpot, 13=LFO1 Freq, 14=LFO2 Freq, 15=Portamento, 16=OSC1 Ctrl2, 17=Filt1 EG1, 18=Filt1 KeyTrack, 19=Filt2 Reso, 20=Filt2 EG1, 21=Filt2 KeyTrack, 22=EG1 Attack, 23=EG1 Decay, 24=EG1 Sustain, 25=EG1 Release, 26=EG2 Attack, 27=EG2 Decay, 28=EG2 Sustain, 29=EG2 Release, 30=EG3 Attack, 31=EG3 Decay, 32=EG3 Sustain, 33=EG3 Release, 34=Patch1 Int, 35=Patch2 Int, 36=Patch3 Int, 37=Patch4 Int, 38=Patch5 Int, 39=Patch6 Int |
| `t1.pt2i` | T2 Virtual Patch › Int | 1–127 (centro 64) |  |
| `t1.pt3s` | T2 Virtual Patch › Source | 0–11 | 0=EG1, 1=EG2, 2=EG3, 3=LFO1, 4=LFO2, 5=Velocity, 6=Pitch Bend, 7=Mod Wheel, 8=Key Track, 9=MIDI1, 10=MIDI2, 11=MIDI3 |
| `t1.pt3d` | T2 Virtual Patch › Dest | 0–39 | 0=Pitch, 1=OSC2 Tune, 2=OSC1 Ctrl1, 3=OSC1 Level, 4=OSC2 Level, 5=Noise Level, 6=Filt1 Balance, 7=Filt1 Cutoff, 8=Filt1 Reso, 9=Filt2 Cutoff, 10=Drive/WS Depth, 11=Amp Level, 12=Panpot, 13=LFO1 Freq, 14=LFO2 Freq, 15=Portamento, 16=OSC1 Ctrl2, 17=Filt1 EG1, 18=Filt1 KeyTrack, 19=Filt2 Reso, 20=Filt2 EG1, 21=Filt2 KeyTrack, 22=EG1 Attack, 23=EG1 Decay, 24=EG1 Sustain, 25=EG1 Release, 26=EG2 Attack, 27=EG2 Decay, 28=EG2 Sustain, 29=EG2 Release, 30=EG3 Attack, 31=EG3 Decay, 32=EG3 Sustain, 33=EG3 Release, 34=Patch1 Int, 35=Patch2 Int, 36=Patch3 Int, 37=Patch4 Int, 38=Patch5 Int, 39=Patch6 Int |
| `t1.pt3i` | T2 Virtual Patch › Int | 1–127 (centro 64) |  |
| `t1.pt4s` | T2 Virtual Patch › Source | 0–11 | 0=EG1, 1=EG2, 2=EG3, 3=LFO1, 4=LFO2, 5=Velocity, 6=Pitch Bend, 7=Mod Wheel, 8=Key Track, 9=MIDI1, 10=MIDI2, 11=MIDI3 |
| `t1.pt4d` | T2 Virtual Patch › Dest | 0–39 | 0=Pitch, 1=OSC2 Tune, 2=OSC1 Ctrl1, 3=OSC1 Level, 4=OSC2 Level, 5=Noise Level, 6=Filt1 Balance, 7=Filt1 Cutoff, 8=Filt1 Reso, 9=Filt2 Cutoff, 10=Drive/WS Depth, 11=Amp Level, 12=Panpot, 13=LFO1 Freq, 14=LFO2 Freq, 15=Portamento, 16=OSC1 Ctrl2, 17=Filt1 EG1, 18=Filt1 KeyTrack, 19=Filt2 Reso, 20=Filt2 EG1, 21=Filt2 KeyTrack, 22=EG1 Attack, 23=EG1 Decay, 24=EG1 Sustain, 25=EG1 Release, 26=EG2 Attack, 27=EG2 Decay, 28=EG2 Sustain, 29=EG2 Release, 30=EG3 Attack, 31=EG3 Decay, 32=EG3 Sustain, 33=EG3 Release, 34=Patch1 Int, 35=Patch2 Int, 36=Patch3 Int, 37=Patch4 Int, 38=Patch5 Int, 39=Patch6 Int |
| `t1.pt4i` | T2 Virtual Patch › Int | 1–127 (centro 64) |  |
| `t1.pt5s` | T2 Virtual Patch › Source | 0–11 | 0=EG1, 1=EG2, 2=EG3, 3=LFO1, 4=LFO2, 5=Velocity, 6=Pitch Bend, 7=Mod Wheel, 8=Key Track, 9=MIDI1, 10=MIDI2, 11=MIDI3 |
| `t1.pt5d` | T2 Virtual Patch › Dest | 0–39 | 0=Pitch, 1=OSC2 Tune, 2=OSC1 Ctrl1, 3=OSC1 Level, 4=OSC2 Level, 5=Noise Level, 6=Filt1 Balance, 7=Filt1 Cutoff, 8=Filt1 Reso, 9=Filt2 Cutoff, 10=Drive/WS Depth, 11=Amp Level, 12=Panpot, 13=LFO1 Freq, 14=LFO2 Freq, 15=Portamento, 16=OSC1 Ctrl2, 17=Filt1 EG1, 18=Filt1 KeyTrack, 19=Filt2 Reso, 20=Filt2 EG1, 21=Filt2 KeyTrack, 22=EG1 Attack, 23=EG1 Decay, 24=EG1 Sustain, 25=EG1 Release, 26=EG2 Attack, 27=EG2 Decay, 28=EG2 Sustain, 29=EG2 Release, 30=EG3 Attack, 31=EG3 Decay, 32=EG3 Sustain, 33=EG3 Release, 34=Patch1 Int, 35=Patch2 Int, 36=Patch3 Int, 37=Patch4 Int, 38=Patch5 Int, 39=Patch6 Int |
| `t1.pt5i` | T2 Virtual Patch › Int | 1–127 (centro 64) |  |
| `t1.eqLf` | T2 EQ › Low Freq | 0–33 |  |
| `t1.eqLg` | T2 EQ › Low Gain | 34–94 (centro 64) |  |
| `t1.eqHf` | T2 EQ › Hi Freq | 0–25 |  |
| `t1.eqHg` | T2 EQ › Hi Gain | 34–94 (centro 64) |  |
| `vMode` | Program › Voice Mode | 0–3 | 0=Single, 1=Layer, 2=Split, 3=Multi |
| `t2ch` | Program › T2 MIDI Ch | 0–16 | 0=1, 1=2, 2=3, 3=4, 4=5, 5=6, 6=7, 7=8, 8=9, 9=10, 10=11, 11=12, 12=13, 13=14, 14=15, 15=16, 16=Global |
| `octave` | Program › Octave | 5–11 (centro 8) |  |
| `scaleT` | Program › Scale | 0–9 | 0=Equal Temp, 1=Pure Major, 2=Pure Minor, 3=Arabic, 4=Pythagorean, 5=Werckmeister, 6=Kirnberger, 7=Slendro, 8=Pelog, 9=User Scale |
| `scaleK` | Program › Scale Key | 0–11 | 0=C, 1=C#, 2=D, 3=D#, 4=E, 5=F, 6=F#, 7=G, 8=G#, 9=A, 10=A#, 11=B |
| `tempo` | Arpeggiator › Tempo | 20–300 |  |
| `arpOn` | Arpeggiator › Arp On | 0/1 |  |
| `arpKey` | Arpeggiator › Key Sync | 0/1 |  |
| `arpTimb` | Arpeggiator › Timbre | 0–2 | 0=Timbre 1, 1=Timbre 2, 2=Timbre 1+2 |
| `arpType` | Arpeggiator › Type | 0–5 | 0=Up, 1=Down, 2=Alt 1, 3=Alt 2, 4=Random, 5=Trigger |
| `arpRes` | Arpeggiator › Resolution | 0–8 | 0=1/32, 1=1/24, 2=1/16, 3=1/12, 4=1/8, 5=1/6, 6=1/4, 7=1/2, 8=1/1 |
| `arpOct` | Arpeggiator › Octave | 0–3 | 0=1 Oct, 1=2 Oct, 2=3 Oct, 3=4 Oct |
| `arpLast` | Arpeggiator › Last Step | 0–7 | 0=1, 1=2, 2=3, 3=4, 4=5, 5=6, 6=7, 7=8 |
| `arpLatch` | Arpeggiator › Latch | 0/1 |  |
| `arpGate` | Arpeggiator › Gate | 0–100 |  |
| `arpSwing` | Arpeggiator › Swing | 14–114 (centro 64) |  |
| `step0` | Arpeggiator › 1 | 0/1 |  |
| `step1` | Arpeggiator › 2 | 0/1 |  |
| `step2` | Arpeggiator › 3 | 0/1 |  |
| `step3` | Arpeggiator › 4 | 0/1 |  |
| `step4` | Arpeggiator › 5 | 0/1 |  |
| `step5` | Arpeggiator › 6 | 0/1 |  |
| `step6` | Arpeggiator › 7 | 0/1 |  |
| `step7` | Arpeggiator › 8 | 0/1 |  |
| `vcSw` | Vocoder › Vocoder › Vocoder | 0/1 |  |
| `vcSel` | Vocoder › Vocoder › Carrier | 0–1 | 0=Audio In, 1=Timbre 2 |
| `vcGate` | Vocoder › Vocoder › HPF Gate | 0/1 |  |
| `vcGs` | Vocoder › Vocoder › Gate Sens | 0–127 |  |
| `vcThr` | Vocoder › Vocoder › Threshold | 0–127 |  |
| `vcHpf` | Vocoder › Vocoder › HPF Level | 0–127 |  |
| `vcDir` | Vocoder › Livelli › Direct | 0–127 |  |
| `vcT1` | Vocoder › Livelli › Timbre 1 | 0–127 |  |
| `vcT2` | Vocoder › Livelli › Timbre 2 | 0–127 |  |
| `vcLvl` | Vocoder › Livelli › Vocoder | 0–127 |  |
| `vcShift` | Vocoder › Filtro › Formant Shift | 2–6 (centro 4) |  |
| `vcFcSrc` | Vocoder › Filtro › Fc Mod Src | 0–11 | 0=EG1, 1=EG2, 2=EG3, 3=LFO1, 4=LFO2, 5=Velocity, 6=Pitch Bend, 7=Mod Wheel, 8=Key Track, 9=MIDI1, 10=MIDI2, 11=MIDI3 |
| `vcCut` | Vocoder › Filtro › Cutoff Ofs | 1–127 (centro 64) |  |
| `vcRes` | Vocoder › Filtro › Resonance | 0–127 |  |
| `vcFcInt` | Vocoder › Filtro › Fc Mod Int | 1–127 (centro 64) |  |
| `vcEf` | Vocoder › Filtro › E.F. Sens | 0–127 |  |
| `vb0p` | Vocoder · 16 bande › Pan 1 | 0–127 (centro 64) |  |
| `vb0l` | Vocoder · 16 bande › Level 1 | 0–127 |  |
| `vb1p` | Vocoder · 16 bande › Pan 2 | 0–127 (centro 64) |  |
| `vb1l` | Vocoder · 16 bande › Level 2 | 0–127 |  |
| `vb2p` | Vocoder · 16 bande › Pan 3 | 0–127 (centro 64) |  |
| `vb2l` | Vocoder · 16 bande › Level 3 | 0–127 |  |
| `vb3p` | Vocoder · 16 bande › Pan 4 | 0–127 (centro 64) |  |
| `vb3l` | Vocoder · 16 bande › Level 4 | 0–127 |  |
| `vb4p` | Vocoder · 16 bande › Pan 5 | 0–127 (centro 64) |  |
| `vb4l` | Vocoder · 16 bande › Level 5 | 0–127 |  |
| `vb5p` | Vocoder · 16 bande › Pan 6 | 0–127 (centro 64) |  |
| `vb5l` | Vocoder · 16 bande › Level 6 | 0–127 |  |
| `vb6p` | Vocoder · 16 bande › Pan 7 | 0–127 (centro 64) |  |
| `vb6l` | Vocoder · 16 bande › Level 7 | 0–127 |  |
| `vb7p` | Vocoder · 16 bande › Pan 8 | 0–127 (centro 64) |  |
| `vb7l` | Vocoder · 16 bande › Level 8 | 0–127 |  |
| `vb8p` | Vocoder · 16 bande › Pan 9 | 0–127 (centro 64) |  |
| `vb8l` | Vocoder · 16 bande › Level 9 | 0–127 |  |
| `vb9p` | Vocoder · 16 bande › Pan 10 | 0–127 (centro 64) |  |
| `vb9l` | Vocoder · 16 bande › Level 10 | 0–127 |  |
| `vb10p` | Vocoder · 16 bande › Pan 11 | 0–127 (centro 64) |  |
| `vb10l` | Vocoder · 16 bande › Level 11 | 0–127 |  |
| `vb11p` | Vocoder · 16 bande › Pan 12 | 0–127 (centro 64) |  |
| `vb11l` | Vocoder · 16 bande › Level 12 | 0–127 |  |
| `vb12p` | Vocoder · 16 bande › Pan 13 | 0–127 (centro 64) |  |
| `vb12l` | Vocoder · 16 bande › Level 13 | 0–127 |  |
| `vb13p` | Vocoder · 16 bande › Pan 14 | 0–127 (centro 64) |  |
| `vb13l` | Vocoder · 16 bande › Level 14 | 0–127 |  |
| `vb14p` | Vocoder · 16 bande › Pan 15 | 0–127 (centro 64) |  |
| `vb14l` | Vocoder · 16 bande › Level 15 | 0–127 |  |
| `vb15p` | Vocoder · 16 bande › Pan 16 | 0–127 (centro 64) |  |
| `vb15l` | Vocoder · 16 bande › Level 16 | 0–127 |  |
| `fx0type` | Master FX 1 › Type | 0–17 | 0=No Effect, 1=Compressor, 2=Filter, 3=Band EQ, 4=Distortion, 5=Decimator, 6=Delay, 7=L/C/R Delay, 8=Auto Panning Delay, 9=Modulation Delay, 10=Tape Echo, 11=Chorus, 12=Flanger, 13=Vibrato, 14=Phaser, 15=Tremolo, 16=Ring Modulator, 17=Grain Shifter |
| `fx0k1` | Master FX 1 › Ctrl 1 | 0–19 | 0=—, 1=—, 2=—, 3=—, 4=—, 5=—, 6=—, 7=—, 8=—, 9=—, 10=—, 11=—, 12=—, 13=—, 14=—, 15=—, 16=—, 17=—, 18=—, 19=— |
| `fx0k2` | Master FX 1 › Ctrl 2 | 0–19 | 0=—, 1=—, 2=—, 3=—, 4=—, 5=—, 6=—, 7=—, 8=—, 9=—, 10=—, 11=—, 12=—, 13=—, 14=—, 15=—, 16=—, 17=—, 18=—, 19=— |
| `fx1type` | Master FX 2 › Type | 0–17 | 0=No Effect, 1=Compressor, 2=Filter, 3=Band EQ, 4=Distortion, 5=Decimator, 6=Delay, 7=L/C/R Delay, 8=Auto Panning Delay, 9=Modulation Delay, 10=Tape Echo, 11=Chorus, 12=Flanger, 13=Vibrato, 14=Phaser, 15=Tremolo, 16=Ring Modulator, 17=Grain Shifter |
| `fx1k1` | Master FX 2 › Ctrl 1 | 0–19 | 0=—, 1=—, 2=—, 3=—, 4=—, 5=—, 6=—, 7=—, 8=—, 9=—, 10=—, 11=—, 12=—, 13=—, 14=—, 15=—, 16=—, 17=—, 18=—, 19=— |
| `fx1k2` | Master FX 2 › Ctrl 2 | 0–19 | 0=—, 1=—, 2=—, 3=—, 4=—, 5=—, 6=—, 7=—, 8=—, 9=—, 10=—, 11=—, 12=—, 13=—, 14=—, 15=—, 16=—, 17=—, 18=—, 19=— |

## Little Phatty (chiave = cc + numero del CC)

| Chiave | Parametro | Valori | Opzioni |
|---|---|---|---|
| `cc3` | Modulation › LFO Rate | 0–127 |  |
| `cc6` | Modulation › Amount | 0–127 |  |
| `cc68` | Modulation › Source | 0–80 | 0=Tri, 16=Square, 32=Saw, 48=Ramp, 64=Filt Env, 80=Osc 2 |
| `cc69` | Modulation › Destination | 0–48 | 0=Pitch, 16=Filter, 32=Wave, 48=Osc 2 |
| `cc102` | Modulation › LFO › LFO Sync | 0–64 | 0=Internal, 64=MIDI Clock |
| `cc103` | Modulation › LFO › Clock Div | 0–112 | 0=1/32, 8=1/32 ., 16=1/16, 24=1/16 ., 32=1/8, 40=1/8 ., 48=1/4, 56=1/4 ., 64=1/2, 72=1/2 ., 80=1/1, 88=1/1+1/4, 96=1/1+1/2, 104=1/1+1/2 ., 112=2/1 |
| `cc104` | Modulation › Sorgenti extra › Mod Src 5 | 0–64 | 0=Filter Env, 64=S&H |
| `cc105` | Modulation › Sorgenti extra › Mod Src 6 | 0–64 | 0=Osc 2, 64=Noise |
| `cc106` | Modulation › Sorgenti extra › Mod Dest 2 | 0–100 | 0=Off, 25=Pitch, 50=Filter, 75=Wave, 100=Osc 2 |
| `cc74` | Oscillators › Osc 1 › Octave | 0–64 | 0=16', 32=8', 48=4', 64=2' |
| `cc9` | Oscillators › Osc 1 › Wave | 0–127 |  |
| `cc15` | Oscillators › Osc 1 › Level | 0–127 |  |
| `cc75` | Oscillators › Osc 2 › Octave | 0–64 | 0=16', 32=8', 48=4', 64=2' |
| `cc10` | Oscillators › Osc 2 › Freq | 0–127 (centro 64) |  |
| `cc11` | Oscillators › Osc 2 › Wave | 0–127 |  |
| `cc16` | Oscillators › Osc 2 › Level | 0–127 |  |
| `cc77` | Oscillators › Glide · Sync › 1-2 Sync | 0=off, 64=on |  |
| `cc65` | Oscillators › Glide · Sync › Glide | 0=off, 64=on |  |
| `cc5` | Oscillators › Glide · Sync › Glide Rate | 0–127 |  |
| `cc19` | Filter › Cutoff | 0–16383 |  |
| `cc21` | Filter › Resonance | 0–127 |  |
| `cc22` | Filter › KB Amount | 0–127 |  |
| `cc27` | Filter › EG Amount | 0–127 |  |
| `cc18` | Filter › Overload | 0–127 |  |
| `cc109` | Filter › Poles | 0–96 | 0=1, 32=2, 64=3, 96=4 |
| `cc110` | Filter › Vel Sens | 0–117 | 0=-8, 12=-7, 19=-6, 26=-5, 33=-4, 40=-3, 47=-2, 54=-1, 61=0, 68=+1, 75=+2, 82=+3, 89=+4, 96=+5, 103=+6, 110=+7, 117=+8 |
| `cc23` | Envelope Generators › Filter › Attack | 0–127 |  |
| `cc24` | Envelope Generators › Filter › Decay | 0–127 |  |
| `cc25` | Envelope Generators › Filter › Sustain | 0–127 |  |
| `cc26` | Envelope Generators › Filter › Release | 0–127 |  |
| `cc28` | Envelope Generators › Volume › Attack | 0–127 |  |
| `cc29` | Envelope Generators › Volume › Decay | 0–127 |  |
| `cc30` | Envelope Generators › Volume › Sustain | 0–127 |  |
| `cc31` | Envelope Generators › Volume › Release | 0–127 |  |
| `cc111` | Envelope Generators › Retrigger › EGR Release | 0=off, 64=on |  |
| `cc112` | Envelope Generators › Retrigger › Legato | 0–86 | 0=On, 43=Off, 86=Reset |
| `cc7` | Output › Volume | 0–127 |  |
| `cc107` | Output › Tastiera › Bend Up | 0–127 |  |
| `cc108` | Output › Tastiera › Bend Down | 0–127 |  |
| `cc88` | Output › Tastiera › Key Priority | 0–96 | 0=Global, 32=Low, 64=High, 96=Last |
| `cc113` | Arpeggiator › Arp On | 0=off, 64=on |  |
| `cc90` | Arpeggiator › Run | 0=off, 64=on |  |
| `cc119` | Arpeggiator › Latch On | 0=off, 64=on |  |
| `cc91` | Arpeggiator › Latch | 0=off, 64=on |  |
| `cc4` | Arpeggiator › Tempo | 300–3000 |  |
| `cc114` | Arpeggiator › Clock Src | 0–86 | 0=Internal, 43=LFO, 86=MIDI |
| `cc115` | Arpeggiator › Clock Div | 0–112 | 0=1/32, 8=1/32 ., 16=1/16, 24=1/16 ., 32=1/8, 40=1/8 ., 48=1/4, 56=1/4 ., 64=1/2, 72=1/2 ., 80=1/1, 88=1/1+1/4, 96=1/1+1/2, 104=1/1+1/2 ., 112=2/1 |
| `cc116` | Arpeggiator › Range | 0–109 | 0=-3, 19=-2, 38=-1, 57=0, 71=+1, 90=+2, 109=+3 |
| `cc117` | Arpeggiator › Pattern | 0–86 | 0=Up, 43=Down, 86=Order |
| `cc118` | Arpeggiator › Mode | 0–86 | 0=Loop, 43=Back/Forth, 86=Once |

Little Phatty: `cc19` (Cutoff) va da 0 a 16383 e viene inviato come CC19 + CC51; `cc4` (Tempo) è in decimi di BPM e viene inviato come CC4 + CC36.

### microKORG XL: parametri degli effetti

`fx0p0`…`fx0p19` (Master FX 1) e `fx1p0`…`fx1p19` (Master FX 2): il significato dipende da `fx0type`/`fx1type` e segue l'ordine della «EFFECT PARAMETER STRUCTURE» in `docs/microKORG_XL_MIDIimp.txt` (fx0p0 = primo parametro, di solito Dry/Wet 0–100).
