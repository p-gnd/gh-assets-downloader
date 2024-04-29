# Makefile
## Testing

### run unit-tests with pytest
`unit-tests `
	
### run unit-tests with pytest and show coverage (terminal + html)
`unit-tests-cov `

### run unit tests with pytest and show coverage (terminal + html) & fail if coverage too low & create files for CI
`unit-tests-cov-fail`


## Formatting
### run black (code formatter)
`format-black`
### run isort (imports formatter)
`format-isort`
### run all formatters
`format: format-black format-isort`

## Linting
### run black in linting mode
`lint-black` 
	
### run isort in linting mode
`lint-isort`
	
### run flake8 (code linter)
`lint-flake8`
	
### run mypy (static-type checker)
`lint-mypy`
	
### run mypy & create report
`lint-mypy-report`
	

### run all linters
`lint`


## Documentation
### build documentation locally
`docs-build`

### build & deploy documentation to "gh-pages" branch
`docs-deploy` 

### create openapi.json
`create_openapi` 

## Clean-up
### remove output files from pytest & coverage
`clean-cov` 
### remove output files from mkdocs
`clean-docs` 
	
### run all clean commands
`clean` 

## Releases
### returns the current version
`current-version`
### returns the next version
`next-version`
### returns the current changelog
`current-changelog`
### returns the next changelog
`next-changelog`

### publish command (noop="no operation mode")
`publish-noop`

## Docker
### docker build
`build` 
### docker run app
`run` 
### docker run with bash
`run-bash` 
### login to ghcr.io using a personal access token (PAT)
`login` 
### tag docker image to ghcr.io/RobertoFioravanti/project:latest
`tag` 
### docker push to container registry (ghcr.io)
`push` 
### scan the docker image for vulnerabilities
`scan`