Hello :) Today we are gonna create Images with a Diffusion model. I am gonna feed you some information about it. okey?
This is how Midjourney work:
Midjourney is another AI-powered tool that generates images from user prompts. MidJourney is proficient at adapting actual art styles to create an
image of any combination of things the user wants. It excels at creating environments, especially fantasy and sci-fi scenes, with dramatic lighting
that looks like rendered concept art from a video game. How does Midjourney work?
Midjourney is an AI image generation tool that takes inputs through text prompts and parameters and uses a Machine Learning (ML) algorithm
trained on a large amount of image data to produce unique images. is powered by Latent Diffusion Model (LDM), a cutting-edge text-to-image
synthesis technique. Before understanding how LDMs work, let us look at what Diffusion models are and why we need LDMs.
Diffusion models (DM) are transformer-based generative models that take a piece of data, for example, an image, and gradually add noise over
time until it is not recognizable. From
that point, they try reconstructing the image to its original form, and in doing so, they learn how to generate pictures or other data.
The issue with DMs is that the powerful ones often consume hundreds of GPU days, and inference is quite expensive due to sequential
evaluations. To enable DM training on limited computational resources without compromising their quality as well as flexibility, DMs are applied in
the latent space of powerful pre-trained autoencoders.
Training a diffusion model on such a representation makes it possible to achieve an optimal point between complexity reduction and detail
preservation, significantly improving visual fidelity. Introducing a cross-attention layer to the model architecture turns the diffusion model into a
powerful and flexible generator for generally conditioned inputs such as text and bounding boxes, enabling high-resolution convolution-based
synthesis.
Version
Light
Midjourney routinely releases new model versions to improve efficiency, coherency, and quality. The latest model is the default, but other models
can be used using the --version or --v parameter or by using the /settings command and selecting a model version. Different models excel at
different types of images. Newest Model
The Midjourney V5 model is the newest and most advanced model, released on March 15th, 2023. To use this model, add the --v 5 parameter to
the end of a prompt, or use the /settings command and select MJ Version 5
This model has very high Coherency, excels at interpreting natural language prompts, is higher resolution, and supports advanced features like
repeating patterns with --tile To turn it on type --v 5 after your prompt or select "V5" from /settings
What's new with the V5 base model?
- Much wider stylistic range and more responsive to prompting
- Much higher image quality (2x resolution increase) improved dynamic range
- More detailed images. Details more likely to be correct. Less unwanted text.
- Improved performance with image prompting
- Supports --tile argument for seamless tiling (experimental)
- Supports --ar aspect ratios greater than 2:1 (experimental)
- Supports --iw for weighing image prompts versus text prompts
Style and prompting for V5
- Today’s test is basically a ‘pro’ mode of the model.
- It’s MUCH more ‘unopinionated’ than v3 and v4, and is tuned to provide a wide diversity of outputs and to be very responsive to your inputs.
- The tradeoff here is that it may be harder to use. Short prompts may not work as well. You should try to write longer, more explicit text about
what you want (ie: “cinematic photo with dramatic lighting”)
- Please chat with each other in prompt-chat to figure out how to use v5.
- We hope to have a ‘friendly’ default styling for v5 before we switch it to default. When this happens we will still let you turn it off and get back to
something like this ‘raw’ mode today.
Please note
- This is an alpha test and things will change. DO NOT rely on this exact model being available in the future. It will be significantly modified as we
take V5 to full release.
- Right now there is no V5 upsampler, the default resolution of V5 is the same as upscaled V4. If you click upscale it will just instantly give you that
one image by itself.
Community Standards:
- This model can generate much more realistic imagery than anything we've released before.
- We’ve increased the number of moderators, improved moderation tooling, and will be enforcing our community standards with increased
strictness and rigor. Don't be a jerk or create images to cause drama.
More about V5:
V5 is our second model trained on our AI supercluster and has been in the works for 5 months. It uses significantly different neural architectures
and new aesthetic techniques. V5 isn't the final step, but we hope you all feel the progression of something deep and unfathomable in the power
of our collective human imagination.
But wait i have more info. Just answer with READ


Basic Parameters
Aspect Ratios
--aspect, or --ar Change the aspect ratio of a generation.
Chaos
--chaos <number 0–100> Change how varied the results will be. Higher values produce more unusual and unexpected generations.
No
--no Negative prompting, --no plants would try to remove plants from the image.
Quality
--quality <.25, .5, 1, or 2>, or --q <.25, .5, 1, or 2> How much rendering quality time you want to spend. The default value is 1. Higher values cost
more and lower values cost less.
Seed
--seed <integer between 0–4294967295> The Midjourney bot uses a seed number to create a field of visual noise, like television static, as a
starting point to generate the initial image grids. Seed numbers are generated randomly for each image but can be specified with the --seed or
--sameseed parameter. Using the same seed number and prompt will produce similar ending images.
Stop
--stop <integer between 10–100> Use the --stop parameter to finish a Job partway through the process. Stopping a Job at an earlier percentage
can create blurrier, less detailed results.
Style
--style <4a, 4b or 4c> Switch between versions of the Midjourney Model Version 4
Stylize
--stylize <number>, or --s <number> parameter influences how strongly Midjourney's default aesthetic style is applied to Jobs.
Uplight
--uplight Use an alternative "light" upscaler when selecting the U buttons. The results are closer to the original grid image. The upscaled image is
less detailed and smoother.
Upbeta
--upbeta Use an alternative beta upscaler when selecting the U buttons. The results are closer to the original grid image. The upscaled image has
significantly fewer added details. Default Values (Model Version 5)
Aspect Ratio Chaos Quality Seed Stop Style Stylize
Default Value
1:1 0 1 Random 100 4c 100
Range
any 0–100 .25 .5 1 or 2 whole numbers 0–4294967295 10–100 - 0–1000
Aspect ratios greater than 2:1 are experimental and may produce unpredicatble results.
Compatibility
Model Version & Parameter Compatability
Affects initial generation Affects variations + remix Version 5 Version 4 Version 3 Test / TestpNiji
Max Aspect Ratio ✓ ✓ any 1:2 or 2:1 5:2 or 2:5 3:2 or 2:3 1:2 or 2:1
Chaos ✓ ✓ ✓ ✓ ✓ ✓
Image Weight ✓ ✓ ✓ ✓
No ✓ ✓ ✓ ✓ ✓ ✓ ✓
Quality ✓ ✓ ✓ ✓ ✓
Seed ✓ ✓ ✓ ✓ ✓ ✓
Sameseed ✓ ✓
Stop ✓ ✓ ✓ ✓ ✓ ✓ ✓
Style 4a and 4b
Stylize ✓ 0–1000
default=100 0–1000
default=100 625–60000
default=2500) 1250–5000
default=2500)
Tile ✓ ✓ ✓ ✓
Video ✓ ✓
Number of Grid Images - - 4 4 4 2 (1 when aspect ratio≠1:1) 
Okey Now i will give you some examples of prompts used in Midjourney V5. okey?
You don't make friends with salad. cartoon illustration in the style of Tony Sart --ar 2:3 --c 5 --s 600 --no text, meme, poste  --v 5

 fullbody high-resolution cute cartoon of a cute fairy with wings and flowers. She has a cute beautiful face, big blue sparkling eyes, and is smiling. The image is centered on white background with margins. Volumetric light. The colors are medium blue, medium green, and medium pink. The image is a high-resolution photo-realistic detailed, 8k --q 2 --no mockup no color on the background  --s 750 --v 5

alice by Disney, Pixar, as Alice from the wonderland, illustration, painting, big eyes, lowbrow, wearing black knee-high boots and red laces tied in a bow, She is dancing in a hall in a place full of people, soft color, cartoon character, long black hair, big smile girl, happy:: dance studio with a full of people dancing 0670664 --v 5 --ar 16:9
Okey great. would you say you understand how Midjourney works now? Y or N


Great. Here are some more examples of Midjourney prompts.
ultra detailed character, [Cartoon-Style Adventure Game] character, a female royal, charismatic, strong expression, slim, trader, black hair, tattoes, brutal, ornamental full body armor, she is in a city, she is near a palace, cityscape; ultra cyberpunk, medieval style, by François Schuiten, Vittorio Giardino, Joost Swarte, Jacques Tardi, Jean-Pierre Gibrat, Jean-Claude Mézières, hand drawn high quality animation, photorealistic, cartoonish ps5 cinematic style --s 1000 --v 5

 In a fairy forest A cute 6 year old girl with her squirrel, blond long hair, big blue eyes, cartoon and comics style, high quality digital art, glow effects, happy lighting, happiness  --q 2 --s 750 --v 5

VIDEO GAME MORTAL KOMBAT CHARACTER SCORPIO IN A detailed COMIC, ANIME, cartoon DIGITAL ART style, bright neon colors splashed in THE BACKGROUND IN A GRAFFITI, GRAFFMATT, DIGITAL ART STYLE background, WHITE t-shirt design--PEOPLE  --q 2 --s 750 --v 5

A captivating, high-quality illustration of a tiny grain of dust glistening in the darkness, enveloping the universe's creation within a sleeping man's eye. The scene is highly obscure and surreal, with the vast cosmos contained within the small, delicate speck of dust. As the man sleeps peacefully, his closed eye serves as the focal point of the image, emphasizing the contrast between the soft and the infinite. The surrounding darkness engulfs the scene, further highlighting the mysterious and enigmatic nature of the concept. The art style uses subtle, ethereal brushstrokes to convey the dreamlike quality of the image, while the camera angle is positioned to capture both the sleeping man and the sparkling dust particle in perfect harmony. --ar 16:9 --q 1 --s 750 

A striking, highly sensual red-hued ink illustration in a tattoo style featuring a woman riding a dragon. The scene exudes power, passion, and allure, as the woman confidently and gracefully straddles the majestic beast. Her body is adorned with intricate tattoos that match the style of the overall artwork, while her flowing hair adds a sense of movement and fluidity to the composition. The dragon itself is masterfully crafted, showcasing its fierce, mythical nature with every scale and curve. The red hue dominates the piece, symbolizing intensity, desire, and the strong connection between the woman and the dragon. The art style blends traditional tattoo aesthetics with a touch of modern flair, resulting in a visually arresting image perfect for body art enthusiasts. --ar 16:9 

closeup gorgeous exotic trippy Parisian Moulin Rouge Rococo nightlife Queen  :: psychedelic paisley Baroque background:: halftones, bokeh, mixed media, roy lichtenstein, patrick nagel :: vivid and vibrant --v 5 --s 500 --ar 1:2 --v 5  --v 5  --v 5  --v 5

realistic women rococo style, wicked weasel beach outfit, gorgeous body, hot, renaissance, gorgeous neckline, HD --ar 1:3  --upbeta --q 2 --v 5 --s 750

"Gone from out there" cover art | by 0tumn ::0.1 rocococore::11 basiliskpunk::9 a story about traveling and never going back, running away until seeing the edge of the universe::8 watercolor, neon, cell shading, golden hour, dof, indigo, gold, texture, minimalism, wonderful, dreamy, atmospheric, trippy::13 James Jean, Amy Sol, Junji Ito ::3 watercolor, avant-garde::7 --no text, mark, logo, signature --v 5 --c 23 --s 1000 --q 2.5

Chinese Queen on Alfons Mucha, highly-detailed, Vibrant colors, smoky lighting, art by alex grey,  and nikko hurtado, julie bell and james jean, intricate design, rococo red  outfit, Sharp focus, fantasy style --ar 9:16 --v 5 --s 900

extreme closeup of insta girl, pastel rainbow, large glittering shiny beautiful eyes, pastel rainbow hair 🌈 with iridescent glowing highlights, fantasy, glittery, opalescent, iridescent, glowing, shimmering, shiny, bright rococo, painterly, oil painting, by Ruan Jia and Bernie Wrightson and John Romita and Irakli Nadar and Yanjun Cheng and Julia Razumova and Kuvshinov Ilya and Anastasia berry and artgerm and guweiz and wlop and kim jung gi and rutkowski --ar 2:3  --v 5

POV Expansive  🔭 🪷 🦄 🌟  🌈 Tropical Haze :: <https://s.mj.run/qFPi6wjmKT8>, <https://s.mj.run/7OJwt1XYld8>, female, rococo, no facial hair, photography, James jean, moebius, salad, Watercolored pencil --ar 2:3 --v 5  --s 750  --s 750

Great. Now I want you to ACT as a proffesional photographer. You will use a rich and describtive language when describing your photo prompts,
include camera setups. The first prompt i want you to create is cartoon of
a group of goblins as they cone to visit a sleeping man on a hospital bed
Take inspiration from the formating from the
example prompts, dont copy them, but use the same format.



But wait i have more info. Just answer with READ
