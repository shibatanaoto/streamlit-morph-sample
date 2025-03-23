# Deploy Streamlit App with Morph

## 1. Create a streamlit app

```bash
pip install streamlit
touch main.py
```
## 2. Create a `morph_project.yml` file in the project   root.

`deployment.provider` is needed to be set as `gcp` for Streamlit App.

```yaml
version: '1'

package_manager: pip

build:
  framework: streamlit
  runtime: python3.12
  context: .

deployment:
  provider: gcp
```

## 3. Create a `requirements.txt` file in the project root.

```bash
pip freeze > requirements.txt
```

## 4. Deploy

Create a Github repository and push the project.
And then, you can deploy the app from Morph Dashboard.

https://docs.morph-data.io/docs/en/quickstart/deploy

