 Phase 2 Week1 Day 4
  We don't want to use just [Params] for security reasons.
  #put
  @article.assign_attribute - Articles will saved temp and need a save to be saved. This gives time for validation.

  What are the actions which trigger validationd
  search for active record validation. Read the commands which skip the validations also.

Helpers method are created under app/helpers folder.

Config/environment.rb #All files will be included here

sinatrarb.com/intro.html

Check this...
  !!session[:user_id] or !session[:user_id].nil?

def login(user)
  session[:user_id] = user
end

Any file starting with _ (_form_fields.erb)is a partials file
and include partial file in your code like below:

<%= erb :"articles/_fields"%>





