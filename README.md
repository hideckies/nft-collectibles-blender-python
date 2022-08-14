# NFT Collectibles using Blender Python

![image](https://blog.hdks.org/img/create-nft-3d-collectibles-using-blender-scripting/top_image.png)

## What is this?

This project is to demonstrate for generating NFT Collectible **Avatar-Styled** images.
For details, please check https://blog.hdks.org/Create-NFT-3D-Collectibles-Using-Blender-Scripting/ .

## How to Use

### 1. Clone this repository

```bash
git clone https://github.com/hideckies/nft-collectibles-blender-python.git
```

### 2. Settings in script files

```bash
cd nft-collectibles-blender-python
cd scripts
```

Set the value of each setting in script files.  
In particular, **PROJECT_DIR should be set to the absolute path to this repository you cloned.**

In *gen_metadata.py*,

```py
# gen_metadata.py

#  --- Settings --------------------------------------------

# ...

# An absolute path for the root directory
PROJECT_DIR = "c:/nft-collectibles-blender-python/"

# ...

# ---------------------------------------------------------
```

In *gen_model.py*,

```py
# gen_model.py

#  --- Settings --------------------------------------------

# ...

# An absolute path for the root directory
PROJECT_DIR = "c:/nft-collectibles-blender-python/"

# ...

# ---------------------------------------------------------
```

* Set the same path to **PROJECT_DIR** for both files. Currently, I don't know how to import variables from other files in Blender Python.


## 3. Run gen_metadata.py

Open Blender and move to **Scripting** workspace.  

![screenshot_1](https://blog.hdks.org/images/Create-NFT-3D-Collectibles-Using-Blender-Scripting/screenshot_scripting_workspace.jpg)  

To check the status during processing, you can open the console by clicking **“Window”-> “Toggle System Console”** in the top menu.  

In Scripting workspace, click the **Open** -> choose a *gen_metadata.py* -> click the **Run Script**. 

*If you get the error message **"ERROR: Properties duplicate."**, please run again.  
This message show when there is a metadata for each file that has exactly the same attributes. To create a unique collection, you have to avoid duplication.  


When completed, you should see json files like *0.json*, *1.json*, ... in *outputs* directory.  


## 4. Run gen_model.py

Click the **Open** -> choose a *gen_model.py* -> click the **Run Script**.  

When completed, you should see image files like *0.png*, *1.png*, ... in *outputs* directory.  


