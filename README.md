"PRODIGY_Trackcode_02"

from diffusers import StableDiffusionPipeline
import Torch


model_id = "runwaym1/stable-diffusion-v1-5"
pipe = StableDiffusionPipeline.from_pretrained(model_id, torch_dtype=torch.float16)
pipe = pipe.to("cuda")
def generate_image(prompt):
    image = pipe(prompt).images[0]
    return image
    
    
    def generate_from_text(text_prompt):
    image ="astronaut riding a horse_image(text_prompt)"
    
    return image