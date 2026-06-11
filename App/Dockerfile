FROM python:3.10-slim

# Set the working directory
WORKDIR /app

#RUN ls /app

# Copy requirements.txt
COPY Demo-Streamlit-App/requirements.txt requirements.txt

# Install Streamlit
RUN pip install -r requirements.txt

# Copy the app files to the container
COPY Demo-Streamlit-App/app.py .

# Expose the Streamlit default port
EXPOSE 8501

# Run the Streamlit app
CMD ["streamlit", "run", "/app/app.py", "--server.port=8501", "--server.address=0.0.0.0", "--server.enableCORS=false"]
