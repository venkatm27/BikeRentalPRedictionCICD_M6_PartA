# Step 1: Start with a base Python image
FROM python:3.10-slim

# Step 2: Set the working directory in the container
WORKDIR /app

# Step 3: Copy the entire app directory to the working directory in the container
COPY app /app/
# Step 4: Copy the requirements.txt and .whl file into the container
COPY requirements.txt /app/
COPY bikeshare_model-0.0.1-py3-none-any.whl /app/

# Step 5: Install dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Step 6: Expose the port (if necessary for your app)
EXPOSE 8001

# Step 7: Define the command to run your app
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8001"]