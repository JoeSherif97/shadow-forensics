# Solution – GDGCO

## Step 1: Inspect File
Run:
strings GDGFA.jpg

or:
binwalk GDGFA.jpg

Observation:
Presence of appended archive data.

---

## Step 2: Extract Embedded Data
Use:
binwalk --dd='.*' GDGFA.jpg

or:
7z x GDGFA.jpg

---

## Step 3: Analyze Extracted Files
A folder "flags" contains:
G.txt, D.docx, G.pptx, F.pdf, A.png

Each contains Base64-encoded text.

---

## Step 4: Decode Fragments
Example:
base64 -d G.txt

Repeat for all files.

---

## Step 5: Reconstruct Flag
Combine decoded outputs:

GDG{Puzzle_R3Ally_Har5_R19ht}

---

## Key Learning
Hidden data can exist beyond visible file structures, requiring layered analysis techniques.
