# Community Data

Community data are curated and placed in the designated directory by administrators or curators. Users can access these datasets while working with the [applications](jupyter_apps.md).

Within each Jupyter Hub session, users may locally modify copies of the community data. However, these modifications are session-specific and do not affect the global datasets. Each time a user starts a new Jupyter Hub session, the original community data will be available in the corresponding directory. If users wish to retain any changes made to the community data, they should transfer the modified files to their personal or allocated storage.


## How Do Admins Move the Community Data?

The Community Applications project is a special type of project designed for centralized data sharing. Only authorized administrators can add data to the Community Applications project. You can skip this part if you are a regular user.

To upload community data, admins should follow these steps:

1. **Navigate to the Correct Location:**  
   Community data uploads must be performed through the path:  
   `Data Files > Dataset > Community Applications`  
   [Direct link to the Portal](https://digitalporousmedia.org/workbench/data/tapis/projects/drp.project.root)

2. **Initiate the Upload:**  
    Click the purple **"+Add"** button and select the appropriate action:

    - Create a folder
    - Create a new dataset
    - Upload data from your local system to the current location

    /// admonition | Warning
            type: caution 

        Data cannot be uploaded directly to the "Community Applications" project exposed under `Data Files > Community Applications`. Instead, admins must use the special project accessible only to admin users under `Data Files > Datasets > Community Applications`.
    ///

3. **Data Visibility:**  
   Once an approved admin uploads data into the special "Community Applications" project the data will become visible (read-only) to all users under the path `Data Files > Community Applications`.

4. **JupyterHub Integration:**  
   There is no conflict between having an active JupyterHub session and uploading data to Community Applications. Users in JupyterHub will see new data appear under the "Community" folder once it is properly uploaded by an admin. If the new data does not appear automatically, users can click the refresh icon (small circular arrow) in the Jupyter file browser to update the file listing.

5. **Concurrent Uploads:**  
   Multiple admins can upload data to the Community Applications project simultaneously without conflict.

If you encounter any issues or require additional permissions, please contact the DPM team.
