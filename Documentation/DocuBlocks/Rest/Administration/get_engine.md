
@startDocuBlock get_engine
@brief returns the engine the type the server is running with

@RESTHEADER{GET /_api/engine, Return server database engine type}

@RESTDESCRIPTION
Returns the storage engine the server is configured to use.
The response is a JSON object with the following attributes:

@RESTRETURNCODES

@RESTRETURNCODE{200}
is returned in all cases.

@RESTREPLYBODY{name,string,required,string}
will be *mmfiles* or *rocksdb*

@EXAMPLES

Return the active storage engine

@EXAMPLE_ARANGOSH_RUN{RestEngine}
    var response = logCurlRequest('GET', '/_api/engine');

    assert(response.code === 200);

    logJsonResponse(response);
@END_EXAMPLE_ARANGOSH_RUN
@endDocuBlock

