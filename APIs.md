API's

### What is an API
developer.github.com/V3

from the terminal
```
curl -v https://api.github.com
```

- curl - command line URL


### What a Web API

### Consume a Web API

require 'httparty'
get '/' do
  <!-- #make a request to github -->
  headers: {"User-Agent" => "peeper rams"}
  emojis_response= HTTParty.get("https://api.github.com/emojis", headers: headers)
  p emojis_response
end
```
posts '/gists'
  headers: {"User-Agent" => "peeper rams",
            "Authorization" => "token"}
  json_body = {
    description: "the description for this gist"
    public: true,
    files: {
      "file1.txt" => {content: "Hello, i did a api request"}
          }
  gist_response = HTTParty.get("https://api.github.com/gists", headers: headers)
}
  p gist_response
end
```
<%=  %>



Views
<% emojis_response.each do |key, url|%>
 <img src=<%=url%>/>
<% end %>

RACK::Lint

A linter is checks the syntax.
Rack is between sinatra and webswerver


looked for the parsed_response

Building an API

endpoints(urls)
  - RESTful
  - convention
  - easier to reason about
  - predictable

headers (meta information, user-agent, authorization, ratelimit, content-type)
- versioning
- heasers
documentation
respond with a format that developers can use.
- to_json
respond with a sensible status code.
- 200, 201

HATEOAS
Hypertext as the engine of application state
Pseudobook steve kloznik

create a file called sinatra.rb
build a restful route called api/v1/games
in that route, i'll select the games
return the games in JSAON format
content type json











