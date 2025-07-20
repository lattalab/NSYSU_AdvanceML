## Final project

### Dataset: TomatoD
reference:
1. [website](https://datasetninja.com/tomatod)
2. [github](https://github.com/up2metric/tomatOD)

### project proposal
Original goal: use `DETR` model to do a object detection task.

### Difficulty
However, DETR need higher hardware resources. In my experience, running on CPU will cost 30 minutes in `1 epoch`.  
Although, GPU can run faster, but DETR need a lot of epochs to convergence.

I have tried `Colab`, but is Easy to reach free limits.

OK, Since I have `NVIDIA GeForce GTX 1650 GPU`, but it also hard to train.
Reason:  
1. DETR is a large model
2. hard to train due to `transformer-mechanism`, `object-queries` (those innovative concept)
3. Rely on large data
4. Bad at small object   
(Unfortunately, I have chosen dataset that are mainly `small object`.)

Conclusion: My DETR experience are pretty bad.

### YOLO Testing
After training YOLOv10, there are a lot of advantages rather than DETR.  
(It may due to my training skill.)

1. Accuracy are more precisely.
2. mAP has been improved significantly.
3. YOLOv10 can detect small objects.
4. It can predict true bbox(es) in the image. (Althought there are many bboxes are not.)

| 比較項目       | DETR                            | YOLO                 |
| ---------- | ------------------------------- | -------------------- |
| 訓練資料需求     | 多（大型資料集效果較佳）                    | 少（小資料集就能出效果）         |
| 模型收斂速度     | 慢                               | 快                    |
| bbox 預測精準度 | 中等，依靠 transformer 的 global info | 很精準（尤其 anchor-based） |
| 上手門檻       | 較高                              | 非常低，有大量範例和訓練框架       |
| 評估工具       | 需額外處理 post-processing           | 多數框架內建整合             |
| 適合場景       | 複雜物件、需 end-to-end 的             | 大部分工業應用、輕量場景         |
