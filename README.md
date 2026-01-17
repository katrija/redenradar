# redenradar

This repository contains data and jupyter notebooks used in the project "redenradar" which I completed together with a group as part of the [TechLabs Digital Shaper Program]([https://link-url-here.org](https://www.techlabs.org/digital-shaper-program) on Deep Learning (Winter 2024/25). 

The idea of the project was to use a Large Language Model (LLM), in our case, GottBERT (Scheible et al, 2024), to predict the party affiliation of speakers in the German Bundestag. Speeches were obtained from the plenary minutes accessible via the [Open Data Service of the German Bundestag](https://www.bundestag.de/services/opendata). In initial steps, we cleaned the data (e.g., special characters were removed) and performed some preprocessing (e.g., party names were removed from the speeches, equal representation of parties was ensured via upsampling). We divided the data into a training, validation and test set (training: years 2020 - 2021, validation: year 2023, test: years 2024-2025), and used the transformers and PyTorch modules for tokenization and training.

The final model yielded an accuracy of about 70 % for the validation set. Across parties, precision ranged from 56 % (CDU/CSU) to 91 % (AfD), and recall ranged from 53 % (FDP) to 89 % (AfD). Confusions reflected similarity on the political spectrum as well as cooperation of parties in coalition.

Scheible, R., Frei, J., Thomczyk, F., He, H., Tippmann, P., Knaus, J., Jaravine, V., Kramer, F., & Boeker, M. (2024). GottBERT: a pure German Language Model. In Y. Al-Onaizan, M. Bansal, & Y.-N. Chen (Eds.), Proceedings of the 2024 Conference on Empirical Methods in Natural Language Processing (pp. 21237–21250). Association for Computational Linguistics. https://doi.org/10.18653/v1/2024.emnlp-main.1183
