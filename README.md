# EVA4_S5
Understanding code structuring and when and where to apply various regularization techniques in Pytorch

Step 1 :
Target - Getting executable skeleton, not worried about parameters and final accuracy
Result - Best accuracy : 99.52%(train) 99.11%(test) ; Params : 194,884
Analysis - Able execute the code and see results but accuracy is not consistent across the epochs which is expected

Step 2 :
Target - Add batch normalization to previous code and reduce the number of parameters and see if using batch normalization reduces gap between train and test accuracy
Result - Best accuracy : 99.9%(train) 99.26%(test) ; Params : 10,970
Analysis - Improvement in both train and validation accuracy but model tends to overfit and needs more regularization to reduce train and test accuracy. Final few epochs are consistently above 99.2%

Step 3 :
Target - Along with batch normalization add dropout(0.05) IN ALL LAYERS EXCEPT LAST LAYER and see if using batch normalization along with dropout reduces gap between train and test accuracy
Result - Best accuracy : 99.44%(train) 99.36%(test) ; Params : 10,970
Analysis - No overfit in the model and train-test gap is reduced. Final few epochs are above 99.3% consistently and the model can be trained better to improve test accuracy

Step 4 :
Target - Along with batch normalization add dropout(0.05) IN ALL LAYERS EXCEPT LAST LAYER and add image augmentation with slight rotation of 5 degrees and see if using batch normalization with dropout and image augmentation further reduces gap between train and test accuracy. Global Average Pooling is NOT introduced yet.
Result - Best accuracy : 99.64%(train) 99.40%(test) ; Params : 19,408
Analysis - Slight overfit in the model and train-test gap is increased. Final few epochs are above 99.35% consistently

Step 5 :
Target - Along with batch normalization dropout(0.05) is added IN ALL LAYERS EXCEPT LAST LAYER and image augmentation is used. Global Average Pooling is introduced and expecting to hit 99.4% consistently.
Result - Best accuracy : 99.06%(train) 99.46%(test) ; Params : 8,936
Analysis - No overfit in the model is observed. Train accuracy is less than test accuracy complementing the use of regularization and augmentation strategies. Final few epochs are above 99.4% consistently.
