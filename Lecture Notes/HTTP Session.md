HTTP Session
Doughlus Crawford Videos for about Web History

enable :sessions

get '/foo' do
  session[:message] = "Hello World"
  redirect to ('/bar')
end

get '/bar' do
  session[:message] #=> "Hello World"
end

===========================

get '/' do
  session[:user_name] = "Number 6"
  "Welcome"
end

get '/test' do
  if session[:user_name]
    return "Thanks for visiting us again You are #{session.user_id}"
  else
    "Welcome to "
  end
end

===============================================

environment.rb session_secret

How do we use to manage our users?
==================================================

Common RESTful routes for Users

# for showing login and signup forms
get





