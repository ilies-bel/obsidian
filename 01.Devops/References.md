doc references : https://docs.gitlab.com/ee/ci/yaml/index.html


## Heritage 
	https://docs.gitlab.com/ee/ci/jobs/#hide-jobs

On peut cacher un job avec un . devant pour ensuite le réutiliser avec une yaml anchore ou le keyword extends.

- extends est conseillé, permet les references externes avec **include**
- anchore permet de merge des arrays sans ecraser  

## Configuration
Configurer le runner pour tenter le pull 2 fois 
https://docs.gitlab.com/runner/executors/docker.html#retrying-a-failed-pull