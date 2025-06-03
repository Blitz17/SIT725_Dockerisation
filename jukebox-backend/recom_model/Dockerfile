# Use Python base image
FROM python:3.11.5

RUN pip install flask pandas scikit-learn pymongo
RUN pip install flask pandas scikit-learn flask-cors
# Set working directory inside container
WORKDIR /app

# Copy the Flask app code
COPY . .

# Expose Flask port
EXPOSE 5000

# Run the app
CMD ["python", "app.py"]