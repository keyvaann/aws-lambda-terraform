FROM public.ecr.aws/lambda/python:3.10

# Copy requirements.txt
COPY requirements.txt ./

# Install the specified packages
RUN python3.10 -m pip install -r requirements.txt -t .

# Copy function code
COPY app.py ./

# Set the CMD to your handler (could also be done as a parameter override outside of the Dockerfile)
CMD [ "app.lambda_handler" ]
