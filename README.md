# Captchas-Prediction


In this project the 5 character text captcha was given with large number of test data. I have trained the model with 6 epochs and 90k data. Eventually got more than 90% of the accuracy.  I have used the same optimizer as Adam; it determines learning rates for various variables. It uses gradient descent to change the learning rates (alpha). 
I have used generate.py, to generate the various 5 characters text captcha and hence used Evaluator.py to calculate the accuracy on the validation set. 

Captcha:
python Evaluvator.py --captcha-length 8  --predicted-output stuff.txt

Training :
python train.py --width 128 --height 64 --length 5 --symbols symbols.txt --batch-size 4 --epochs 2 --output-model test.h5 --train-dataset training_data --validate-dataset validation_data

Output in stuff:
python classify.py --model-name test --captcha-dir example_captchas --output stuff.txt --symbols symbols.txt

genearating captchas:
python generate.py --width 128 --height 64 --length 5 --symbols symbols.txt --count 10 --output-dir test1
