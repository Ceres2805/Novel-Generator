# Novel Generator

This project generates a full-length novel using the Gemini API. The generated novel follows the traditional three-act structure with well-developed characters, conflicts, and resolutions.

## Requirements

- Python 3.x
- `google-genai` library
- `pyttsx3` library

## Installation

1. Clone the repository:
    ```sh
    git clone https://github.com/yourusername/Novel-Generator.git
    cd Novel-Generator
    ```

2. Install the required libraries:
    ```sh
    pip install google-genai pyttsx3
    ```

## Usage

1. Open the [`novel_generator.ipynb`](http://_vscodecontentref_/1) notebook in Jupyter Notebook or Jupyter Lab.
2. Set your Gemini API key:
    ```python
    client = genai.Client(api_key="your_api_key")
    ```
3. Define the genre, theme, and character profile for your novel:
    ```python
    genre = "genre"
    theme = "theme"
    character_profile = "character profile"
    ```
4. Run the notebook cells to generate the novel. The novel will be saved in the `generated_novel` folder as [generated_novel.txt](http://_vscodecontentref_/2).
5. Convert the generated text to audio:
    ```python
    text_chunks = split_text(novel_text)
    text_to_audio(text_chunks, 'generated_novel')
    engine.runAndWait()
    ```
    
## Credits

- Developed by [Ceres2805](https://github.com/Ceres2805)

## License

This project is licensed under the MIT License.

