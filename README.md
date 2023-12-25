[Next.js'](https://nextjs.org/docs) [Image component](https://nextjs.org/docs/app/api-reference/components/image) allows a ['blurred' placeholder image](https://nextjs.org/docs/app/api-reference/components/image#blurdataurl). The placeholder image is shown while the real image is loading.

For my [photography portfolio website](https://github.com/seanislegend/seanislegend.com), I want to placeholder images instead of spinners. However, I use Contentful as my CMS and it does not support Base64 encoded images, which is required for the placeholder image.

This small API is used as webhook by Contentful. When a new 'Photo' entry is published, it will fetch the image from Contentful, resize it to the 10px size needed, and then return a Base64 encoded string. This string is then saved to the Photo entry in Contentful so it can then be retrieved when loading data for the portfolio website.
