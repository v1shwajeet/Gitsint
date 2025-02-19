# GitSint Dockerized

This repository contains a Docker setup for running [GitSint](https://github.com/v1shwajeet/GitSint), an OSINT tool for investigating GitHub users. The Docker container ensures all dependencies are installed and allows running the tool without setting up a virtual environment manually.

## Prerequisites

- [Docker](https://www.docker.com/get-started) installed on your system.

## Build the Docker Image

Clone the repository and navigate to the project directory:

```sh
# Clone the repository
git clone https://github.com/N0rz3/GitSint.git
cd GitSint
```

Build the Docker image:

```sh
docker build -t gitsint .
```

## Run GitSint in Docker

Run the container with your desired GitHub username:

```sh
docker run --rm gitsint -u YOUR_GITHUB_USERNAME
```

Replace `YOUR_GITHUB_USERNAME` with the GitHub username you want to investigate.

## Customize the Command

You can pass additional arguments to GitSint as needed:

```sh
docker run --rm gitsint -u YOUR_GITHUB_USERNAME -o output.txt
```

This will save the results to `output.txt`.

## Notes

- The `--rm` flag removes the container after execution to keep your system clean.
- The image includes all required dependencies, so no additional setup is needed.

## Troubleshooting

If you encounter issues:

1. Ensure Docker is installed and running.
2. Check that the `requirements.txt` file exists and is correctly formatted.
3. Rebuild the image if dependencies have changed:
   ```sh
   docker build --no-cache -t gitsint .
   ```

## License

This project follows the [GitSint](https://github.com/N0rz3/GitSint) license. Ensure you comply with its terms when using this tool.

