# carbon-footprint-and-energy-efficiency-experiments-of-llm-models
This project contains experiments with open-source LLM models to evaluate their carbon footprint and energy efficiency through code experiments, and it is open so that anyone can use them, as well as serving as an example of alternatives to proprietary models like GPT, Claude, etc.

## Installation
To set up the project, follow these steps:

1. Clone the repository:
    ```sh
    git clone https://github.com/yovannynogales/carbon-footprint-and-energy-efficiency-experiments-of-llm-models.git
    cd carbon-footprint-and-energy-efficiency-experiments-of-llm-models
    ```

2. Create a virtual environment and activate it:
    ```sh
    python -m venv carbon-footprint-and-energy-efficiency-project-env
    # For Unix-based
    source carbon-footprint-and-energy-efficiency-project-env/bin/activate
    # For Windows-based
    carbon-footprint-and-energy-efficiency-project-env\Scripts\activate
    ```

3. Install the main dependencies:
    ```sh
    # To run in CPU
    pip3 install torch torchvision torchaudio
    # or to run in GPU
    pip3 install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu126
    ```

4. Install the secundary dependencies:
    ```sh
    # To run in CPU
    pip3 install transformers
    pip3 install transformers
    pip3 install sentencepiece
    pip3 install autoawq accelerate
    pip3 install codecarbon
    pip3 install bert-score
    ```

5. Configure jupyter in a different terminal to use for all your conda environments (Depends on your preference to configure jupyter notebooks)
    ```sh
    pip3 install ipykernel
    python -m ipykernel install --user --name=carbon-footprint-and-energy-efficiency-project
    ```
    After you apply the step 5, restart the IDE that you are using.

5. Test to download and use it a small model to validate that everything is well configured.
    ```sh
    # For CPU
    python -c "from transformers import pipeline; nlp = pipeline('sentiment-analysis'); result = nlp('I love using Hugging Face Transformers'); print(result)"
    # For GPU
    python -c "from transformers import pipeline; nlp = pipeline('sentiment-analysis', device=0); result = nlp('I love using Hugging Face Transformers'); print(result)"
    ```

6. In case that you received some import errors for missing classes, please consider to update the torch dependencies to the proper version to use that clases:
    ```sh
    pip3 install torch==2.6.0+cu126 --index-url https://download.pytorch.org/whl/cu126
    pip3 install torchvision==0.20 --index-url https://download.pytorch.org/whl/cu126
    ```
    Try again to execute the step 5, everything has to be executed correctly now.

## Contributing
We welcome contributions to improve this project. Please follow these steps to contribute:

1. Fork the repository.
2. Create a new branch:
    ```sh
    git checkout -b feature-branch
    ```
3. Make your changes and commit them:
    ```sh
    git commit -m "Description of changes"
    ```
4. Push to the branch:
    ```sh
    git push origin feature-branch
    ```
5. Create a pull request.

## License
This project is licensed under the Apache License Version 2.0. See the [LICENSE](LICENSE) file for details.