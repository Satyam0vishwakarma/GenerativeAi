# GenerativeAi
"This repository is based on an internship project. The project-related images are uploaded here."
Some sample Generated Images : 
***
# An ancient underwater temple with divine idols and a diver exploring the
scene. Light streams through the dark, murky water, highlighting carvings and fish swimming around. The scene is serene and mystical.
![ComfyUI_00003_](https://github.com/user-attachments/assets/8082c78e-92c8-40cd-8649-3b797fbf4e7f)

***
# A group of swans flying on the top of river
![ComfyUI_00006_](https://github.com/user-attachments/assets/c0f7ec93-6f22-444d-835c-eeb5e7ad47f7)

***
# A misty forest at dawn , with sunlight streaming through the trees.
![ComfyUI_00022_](https://github.com/user-attachments/assets/d31f4bea-90ec-4fb7-aba5-a4316f5b5c30)
***
# A wide-open field under a brilliant star-filled sky, with the Milky Way clearly visible.
![ComfyUI_00025_](https://github.com/user-attachments/assets/782331b9-0d2b-4e5c-ae3b-d4683d975977)
***
# A snowy village under the clear sky attached to the snow mountains.
![ComfyUI_00029_](https://github.com/user-attachments/assets/eaac5019-0ffc-4d7a-ba47-e4d1351a49bd)
![ComfyUI_00030_](https://github.com/user-attachments/assets/c034f21d-3fa1-4739-a8c0-94cb660fef8e)
![ComfyUI_00031_](https://github.com/user-attachments/assets/19a45ecd-4053-4bad-80e1-2670823079c3)
***
# A stunning nebula stretching across the night sky, with vibrant swirls of purples, blues, reds, and golds. The stars scattered throughout create a dazzling cosmic dance, painting a breath-taking masterpiece in space.
![ComfyUI_00032_](https://github.com/user-attachments/assets/51b65532-bbd2-48e1-8690-723a5b526572)
***
# The Egyptian pyramids standing tall in the desert, with a cloudless sky overhead
![ComfyUI_00033_](https://github.com/user-attachments/assets/9c4ae08f-1f17-4ad8-a00f-e5c47386862d)
***
# A playful kitten chasing a ball of yarn
![ComfyUI_00034_](https://github.com/user-attachments/assets/d56a3831-1c5b-422d-99d3-5cd9eeab463b)

***
Before starting the project is based on Image generation(Internship Based).
Entitled with _**"IMAGE GENERATION USING STABLE DIFFUSION AND COMFY UI"**_
Requirements: You should have a good Pc/Laptop with minimum of 8GB Ram or A Nvidia GPU with updated drivers.

* Now Lets move on to the project.
1. Download & Install Comfy UI: Get Comfy UI from the official GitHub repository. Extract the files and navigate to the Comfy UI folder.
![image](https://github.com/user-attachments/assets/93c00759-d6c4-48db-b21c-d7aa18d8a350)


2. Download Stable Diffusion Model: Obtain a Stable Diffusion .safetensors model from Hugging Face or another source. Place it inside the Comfy UI/models/checkpoints/ directory.
![image](https://github.com/user-attachments/assets/16b71261-eb55-4022-993b-4250f1d51649)


3. Run Comfy UI: Navigate to the Comfy UI directory and run the windows batch file (run_cpu or run_nvidia_gpu). Once running, access the UI at: http://127.0.0.1:8188.
![image](https://github.com/user-attachments/assets/0ba9c36d-23eb-4695-935a-bd83c475e145)

* Generating Images
1. Open Comfy UI Interface: Launch the Comfy UI interface.
![image](https://github.com/user-attachments/assets/46186a23-af95-49b2-b48f-b68d789c89db)

***


2. Enter Prompt: Type your desired prompt in the text box.

* ![image](https://github.com/user-attachments/assets/6474749c-337f-4848-8264-3986a10c1d59)

***


First prompt box for positive prompt(your prompt)


* ![image](https://github.com/user-attachments/assets/21c1d49e-9898-4d12-be03-b2c860da8bb1)

Second prompt box for negative prompt box(it can be like no blur, no human, etc.)


![image](https://github.com/user-attachments/assets/633c5f42-c03c-470e-83bf-dbeaff86c49d)

***


3. Generate Image: Click the Generate button(Queue) to create an image. The generated images will be saved in the output directory
beside the Queue button, batch available that is simply the number of images you want to generate.


### Main components:

Nodes: These represent specific functions, such as loading models, generating images, etc. Each node performs a particular task within the workflow1.

Connections: Lines that connect nodes, indicating the flow of data between them.

Input/Output Ports: Small dots on nodes, with purple indicating input and orange indicating output.

Workflow Canvas: The area where you can drag and drop nodes to create your workflow.

Node Menu: A menu that allows you to add nodes by right-clicking on the canvas and searching for the needed nodes.

Node Operations: Various operations like duplicating nodes (hold Alt while dragging), modifying parameters (double-click nodes), and deleting nodes (press Delete key).

Workflow Import/Export: You can export workflows as JSON files and import them by dragging and dropping the file onto the interface or using the Load button.


### Some specific components
KSampler: This node is used for advanced sampling operations within generative models. It allows customization of the sampling process through various parameters like model selection, seed control, steps, conditioning factors, and denoising levels1. It's essential for generating new data samples by manipulating latent space representations.

Load Checkpoint: This node loads a diffusion model that can be used by other nodes like KSampler.

CLIP Text Encode: Encodes a text prompt using a CLIP model into an embedding, providing a conditioning embedding for the sampling process.

VAE Decode: Decodes the denoised latent image output from KSampler into ordinary image data.

Empty Latent Image: Provides an empty latent image as input for workflows that generate images from scratch.

Image to Image Workflow: Uses an initial image and text prompt to guide the generation of new images.

The project uses the stable diffusions model and comfy UI. The Comfy UI is a for User interface and the stable diffusion model act as brain of the project.
