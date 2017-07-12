http://www.rabbitmq.com/build-server.html


https://github.com/rabbitmq/rabbitmq-server




Building the server

Change to the rabbitmq-server directory, and type make.

Other interesting Makefile targets include

all
The default target. Builds the server.
shell
Builds the client libraries and starts an Erlang shell with the libraries loaded.
run-broker
Builds the server and starts an instance with an interactive Erlang shell. This will by default put data, including a Mnesia database, in /tmp/rabbitmq-test-instances, but this location can be overridden by setting the Makefile variable TEST_TMPDIR:
make run-broker TEST_TMPDIR=/some/other/location/for/rabbitmq-test-instances
clean
Removes temporary build products.
distclean
Removes all build products, including fetched dependencies.
tests
Runs a set of tests.













