run:
	@gunicorn todoapp:app --bind localhost:8080 --worker-class aiohttp.worker.GunicornUVLoopWebWorker -e SIMPLE_SETTINGS=todoapp.settings.development

requirements-test:
	@pip install -r requirements/test.txt

test:
	@SIMPLE_SETTINGS=todoapp.settings.test py.test todoapp

check:
	@flake8
	@isort --check
