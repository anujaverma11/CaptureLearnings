## How to kill a host session running in background?
ps ax | grep ruby
kill -9 225



=======================================================================
#### Helpers and Partials
Helpers can be built in Helper and custom helpers

helpers A, B
ERB FILE
```
<%= erb :_table, locals:{items: %w[a b c d e], name: "letters"}
 %>
```

```
This is a list of <%= letters %>
 Partial _table.erb
<% items.each do |x| %>
  <%= x %>
<% end %>
```
=======================================================================

#### Include module vs Exclude module
In modules
include a module in class is like copy pasted the methods of module inside class.

exclude a module in class is like copy pasted the methods with 'self' statement so that they can be used as class methods.

class One
include module
  <!-- def x
  end

  def y
  end -->
end

o = One.new
o.x


class Two
exclude module
 <!-- self.x
  end

  def self.y
  end -->
end

Two.x

=======================================================================



Ashton and Daniela - RSPEC tests
Derek Ryan emalio - timer time
Andreas Robert Travis - Spritely.net / flatuicolors.com / colour lovers.com
Tom, Alex, Lorraine - NAvigation bar - See how the radio button worked

be shotgun -p 9494
to change the port
mkdir: test
paperclip gem

~~~~~~~~~~~~~For changing ruby versions~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
rbenv versions
rbenv install 2.1.0
rbenv global 2.1.0

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Ruby Rack -http://rack.github.io/
  include gem rack
Sinatra is an application, Webrick is the webserver

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Pizza.all.limit(2).to_sql
Pizza.all.order(:price_cents => :asc)

activerecord validation errors - work on this today
Activerecords querying the database - work on this today
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
### 7 routes
  index
  show
  new
  create
  edit
  update
  destroy

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
### Nested Routing
is a kind of routing which works with associations where routes are nested.

Article.all
@category = Category.find(params[:category_id])
@article = @category.articles.find(params[:id])

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Martin fowler - Refactoring Book



describe "index controller" do
  describe "GET/articles" do
    it "responds with ok status" do
      # given
      #   these things
      #   that this world exists
      # when
      #   this thing happends
      get '/articles'
      # then
      #   this should have happened
      expect(last_response.status).to eq(200)
    end

    it "responds with ok status" do
      # given
      Article.create(title:"I <3 Tinder Pizza")
      # when
      get '/articles'
      # then
      expect(last_response.status.body).to include("I <3 Tinder Pizza")
    end
  end

  describe "post/articles" do
    it "responds with successful status" do
      # given
      #   these things
      #   that this world exists
      # when
      #   this thing happends
      post '/articles'
      # then
      #   this should have happened
      expect(last_response.status).to eq(200)
    end

    it "creates an article" do
      # given
      count_before = Article.count
      # when
      post '/articles', title: "My new article!"
      # then
      count_after = Article.count
      expect(count_before).to_not eq(count_after)
    end
  end
end

-----------------------------------------------
gem better errors
def auth_logged_in?
  session[id]
end


#### Self Referential joins














