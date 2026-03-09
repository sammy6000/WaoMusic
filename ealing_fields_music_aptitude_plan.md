
# Ealing Fields Music Aptitude Test – Key Facts & App Design Strategy

## Source
Ealing Fields High School  
"Specialist Music Place Admissions Criteria 2027–2028"

This document defines how the **specialist music aptitude places (16 places)** are allocated for Year 7.

The test must measure **musical aptitude, not prior musical training**, as required by the UK School Admissions Code.

---

# Admissions Structure

## Number of Places
- 16 music aptitude places per year
- Allocated **independently of distance-based admissions**

Applicants are ranked **purely by aptitude score**.

Tie-breaker:  
- distance to school

---

# Test Structure

## Round 1 – Listening Test

Duration:
- ~1 hour

Score:
- **60 marks**

Format:
- unseen listening exam
- multiple short listening questions

Skills assessed:

- pitch discrimination
- rhythm discrimination
- chord discrimination
- melody recognition

These correspond to **aural perception and auditory memory** skills.

### Typical Task Types

**Pitch discrimination**
Tone A vs Tone B → same or different

**Rhythm comparison**
Rhythm pattern A vs B → same or different

**Melody memory**
Listen to melody → identify matching melody

**Chord discrimination**
Chord A vs B → same or different

---

## Round 2 – Practical Assessment

Only top candidates from Round 1 progress.

Duration:
- ~20 minutes

Score:
- **40 marks**

Tasks include:

- clap back rhythms
- reproduce pitches vocally
- identify instruments from recordings

This evaluates:

| Skill | Cognitive Ability |
|------|------|
| Rhythm imitation | temporal memory + motor timing |
| Pitch reproduction | tonal memory + vocal control |
| Instrument recognition | timbre perception |

---

# Legal Constraint

Admissions law requires tests to measure **aptitude rather than learned musical ability**.

The assessment therefore cannot reward:

- instrument grades
- music theory knowledge
- formal training

The tasks must be solvable by students with **no musical background**.

---

# Instrument Identification Design

The instrument recognition task relies on **clear timbral differences**, not specialist orchestral knowledge.

Expected difficulty examples:

- violin vs trumpet
- piano vs guitar
- flute vs drum

Unlikely examples:

- viola vs violin
- glockenspiel vs xylophone
- oboe vs cor anglais

---

# Dataset Strategy

Use **real acoustic instrument recordings**, not MIDI.

Recommended source:

Philharmonia Orchestra Sound Sample Library  
https://philharmonia.co.uk/resources/sound-samples/

Advantages:
- isolated recordings
- professional orchestral instruments
- consistent audio quality

---

# Recommended Instrument Set

## Strings
- violin
- cello

## Woodwind
- flute
- clarinet

## Brass
- trumpet
- trombone

## Percussion
- snare drum
- xylophone

## Other
- piano
- acoustic guitar

Total ≈ 10 instruments.

---

# Audio Sample Processing

Use:
- single sustained notes
- 0.7–1.5 second clips
- normalized audio levels

Avoid:
- scales
- musical phrases
- crescendos

---

# Dataset Structure

samples/
  violin/
    violin_1.wav
    violin_2.wav
  flute/
    flute_1.wav
    flute_2.wav

Use 5–8 clips per instrument.

Total dataset ≈ 50 samples.

---

# Training Progression

## Level 1 – Instrument Families
string / woodwind / brass / percussion

## Level 2 – Within Family
violin vs cello  
flute vs clarinet  
trumpet vs trombone

## Level 3 – Instrument Identification
Which instrument is playing?

## Level 4 – Same/Different Instrument
Clip A vs Clip B

---

# Additional Training Targets

Most difficult Round 2 skills:

1. rhythm imitation
2. pitch reproduction

Training modules should include:

- pitch discrimination
- rhythm memory
- melody memory
- rhythm reproduction
- pitch reproduction
- timbre recognition

---

# Recommended App Modules

1 Pitch perception  
2 Rhythm perception  
3 Melody memory  
4 Rhythm imitation  
5 Pitch reproduction  
6 Instrument recognition  

---

# Key Insight

Round 1 (aural listening test) is where **most marks are gained or lost**.

The training system should therefore prioritise:

- auditory discrimination
- rhythm perception
- auditory working memory
