run:
	@gunicorn todo-app:app --bind localhost:8080 --worker-class aiohttp.worker.GunicornUVLoopWebWorker -e SIMPLE_SETTINGS=todo-app.settings.development

requirements-test:
	@pip install -r requirements/test.txt

test:
	@SIMPLE_SETTINGS=todo-app.settings.test py.test todo-app

check:
	@flake8
	@isort --check
