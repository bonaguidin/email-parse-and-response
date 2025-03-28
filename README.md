# YMCA Email Generator (re-worked to include non-YMCA related emails).

Parse user interest forms and generate personalized responses using the SambaNova API.

## Project Description

This project automates the generation of email responses to user interest forms submitted to the YMCA. It parses the form data, extracts relevant information like name, interests, and tour requests, and uses the SambaNova API to generate customized email replies. The system is designed to streamline communication with potential YMCA members, providing timely and relevant information.

## Features

* **Automated Email Response Generation:** Automatically creates personalized email responses.
* **Flexible Data Parsing:** Extracts user information from various email formats.
* **SambaNova API Integration:** Leverages the power of large language models for natural language response generation.
* **Template-Based Responses:** Utilizes predefined templates for different response types (tour requests, membership inquiries).
* **Program Information Integration:** Incorporates details about YMCA programs based on user interests.
* **Web-Based Interface:** Provides a user-friendly web interface using Gradio for easy interaction.
* **Fuzzy Matching:** Uses fuzzy matching to handle variations in user input.
* **Dynamic Prompt Construction:** Creates dynamic prompts for the LLM based on user data and program details.

## Technologies Used

* **Python:** The core programming language.
* **OpenAI (SambaNova API):** For generating natural language responses.
* **Gradio:** For creating the web-based user interface.
* **FuzzyWuzzy:** For fuzzy string matching.
* **IPywidgets:** For initial interactive UI elements (now replaced by Gradio).
* **Regular Expressions (re):** For pattern matching and text extraction.
* **Google Colab:** For development and hosting.

## Setup and Installation

1.  **Clone the Repository (Optional):**
    ```bash
    git clone (https://github.com/bonaguidin/email-parse-and-response)
    ```
2.  **Install Required Packages:**
    ```bash
    pip install openai ipywidgets streamlit pyngrok fuzzywuzzy ipython gradio
    ```
3.  **Set Up API Key:**
    * Replace `"API_KEY"` in the `client = openai.OpenAI(...)` initialization with your SambaNova API key. **(Important: Store your API key securely using environment variables or a configuration file.)**
4.  **Run the Colab Notebook:**
    * Open the Colab notebook (`.ipynb` file) in Google Colab.
    * Run the single cell to execute the code.
5.  **Access the Gradio Interface:**
    * The Gradio interface will generate a public URL. Click on the URL (blue link) to access the web application.
    * The Gradio web application **will only run for as long as the Colab notebook is running or up to 72 hours**, whichever comes first. 

## Usage

1.  **Input Email:**
    * Paste the user's interest form email into the input textbox.
2.  **Select Template:**
    * Choose the appropriate response template from the dropdown menu (Auto Select, Tour Response, Membership Response).
3.  **Generate Response:**
    * The generated email response will appear in the output textbox.
4.  **Copy or Send:**
    * Copy the generated response and send it to the user.

## Code Structure

* **`parse_structured_email(email_text)`:** Parses the user's email to extract relevant information.
* **`generate_response(email_text, template_choice)`:** Generates the email response using the SambaNova API.
* **`generate_response_gradio(email_text, template_choice)`:** Gradio function to integrate the functionality into a web interface.
* **`PAST_TEMPLATES`:** Dictionary containing response templates.
* **`PROGRAM_DETAILS`:** Dictionary containing information about YMCA programs.

## Contributing

Contributions are welcome! If you'd like to contribute:

1.  Fork the repository.
2.  Create a new branch for your feature or bug fix.
3.  Commit your changes.
4.  Push to your branch.
5.  Submit a pull request.

## Future Enhancements

* **Database Integration:** Store user data and program information in a database for better management.
* **Advanced Program Matching:** Improve the logic for matching user interests with relevant programs.
* **Email Sending Functionality:** Integrate email sending capabilities directly into the application.
* **Improved UI/UX:** Enhance the Gradio interface with more features and a better design.
* **Error Handling:** Implement more robust error handling and logging.
* **Authentication:** Add user authentication for secure access.
* **Deployment:** Deploy the application to a cloud platform for production use.
* **Testing:** Add unit tests to ensure code quality.

## License

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the “Software”), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED “AS IS”, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

## Contact

### Noah Bonaguidi
### bonaguidin@gmail.com
