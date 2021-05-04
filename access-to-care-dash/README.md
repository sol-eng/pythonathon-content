# Access to Care - Dash app

**Motivation** - To continue developing and refining the dash app.  Also, to document the steps needed to setup and run the Python environment itself.


## Running the app

### First time setup

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
      
