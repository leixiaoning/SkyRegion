# Sky Region AI Inference Server on Flask

  SkyRegion is an Image Segmentation Model, created by fine-tuning Mask R-CNN, which generates a mask for a given image. This repo is the Inference Server that can be used by Web Apps or Mobile Apps.

  * ### Example Input:
    <img src="images/input-1.png" width="50%" />

  * ### Output and Composite Image:
    <img src="images/mask-1.png" width="45%" /> &nbsp;&nbsp;&nbsp;
    <img src="images/composite-1.png" width="45%" />
    <br /> <br />

    Composite generated by applying a blur effect using the mask. This makes it easier for the user to understand what's happening.

  * Server IP: `<your-computer-ip>:8001`

  * ## Installation
    
    * Install required packages <br />
      `pip3 install -r requirements.txt`

    * Download models <br />
      `python3 download_models.py`

    * Run Server <br />
      `python3 app.py`

  * ## Installation (Docker) (Recommended)

    * To Build: <br />
      `docker build -t sky-region -f docker/Dockerfile .`
    
    * To Run:<br />
      `docker run -d --rm -p 8001:8000 --name sky-region sky-region`
