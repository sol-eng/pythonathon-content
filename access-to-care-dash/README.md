# Access to Care - Dash app

**Motivation** - To continue developing and refining the dash app.  Also, to document the steps needed to setup and run the Python environment itself.


## Setup Inside R, using `reticulate`

1. Load `reticulate`, and create a virtual environment called "dash"
         
      ```r
      library(reticulate)
      
      virtualenv_create("dash")
      ```

2. Install the needed Python packages, in this case: `dash`, `requests` and `pandas`
         
      ```r
      virtualenv_install("dash", c("dash", "requests", "pandas"))
      ```
      
## Running the app

1. After creating the virtual environment, restart RStudio

2. Before loading `reticulate` set the `RETICULATE_PYTHON` environment variable to point to the new virtual environment
      
      ```r
      Sys.setenv("RETICULATE_PYTHON" = "~/.virtualenvs/dash/bin/python")
      ```
      
3. Set working directory to the "access-to-care-dash" sub-folder. This is mainly so that the references to the CSS and pictures inside the "assets" folder work.

      ```r
      setwd("access-to-care-dash")
      ```
4. Source the "app.py" script using `source_python`, or by clicking on the "Source Script" button in the IDE

      ```r
      reticulate::source_python("app.py")
      ```

## Setup outside of R

1. Install `virtualenv`

      ```
      pip install virtualenv
      ```
2. Create a new Virtual Environment in a folder called `env`
      
      ```
      virtualenv access-to-care-dash/env
      ```

3. Activate the Virtual Environment by running the `activate` script inside the `bin` sub-folder

      ```
      source access-to-care-dash/env/bin/activate
      ```
      
4. Confirm that the Python environment is pointed to`...env/bin/python` 

      ```
      which python
      ```
      
5. Install the `dash`, `pandas`, and `requests` packages.

      ```
      pip install dash pandas requests
      ```

6. Run the app in the terminal

      ```
      python access-to-care-dash/app.py
      ```
      