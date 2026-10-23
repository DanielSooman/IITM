## Transcription and classification

All questions are **1 mark**. No negative marking is shown. Questions 1, 2, and 10 accept numeric input; Questions 3–9 are single-answer MCQs.

### Q1–Q2 common diagram
Diagram flow:

- Main branch:  
  \(x \rightarrow\) weight layer \((w_1=2)\rightarrow\text{ReLU}\rightarrow\) weight layer \((w_2=3)\), labelled \(F(x)\).
- Skip branch: \(x\) goes by an **identity** connection into an addition node with \(F(x)\).
- The diagram visibly shows a **ReLU after the addition node**, while the bottom annotation says \(F(x)+x\).

**Q1.** “If the input to the network is \(x=-1\) then what will be the output of the network before skip connection? There are no bias attached to the network.”

**Q2.** “With the same input (i.e. \(x=-1\)), what will be the output after skip connection?”

> Important ambiguity: “after skip connection” may mean the value immediately after addition, \(F(x)+x\), or the final block output after the ReLU visibly drawn after addition.

### Q3
“In a semantic segmentation model, what is the typical role of the ‘decoder’?”

A. Gradually up-sample the low-resolution feature maps to produce a full-resolution segmentation map.  
B. Apply data augmentation to input images before they enter the network.  
C. Extract high-level semantic features from the input image.  
D. Calculate the final loss function and update the model’s weights.

### Q4
```python
model = torchvision.models.efficientnet_b0(weights='DEFAULT')
for p in model.parameters():
    p.requires_grad = False

model.classifier[1] = torch.nn.Linear(1280, 3)
optimizer = torch.optim.Adam(model.parameters(), lr=3e-3)
```

“When `optimizer.step()` is called during training, which parameters will be updated?”

A. None, because the first loop set `requires_grad = False` on all original parameters.  
B. Only the weights and bias of the new `torch.nn.Linear(1280, 3)` layer.  
C. All parameters in `model.classifier`, including the Dropout layer.  
D. All model parameters, because the optimizer was instantiated with `model.parameters()`.

### Q5
“Which transformation is wrong for the test dataset? Assume:
```python
import albumentations as A
```”

A. `Resize(512,512)`  
B. `Normalize(mean=(0,0,0), std=(1,1,1))`  
C. `Rotate(p=0.1)`  
D. `ToTensorV2()`

### Q6
“What is the expected directory format for using `datasets.ImageFolder`?”

A. `train/class_instances`  
B. `all_classes/train/instances`  
C. `train/<class_name>/<images>`  
D. `images/train/class_name`

### Q7
```python
import torchvision.transforms as transforms

def transform_data():
    train_transform = transforms.Compose([
        transforms.Resize((100,100)),
        transforms.RandomHorizontalFlip(p=0.1),
        transforms.RandomRotation(degrees=5),
        transforms.ColorJitter(
            brightness=0.2,
            saturation=0.2
        ),
        transforms.Normalize(mean=image_mean, std=image_std),
        transforms.ToTensor()
    ])
    return train_transform
```

“For a PIL input image transformation… What is wrong with the above code?”

A. `transforms.Resize` must always come after `ToTensor()`  
B. `transforms.RandomRotation` cannot be combined with `transforms.ColorJitter`.  
C. Nothing is wrong; the code will work fine as it is.  
D. `transforms.Normalize` is applied before `ToTensor()`.

### Q8
“The outputs of the parallel branches in a GoogLeNet Inception module are combined by:”

A. Element-wise addition of all feature maps.  
B. Concatenation of the feature maps along the channel dimension.  
C. A \(1\times1\) convolution that merges all feature maps.  
D. A global average pooling operation.

### Q9
```python
import torch.nn as nn
import torch

# A block that halves spatial dimensions and doubles channels
block = nn.Sequential(
    nn.Conv2d(64, 128, kernel_size=3, stride=2, padding=1), nn.ReLU(),
    nn.Conv2d(128, 128, kernel_size=3, padding=1), nn.ReLU()
)

x = torch.randn(8, 64, 56, 56)
output = block(x) + x
```

“What is the result of executing this code?”

A. It executes successfully, as PyTorch broadcasts `x` to match `block(x)`.  
B. It fails because spatial dimensions \(56\times56\) and \(28\times28\) are incompatible.  
C. It fails because channel dimensions 64 and 128 are incompatible.  
D. It fails because both spatial and channel dimensions are incompatible for element-wise addition.

### Q10
```python
import torch
import torch.nn as nn
import torchvision.models as models

model = models.vgg16(pretrained=True)

# Freeze feature extractor
for param in model.parameters():
    param.requires_grad = False

# Adding a linear layer for fine tuning (including bias)
model.classifier[6] = nn.Linear(4096, 5, bias=False)

# Count trainable parameters
trainable_params = sum(p.numel() for p in model.parameters() if p.requires_grad)
print(trainable_params)
```

“What is the output of the final print statement?”

> The comment says “including bias,” but the actual code explicitly has `bias=False`; the code controls the answer.

---

## Answers and reasoning

### Q1 — **0**
\[
F(x)=w_2\operatorname{ReLU}(w_1x)
\]
\[
w_1x=2(-1)=-2,\qquad \operatorname{ReLU}(-2)=0
\]
\[
F(x)=3(0)=0
\]

**Final answer: `0`**

---

### Q2 — **ambiguous as written**
The residual-addition value is:
\[
F(x)+x=0+(-1)=-1
\]

- **Immediately after the skip/addition node:** \(\boxed{-1}\)
- **After the final ReLU shown in the diagram:**  
  \[
  \operatorname{ReLU}(-1)=\boxed{0}
  \]

Because the question says “after skip connection” and the diagram labels the sum as \(F(x)+x\), the likely intended numeric answer is **`-1`**. But if the quiz defines the output as the entire shown block including the post-addition ReLU, its expected answer would be **`0`**.

**Recommended entry: `-1`, but double-check your course convention for the final ReLU.**

---

### Q3 — **A**
A decoder restores spatial resolution, usually by up-sampling/deconvolution, to form a pixel-level segmentation map.

- **A:** Correct — this is the decoder’s role.
- **B:** Data augmentation is preprocessing, not decoding.
- **C:** High-level semantic feature extraction is mainly the encoder’s role.
- **D:** Loss calculation/weight updates belong to training, not the decoder.

---

### Q4 — **B**
The loop freezes all parameters that existed at that time. The replacement `nn.Linear(1280, 3)` is created **after** the freezing loop, and new `nn.Linear` parameters default to `requires_grad=True`.

- **A:** False — the newly inserted linear layer is not frozen.
- **B:** Correct — its weight and bias are trainable and updated.
- **C:** False — Dropout has no trainable weights/biases.
- **D:** False — frozen parameters may be in the optimizer, but they have no gradients and are not updated.

---

### Q5 — **C**
`Rotate(p=0.1)` randomly changes some test images. Random augmentation is ordinarily used for training, not standard test preprocessing.

- **A:** Valid deterministic resizing.
- **B:** Valid normalization; these particular values are effectively an identity normalization.
- **C:** Correct — random rotation is inappropriate for ordinary testing.
- **D:** Standard conversion step for model input.

---

### Q6 — **C**
`ImageFolder` expects a root containing one directory per class, with that class’s images inside it. If `train` is the supplied root:

```text
train/
  class_1/
    image1.jpg
  class_2/
    image2.jpg
```

- **A:** Does not clearly provide one folder per class.
- **B:** Places the class structure in the wrong order.
- **C:** Correct conventional layout.
- **D:** Not the stated conventional split-root layout.

Small API nuance: `images/train/class_name` could work if the passed root were specifically `images/train` and image files were inside each class folder. But the intended MCQ answer is clearly **C**.

---

### Q7 — **D**
`Normalize` requires a tensor image, but at that point the input is still a PIL image. `ToTensor()` must precede `Normalize`.

Correct ordering:
```python
transforms.ToTensor(),
transforms.Normalize(mean=image_mean, std=image_std)
```

- **A:** False — `Resize` can operate on PIL images and commonly comes first.
- **B:** False — rotation and color jitter can be combined.
- **C:** False — this transform order raises an error for PIL input.
- **D:** Correct.

---

### Q8 — **B**
Inception branches produce feature maps with matching height and width, then combine them by concatenating channels.

- **A:** Addition is characteristic of residual connections, not Inception’s branch merge.
- **B:** Correct — concatenate along channel dimension.
- **C:** \(1\times1\) convolutions occur within branches, but do not perform the standard final merge.
- **D:** Global average pooling is not how parallel branches are combined.

---

### Q9 — **D**
First convolution changes the tensor shape from:

\[
x:[8,64,56,56]
\]

to:

\[
block(x):[8,128,28,28]
\]

The stride-2 convolution halves spatial dimensions and increases channels from 64 to 128. Therefore the addition attempts:

\[
[8,128,28,28]+[8,64,56,56]
\]

Both channels and spatial dimensions differ; neither mismatch is broadcastable.

- **A:** False — PyTorch cannot broadcast 64 to 128 or 56 to 28.
- **B:** Incomplete — spatial dimensions are incompatible, but channels are too.
- **C:** Incomplete — channels are incompatible, but spatial dimensions are too.
- **D:** Correct.

---

### Q10 — **20480**
All original VGG16 parameters are frozen. The newly inserted layer is trainable by default:

```python
nn.Linear(4096, 5, bias=False)
```

Its weight tensor has:

\[
5 \times 4096 = 20480
\]

parameters. `bias=False` adds no five-element bias vector.

**Final answer: `20480`**

If the code had instead said `bias=True`, the answer would have been \(20480+5=20485\), but the literal code says `bias=False`.

---

## Final answer key

| Question | Answer |
|---|---|
| 1 | `0` |
| 2 | `-1` at residual addition; `0` if post-addition ReLU is included |
| 3 | A |
| 4 | B |
| 5 | C |
| 6 | C |
| 7 | D |
| 8 | B |
| 9 | D |
| 10 | `20480` |

I re-derived the forward pass, tensor shapes, parameter flags, and parameter count separately, then checked the MCQs by eliminating every competing option. The adversarial review found the genuine Q2 ReLU ambiguity and the misleading Q10 bias comment.

**Confidence: Medium.** Verified through three separate single-context reasoning/recheck passes and manual substitution/shape/count checks; no code-execution tool or independent subagent was available.
