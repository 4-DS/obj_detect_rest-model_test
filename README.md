# Step CV-Pipeline: model_test

At this stage, CV Pipeline Model_Test tests the packaged BentoML service, which contains the model and other necessary artifacts.
May contain several tests and examples of calling BentoML REST API methods:
1. Launch test of packaged bentoservice and test image predictor
     - Launching the BentoML service (obtained from the Model_Pack component) to process images and obtain predictors
     - Obtaining a test image and the saved result of processing the test image (must be in the bentoservice artifacts) through the REST API methods of the BentoML service
       The previously saved processing result on the test image is used as a reference value.
     - Prediction of a test image via the REST API of the BentoML service
     - Comparison of the test image predictor with the saved test result. May involve comparing values or other characteristics of a predictor with reference values.

2. Load test, when for a specified time there is a sequential call to the REST API predict method on a test image.
    This test allows you to evaluate the performance of the BentoML model and service when processing a large number of requests.
    
    