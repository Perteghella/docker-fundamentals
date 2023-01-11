# Base image
FROM python:3.12.0a4-alpine
# Set working directory for subsequent commands
WORKDIR /code
ENV FLASK_APP=app.py
ENV FLASK_RUN_HOST=0.0.0.0
RUN apk add --no-cache gcc musl-dev linux-headers
# Install dependencies
COPY requirements.txt requirements.txt
RUN pip install -r requirements.txt
EXPOSE 5000
# Add app code to /code inside container image
COPY . .
# Command to run when container starts
CMD ["flask", "run"]
