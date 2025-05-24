# python..........
def read_and_modify_file():
    try:
        filename = input("Enter the filename to read: ")
        
        # Try to open and read the file
        with open(filename, 'r') as file:
            content = file.read()
        
        # Modify the content (example: convert to uppercase)
        modified_content = content.upper()
        
        # Create output filename (e.g., prefix "modified_")
        output_filename = "modified_" + filename
        
        # Write the modified content to new file
        with open(output_filename, 'w') as file:
            file.write(modified_content)
        
        print(f"Modified content written to '{output_filename}'.")
    
    except FileNotFoundError:
        print(f"Error: The file '{filename}' does not exist.")
    except IOError:
        print(f"Error: Could not read/write file '{filename}'.")

if __name__ == "__main__":
    read_and_modify_file()
