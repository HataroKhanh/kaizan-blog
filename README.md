# Kaizan Blog

A minimal static blog built with [Eleventy (11ty)](https://www.11ty.dev/) and [Bun](https://bun.sh/). This project is containerized with Docker and ready for deployment with Nginx and Cloudflare Tunnels.

## Features

-   🚀 **Fast Build:** Powered by Bun for efficient package management and build processes.
-   ⚡ **Static Site Generation:** Eleventy (11ty) provides a flexible and lightning-fast site generation engine.
-   🖼️ **Image Optimization:** Automated image resizing and optimization using `@11ty/eleventy-img` for faster page loads.
-   💻 **Syntax Highlighting:** Integrated code block syntax highlighting with `@11ty/eleventy-plugin-syntaxhighlight`.
-   🐳 **Containerized:** Full Docker support with Nginx to serve the static site.
-   🔒 **Secure Deployment:** Built-in support for Cloudflare Tunnels for easy and secure public access.

## Tech Stack

-   **Generator:** Eleventy (11ty)
-   **Runtime:** Bun
-   **Styling:** Simple CSS
-   **Templating:** Nunjucks (`.njk`) and Markdown (`.md`)
-   **Deployment:** Docker, Nginx, Cloudflare Tunnels

## Getting Started

### Local Development

1.  **Install Dependencies:**
    ```bash
    bun install
    ```

2.  **Run Development Server:**
    ```bash
    bunx @11ty/eleventy --serve
    ```
    Your site will be available at `http://localhost:8080`.

### Docker Deployment

To build and run the site in a Docker container:

1.  **Set Environment Variables:**
    Create a `.env` file and add your Cloudflare Tunnel token:
    ```env
    CF_TUNNEL_TOKEN=your_token_here
    ```

2.  **Start Services:**
    ```bash
    docker-compose up -d
    ```

The site will be served by Nginx on port 8080 (mapped from port 80 in the container).

## Project Structure

-   `_includes/`: Contains site layouts and templates.
-   `css/`: Global stylesheets (using Simple.css).
-   `images/`: General image assets.
-   `js/`: Client-side JavaScript (e.g., code-copying, image zooming).
-   `posts/`: Markdown files for blog articles.
-   `.eleventy.js`: Main configuration file for Eleventy, including custom shortcodes and plugins.
-   `Dockerfile`: Multi-stage build for the Bun-based site generator and Nginx server.
-   `docker-compose.yml`: Defines the web service and the Cloudflare Tunnel.

## Custom Shortcodes

-   `image`: A custom shortcode to automatically generate responsive `<picture>` tags with multiple formats (AVIF, WebP, JPEG).
    -   Usage: `{% image "./path/to/image.jpg", "alt text" %}`

## Analytics

Access logs are stored in the `nginx-logs` directory and can be analyzed using GoAccess, which is configured to output results to the `goaccess-html` directory.
