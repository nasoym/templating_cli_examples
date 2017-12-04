# templating_cli_examples

## mustache
* info: <https://mustache.github.io/>
* install: `npm install mustache -g`
* example: `mustache <(echo '{"foo":[{"name":"bar"},{"name":"foo"}]}') <(echo "foo {{#foo}} -{{name}} {{/foo}}")`
* example: `mustache <(echo '{"foo":[1,2,2,3]}') <(echo "foo {{#foo}} -{{.}} {{/foo}}")`
* example: `mustache <(echo '{"foo":"bar"}') <(echo "foo {{foo}}")`
* example: `mustache <(echo '{"foo":{"name":"bar"}}') <(echo "foo {{foo.name}}")`

## ninja2
* info: <http://jinja.pocoo.org/docs/2.10/>
* install: `pip2.7 install j2cli`
* example: `echo '{"foo":[{"name":"bar"},{"name":"foo"}]}' | j2 -f json <(echo "foo {% for i in foo%} -{{i.name}} {% endfor %}")`
* example: `echo '{"foo":[1,2,2,3]}' | j2 -f json <(echo "foo {% for i in foo%} -{{i}} {% endfor %}")`
* example: `echo '{"foo":"bar"}' | j2 -f json <(echo "foo: {{foo}}")`
* example: `echo '{"foo":{"name":"bar"}}' | j2 -f json <(echo "foo: {{foo.name}}")`
* example: `j2 -f json <(echo "foo: {{foo.name}}") <(echo '{"foo":{"name":"bar"}}')`




