# Albumy

*Capture and share every wonderful moment.*

## Technical Descriptions

### Two New ML-Powered Features:
1. **Alternative text generation** - Automatically generates alternative text descriptions for images.
2. **Image search** - Automatically tags images using an image detection model for improved search functionality.

**Details:**

- Alternative text is generated using Salesforce's BLIP pre-trained LLM.
- Tags are generated using API4AI's object detection model.
  
For detailed implementation, see the `albumy/blueprints/main.py` file.

### Evaluation of Features
- We uploaded 20 test images and verified that the automatically generated descriptions and tags were accurate.

### Interface Design
- Users upload photos, and automatically generated descriptions and tags can be viewed and edited.

### Production Challenges
- Cost considerations and scaling issues for large-scale use.
- Potential privacy concerns related to automatically generated descriptions.

### Future Work
- Implementing privacy controls and more cost-effective ML models.

### Project Documentation

Find the full technical report [here](docs/report.pdf) for more detailed information about the machine learning features.

This was my little project!

> Example application for *[Python Web Development with Flask](https://helloflask.com/en/book/1)* (《[Flask Web 开发实战](https://helloflask.com/book/1)》).

Demo: http://albumy.helloflask.com

![Screenshot](https://helloflask.com/screenshots/albumy.png)

## Installation

clone:
```
$ git clone https://github.com/greyli/albumy.git
$ cd albumy
```
create & activate virtual env then install dependency:

with venv/virtualenv + pip:
```
$ python -m venv env  # use `virtualenv env` for Python2, use `python3 ...` for Python3 on Linux & macOS
$ source env/bin/activate  # use `env\Scripts\activate` on Windows
$ pip install -r requirements.txt
```
or with Pipenv:
```
$ pipenv install --dev
$ pipenv shell
```
generate API key for replicate:
1. go on https://replicate.com/account/api-tokens
2. sign in with GitHub
3. provide a token name and then create token
4. copy token key then in the repository, create a file named `api.key`
5. paste the token key in the file and save

generate fake data then run:
```
$ flask forge
$ flask run
* Running on http://127.0.0.1:5000/
```
Test account:
* email: `admin@helloflask.com`
* password: `helloflask`

## License

This project is licensed under the MIT License (see the
[LICENSE](LICENSE) file for details).
