# Portainer Templates

Custom container templates for Portainer CE.

## Templates

### GPU Templates

| Template | GPUs | RAM | Description |
|----------|------|-----|-------------|
| GPU Server 1x | 1 | 64GB | LLM training and inference with PyTorch |
| GPU Server 2x | 2 | 128GB | Multi-GPU training with Axolotl |
| GPU Server 3x | 3 | 192GB | Multi-GPU training with DeepSpeed |
| GPU Server 4x | 4 | 256GB | Full multi-GPU training with vLLM |

### Web Templates

| Template | CPU | RAM | Description |
|----------|-----|-----|-------------|
| Web Server Small | 1 | 1GB | Basic web hosting with PHP and Node.js |
| Web Server Medium | 2 | 4GB | Standard web hosting with PHP, Node.js, and Composer |
| Web Server Large | 4 | 16GB | High-performance web hosting with Redis and Imagick |
| Web Server XLarge | 8 | 64GB | Enterprise web hosting |
| Web Server XXLarge | 16 | 100GB | Maximum performance web hosting |

## Usage

### Portainer Setup

1. Access Portainer at http://your-server:9000
2. Go to **Settings** → **App Templates**
3. Enter the URL:
   ```
   https://raw.githubusercontent.com/YOUR_USERNAME/portainer-templates/main/templates.json
   ```
4. Save and navigate to **App Templates**

### Deploying a Template

1. Select a template from the list
2. Fill in the required variables:
   - `username` - Username for SSH access
   - `password` - Password for user account
   - `ssh_port` - SSH port (auto-assigned if empty)
3. Click **Deploy**

## Storage

- GPU templates use `/data1/<username>`
- Web templates use `/data2/<username>`

## Requirements

- Docker with NVIDIA GPU support (for GPU templates)
- Portainer CE 2.0+

## License

MIT
