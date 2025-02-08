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

1. Open the [novel_generator.ipynb](http://_vscodecontentref_/2) notebook in Jupyter Notebook or Jupyter Lab.

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

4. Run the notebook cells to generate the novel. The novel will be saved in the `generated_novel` folder as `generated_novel.txt`.

5. Convert the generated text to audio:
    ```python
    text_chunks = split_text(novel_text)
    text_to_audio(text_chunks, 'generated_novel')
    engine.runAndWait()
    ```

## Functions

### `generate_novel_segment(genre, theme, character_profile, full_novel, start_text="")`
Generates a segment of the novel based on the provided genre, theme, character profile, and the text generated so far.

### `generate_full_novel(genre, theme, character_profile, total_words=80000)`
Generates the full novel by repeatedly calling `generate_novel_segment` until the desired word count is reached.

### `print_novel(novel_text)`
Prints the novel text in real-time.

### `split_text(text, max_length=5000)`
Splits the text into chunks of a specified maximum length.

### `text_to_audio(text_chunks, folder_path)`
Converts text chunks to audio files and saves them in the specified folder.

## License

This project is licensed under the MIT License.

