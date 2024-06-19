# BOB-YOLO
When it comes to object detection tasks, YOLO stands out for its impressive speed and efficiency. Nonetheless, deploying YOLO on resource-constrained devices remains a challenge due to its substantial model size and memory requirements. The direct application of conventional binary quantization strategies to YOLO can result in significant accuracy degradation. A prevalent solution is to introduce floating-point shortcuts. However, the increased computational demand and parameter complexity associated with these shortcuts limit their practical deployment on hardware platforms for optimal acceleration. To solve this problem, **we propose a binary neural network (BNN) for object detection called BOB-YOLO to achieve a balanced performance in terms of computational speed, model size, and detection accuracy.** Our BOB-YOLO fully leverages module-wise latency (MWL) to supervise the latency of floating-point shortcut branches by that of 1-bit trunk branches. This supervision maximizes the information carried by the floating-point data flow in shortcuts while maintaining latency within the limits set by the 1-bit convolution branch, thereby improving parallel computational efficiency. We also introduce the Roofline Model to address these limitations by considering both computational complexity and parameter compression, ensuring high computational intensity. Additionally, we propose a performance evaluation metric $P_d$, which provides an intuitive description of the trade-off between speed and accuracy, aligning closely with the practical requirements of binary quantization strategies. Extensive experiments on the VOC and COCO datasets demonstrate the significant advantages of our method over state-of-the-art BNN methods.

![YOLOl_COCO](/experimental-results/YOLOl_COCO.jpg)

> [!NOTE]
>
> The code and documentation for the entire project are still being finalized. Currently, only the implementation of some methods and the experimental results are provided.
