# Use Python runtime (from parent Python image):
    FROM python:3.9

    # Set working directory:
    
    WORKDIR /app
    
    # Copy current directory contents into the container at WORKDIR:
    ADD ./src_data /app
    
    # Install any needed packages specified in requirements.txt:
    
    RUN pip3 install -r requirements.txt
    
    # Output from python script app.py
    
    EXPOSE 5000
    # Run app.py when the container launches
    
    CMD ["python", "app.py"]
    
    