# How to Upload Data: A Step-by-Step Guide

This guide provides step-by-step instructions for uploading your porous media datasets to the Digital Porous Media Portal (DPM). Following these steps helps ensure your data is well-described, discoverable, and usable by the community.

**Before You Begin:**

* **Account:** Ensure you have registered for a TACC account at [https://accounts.tacc.utexas.edu/register](https://accounts.tacc.utexas.edu/register) and are logged into the DPM.
* **Data Organization:** Plan the structure of your data. Consider distinguishing between originating raw data and derived analysis data. It's often helpful to organize your files and folders locally on your computer or cloud storage (like Dropbox/UT Box) *before* uploading.
* **File Size:**
    * If your total dataset **exceeds 2GB**, please **email the DPM staff first** to discuss the upload.
    * Consider splitting very large volumetric files into smaller, manageable chunks (e.g., under 2GB each) before uploading. This aids users with downloading and processing the data later.
* **Compression:** **Avoid compressing** individual image files (e.g., into `.zip` or `.tar.gz` archives) before uploading if possible. Uploading raw or standard image formats directly allows the portal to automatically generate previews (like GIF movies) and perform basic analysis (like histograms). Use the portal's bulk upload options (Dropbox, UTBox) for transferring many files or large files efficiently.

---

**Step 1: Create or Select a Project**
All data on DPM belongs to a "Project".

1.  Log in to the DPM and navigate to the **"My Projects"** interface.
2.  Choose one:
    * **Create a New Project:** Click the option to create a new project. Provide a descriptive name.
        * *Note on Ownership:* For citation purposes, it's best if the primary data author is the project owner. If someone else (e.g., a student or assistant) will be uploading the data, the data owner should ideally create the project and then add the uploader as a collaborator (see Step 2).
    * **Use an Existing Project:** If you are adding data to a project you previously created, simply navigate to and open that project.

**Step 2: Add Collaborators (Optional)**

If members of your team need to help manage the project or view the data while it's still private:

1.  Ensure your collaborators are registered users on the DPM.
2.  Within your project's management interface, find the option to add collaborators.
3.  Add them using their registered DPM/TACC username or email. Collaborators can then edit the project and upload data.

**Step 3: Upload Your Data Files**

1.  Inside your selected project, find the data upload section or button.
2.  Choose your preferred upload method:
    * **Dropbox:** Link your Dropbox account to transfer files directly.
    * **UTBox:** Link your UTBox account (if applicable) to transfer files directly.
    * **Drag-and-Drop:** Drag files or folders directly from your computer onto the designated upload area in your web browser.
3.  Select the prepared files/folders and start the upload process. Monitor the progress as indicated by the interface.

**Step 4: Add Metadata (Crucial!)**

Metadata (data about your data) is essential for making your dataset understandable and usable. You will be prompted to add metadata for your project and individual files.

1.  **Project Description:** Provide a clear description of the overall project, the physical sample(s), and the experiment(s) involved. Link to relevant publications if available.
2.  **File-Level Metadata:** For each uploaded data file (especially images), provide necessary details.
3.  **Minimum Requirements:** The DPM enforces minimum metadata standards. Pay attention to warnings indicating missing required information. The more detail you provide, the more valuable your dataset becomes.
4.  **Critical Metadata for Raw Binary Images:** Raw binary files (`.raw`, `.bin`, etc.) do not contain size or format information internally. To allow DPM to display them correctly, you **must** provide:

    * **Voxel Dimensions:** The number of voxels (pixels in 3D) in each direction (e.g., width, height, depth/slices).
    * **Voxel Size:** The physical size of one voxel (e.g., in µm). If not applicable (e.g., for synthetic data), enter '1' and make a note in the description.
    * **Data Type:** The numerical format (e.g., 8-bit unsigned integer, 16-bit signed integer, 32-bit float).
    * **Byte Order (Endianness):** Specify 'Big Endian' or 'Little Endian'. This is critical for multi-byte data types (16-bit, 32-bit, etc.). If unsure, you might need to try both – upload the metadata, check the preview (Step 5), and edit if it looks scrambled. (Note: For 8-bit data, byte order doesn't typically matter).
    * *Tip:* If unsure about these parameters, try opening your raw file in software like ImageJ/Fiji locally first to determine the correct settings.

**Step 5: Verify Previews (Especially for Volumetric Images)**

1.  After the upload and metadata entry, the portal will often attempt to generate a preview (e.g., a GIF movie slicing through a 3D volume).
2.  Check the preview on the project page. Does it look as expected?
3.  **Troubleshooting Low-Range Binary Data:** If you uploaded segmented data (e.g., values 0, 1, 2) as a raw binary file, the preview might initially look black or very dark. This is because the visualizer scales to the full potential range (e.g., 0-255 for 8-bit). To fix this:
    * Navigate to the specific image file within your project.
    * Click the **"Actions"** tab/button associated with that file.
    * Select **"Edit"**.
    * Find and check the option labeled **"Use binary correction"** (or similar wording).
    * **Save Changes**.
    * The task to re-render the preview will be queued, and it should update shortly to display the limited range correctly.

**Step 6: Review and Finalize**

Your uploaded data is now stored **privately** within your project.

* Review all uploaded files and metadata for accuracy and completeness.
* You can continue to add/edit data and metadata while the project remains private.
* Once you are satisfied and ready to make the data public, you can proceed with the publication request process (covered in the "Publish Datasets" guide - `publish.md`). Metadata cannot be easily edited by you after publication.

---

For further details on specific file formats or metadata fields, please refer to the relevant sections of the documentation. If you encounter issues, contact the DPM support team.
