# :star2: Yaml to Json Converter
     Used yml2json module to convert Yaml file to Json file
## Example:
      yml2json input.yml -o input.json
## Input:
```sh
    version: '1.0'

  steps:
  build-prj:
    type: build
    image-name: codefreshio/image1
    dockerfile: Dockerfile
    tag: latest

  clone-prj2:
    type: git-clone
    repo: https://github.com/{repoOwner}/{repoName}.git

  build-prj2:
    type: build
    image-name: codefreshio/image2
    dockerfile: Dockerfile
    tag: latest
    working-directory: ${{clone-prj2}}
 ```
  ## Output:
  ```sh
    {
	"version": "1.0",
	"steps": {
		"build-prj": {
			"type": "build",
			"image-name": "codefreshio/image1",
			"dockerfile": "Dockerfile",
			"tag": "latest"
		},
		"clone-prj2": {
			"type": "git-clone",
			"repo": "https://github.com/{repoOwner}/{repoName}.git"
		},
		"build-prj2": {
			"type": "build",
			"image-name": "codefreshio/image2",
			"dockerfile": "Dockerfile",
			"tag": "latest",
			"working-directory": "${{clone-prj2}}"
		}
	}
}
  ```
