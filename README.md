# Car-Damage-Severity-Detection

A full-fledged deep learning application that can identify car damages.

For image categorization, we employed a three-layer network, and we even trained mask rcnn to identify scratch and dent. 
We've deployed our model in AWS EC2 and built a user-friendly angular-based UI that allows users to quickly obtain car damage statistics. 

Once the picture is uploaded in UI, it will be sent to the model through an API gateway and lambda function, which will store it in an S3 bucket then the flask server running on ecs will retrieve image from S3 bucket and process the image. 
The processed image will be displayed in our frontend UI. 
By measuring the precise damage length of the car, we will be able to determine which portion of the car is damaged and how serious the damage will be.
