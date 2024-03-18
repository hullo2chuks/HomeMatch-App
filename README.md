# HomeMatch: LLM and Semantic Real Estate Listing Matching Application

Welcome to HomeMatch, a powerful tool designed to match real estate listings with buyers' preferences using semantic search techniques. This application utilizes cutting-edge technology to generate, store, and personalize real estate listings, providing users with tailored recommendations that align with their specific requirements.

## Installation Instructions

To set up and run HomeMatch, follow these steps:

1. Clone the repository to your local machine.
2. Initialize a Python project and set up a virtual environment.
3. Install the required dependencies using pip:  
`pip install -r requirements.txt`
4. Start Jupyter with: `jupyter notebook`
4. Navigate to the jupyter server home page and run the [HomeMatch.ipynb](HomeMatch.ipynb) file.

## Implementation Details

1. Generate Real Estate Listings: For a Demo, ChatGPT via openai (an LLM) was to generate real estate listings.
   The generated listing can be found in the [listing.json](data%2Flisting.json) file. You can replace this with
   your own listing.

2. Storing Listings in Vector Database: The generated listed is then stored in a vector database LancedDB 
   The description field are used to generated vector embeddings in the database table  for efficient retrieval.

3. Building the User Preference Interface: A simple interface using gradio is then used to collect the buyer's 
   preferences in natural language. 
   ![Screenshot 2024-03-16 at 9.05.24 PM.png](data%2FScreenshot%202024-03-16%20at%209.05.24%E2%80%AFPM.png)

4. Searching Based on Preferences: The collected buyer's preference is structured and used to perform semantic search on
   the vector database. The retrieval algorithm ensure accurate and relevant listing recommendations and returned.

5. Personalizing Listing Descriptions: Finally the descriptions of retrieved listings used ChatGPT LLM to tailor each 
   listing to the buyer's preferences which maintaining factual integrity of the original description.

## File Structure

The project files are organized as follows:
- [HomeMatch.py](HomeMatch.py): Not used. But can replace the `.ipynb` file if needed.
- [HomeMatch.ipynb](HomeMatch.ipynb)`utils.py`: Main application file.
- [requirements.txt](requirements.txt): Dependency requirements
- [data/listing.json](data%2Flisting.json): Raw listing generated with LLM
- `README.md`: This file containing project documentation.

## Dependencies

- LangChain
- [OpenAI]
- [LanceDB]

## Contributing Guidelines

## License Information

## Contact Information

For questions, feedback, or collaboration inquiries, please contact the project maintainer at hullo2chuks@gmail.com.
