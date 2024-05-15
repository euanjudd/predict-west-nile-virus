predict-west-nile-virus

We aim to save the city money while ensuring that the majority of virus-carrying mosquitoes are caught, the strategy should focus on maximizing recall to avoid missing infected mosquitoes and maintaining a reasonable level of precision to avoid unnecessary and costly testing. Fine-tuning the model's threshold based on a careful evaluation of recall and precision can help achieve this balance. The ultimate aim is to make informed, cost-effective decisions that protect public health without incurring undue expenses.

- High precision means that when the model predicts a mosquito specimen is infected, it is likely to be correct. This is important economically because each test conducted incurs costs. Low precision would mean spending resources on testing many mosquitoes that are not actually carrying the virus.

- High recall means that the model is effectively identifying a large proportion of the actual positive cases (infected mosquitoes). This is crucial for public health because failing to detect an infected mosquito could lead to undetected spread of the virus.

Goal: 
- Maximize recall to ensure that most, if not all, mosquitoes carrying the virus are detected and appropriate measures can be taken.
- Maximize precision to ensure that the city does not waste money testing a large number of uninfected specimens, thereby optimizing the use of limited resources.

ROC AUC (Receiver Operating Characteristic Area Under the Curve)
ROC curve plots the True Positive Rate (Recall) against the False Positive Rate at different threshold levels. AUC represents the degree to which the model is capable of distinguishing between the classes (in this case, whether mosquitoes are infected with the West Nile Virus or not). A high ROC AUC score means that the model has a high degree of separability. That is, it can effectively distinguish between infected and non-infected mosquitoes across a range of decision thresholds.

A high ROC AUC score suggests that the model can reliably identify infected mosquitoes (high recall) while keeping the number of false positives low (high precision) across various thresholds. This ability to distinguish between classes means that public health officials can set a threshold that maximizes the detection of infected mosquitoes while minimizing unnecessary tests on uninfected ones. Conversely, a low ROC AUC could lead to many uninfected mosquitoes being falsely identified as infected (low precision), resulting in wasted resources, or many infected mosquitoes being missed (low recall), posing a risk to public health. Choosing a Threshold allows the city to visually assess the trade-off between catching as many infected mosquitoes as possible (high recall) and not testing too many uninfected ones (high precision). They can select a threshold that achieves an acceptable balance according to the city’s public health policies and budget constraints.