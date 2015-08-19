OAuth

Access token
a request is send to google - Can i use your Oauth services?
Google will have Apps database with url
CA.com/callback url
Client Secret
Client ID


.env file
Client_Secret = something //this is hidden
CL_ID = APP_123 //can be shown to the outside world

Whena site sends request it sends Client ID
+ Callback URL


Google will create a

When user says agrees the user is redirected to the original website
with User ID

====================================================================
controllers/index.rb

get '/' do
  erb :index
end

(index.erb)


google Web apps
===============
Creating credentials
  create Project
credentials
  Create new Client ID
    fill the form
http://localhost:9393
http://localhost:9393/oauth2callback

> create client ID

> Forming the URL


Copy the example URL

index.erb

<a href = the whole example> Logging in with Google!</a>


get '/gotogoogle' do
  redierect "the whole URL"
end

get '/oauth2callback' do
  body = {
    code: params[:code]
    client_id: "" //copy from google console
    client_secret: ""  //copy from google console
    redirect_uri: "http://localhost:9393/callback"
    grant_type: "authorization_code"// not the actual code but just the text}

  HTTParty.post("token link", body:body)
  p parama

  info = HTTParty.get()

end









