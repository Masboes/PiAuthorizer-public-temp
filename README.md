# Pandora Intelligence FastApi authorization


## Usecases

The package deals with authorization, uniform autorest support and some stresstesting.\

from PIauthorizer import get_dependencies\
gets list of basic Flask authorization dependencies.\

from PIauthorizer import override\
can be used to override authorization dependencies within test set-up.\

from PIauthorizer import format_operation_ids\
needs to be added at the end of the main.py format_operation_ids(app) ensures that the openapi.json is rendered correctly.\

from PIauthorizer import create_autorest_schema\
needs to be added at the end of the main.py create_autorest_schema(app) ensures that the openapi.json is created when building the app. Note that it should be added afterformat_operation_ids(app).\

from PIauthorizer import Stresstester\
this class van be used to stresstest an API. Initialize with a host_url. run test via run_test(self, endpoint: str, params: dict, request_type: str = 'GET').\

 