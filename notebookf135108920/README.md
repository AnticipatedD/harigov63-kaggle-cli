# Install dependencies as needed:
# pip install kagglehub[hf-datasets]
import kagglehub
from kagglehub import KaggleDatasetAdapter

# Set the path to the file you'd like to load
file_path = ""

# Load the latest version
hf_dataset = kagglehub.load_dataset(
  KaggleDatasetAdapter.HUGGING_FACE,
  "harigov63/training-labels-updated-csv",
  file_path,
  # Provide any additional arguments like 
  # sql_query, hf_kwargs, or pandas_kwargs. See 
  # the documenation for more information:
  # https://github.com/AnticipatedD/harigov63-kaggle-cli/blob/main/README.md#kaggledatasetadapterhugging_face
)

print("Hugging Face Dataset:", hf_dataset)

---

# Install dependencies as needed:
# pip install kagglehub[pandas-datasets]
import kagglehub
from kagglehub import KaggleDatasetAdapter

# Set the path to the file you'd like to load
file_path = ""

# Load the latest version
df = kagglehub.load_dataset(
  KaggleDatasetAdapter.PANDAS,
  "harigov63/training-labels-updated-csv",
  file_path,
  # Provide any additional arguments like 
  # sql_query or pandas_kwargs. See the 
  # documenation for more information:
  # https://github.com/AnticipatedD/harigov63-kaggle-cli/blob/main/README.md#harigov63-kaggle-cli-kaggledatasetadapterpandas
)

print("First 5 records:", df.head())
