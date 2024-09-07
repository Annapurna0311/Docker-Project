# Use a base image with C++ tools installed
FROM gcc:latest

# Set the working directory inside the container
WORKDIR /myapp

# Copy the source file to the working directory
COPY ./myapp.cpp .

# Compile the C++ program
RUN g++ -o myapp myapp.cpp

# Define the command to run the compiled program
CMD ["./myapp"]
