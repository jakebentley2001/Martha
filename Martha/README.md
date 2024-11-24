After doing some research I have found several interesting items to think about

Datasets:
    - Food 101 
    - Roboflow Food Ingredients dataset: 4,196 images 120 ingredient classes: https://universe.roboflow.com/food-recipe-ingredient-images-0gnku/food-ingredients-dataset/dataset/4
    - I think this is food segmentation data https://huggingface.co/datasets/EduardoPacheco/FoodSeg103


Systems
    We probably want to go with a system that does the segmentations in which it finds items that could be food. Then implemenet another model that takes the images that were in the bounding box and classifies them. This paper talks about how this could be a good approach: https://arxiv.org/pdf/1604.07953
    - Classification
        - Aparently ResNet architeture is good. This is a 2023 literature review on the best performing model structures on food datasets. https://www.mecs-press.org/ijeme/ijeme-v14-n2/IJEME-V14-N2-5.pdf. This is an example github of someone training a ResNet 50 model on the food 101 dataset https://github.com/Pyligent/food101-image-classification/blob/master/README.md
        - We can also look at DenseNet which I think is similair to ResNet. This is a github describig the finetuning of a DesNet-161 model on the Food 101 dataset. https://github.com/Prakhar998/Food-Classification
        - Clip also looks slightly promising but not really. Here is an article describing its performance https://www.labellerr.com/blog/performance-of-clip-over-food-classification-dataset-here-are-the-findings/

        - Segmentations