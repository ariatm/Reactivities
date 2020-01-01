#install chocolatey (in order to install nvm-windows)
Set-ExecutionPolicy Bypass -Scope Process -Force; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))

#install NVM-Windows
# choose desired node version
$version = "8.12.0"
# install nvm w/ cmder
choco install cmder
choco install nvm
refreshenv
# install node
nvm install $version
nvm use $version

#installing react-app
npx create-react-app client-app --use-npm --typescript

#react dev tool
React Developer Tools for chrome/firefox by facebook (v4+)

#install axios as http-client inside "client-app"
npm install axios

#install Semantic UI React inside "client-app"
npm install semantic-ui-react

#add Semantic UI React CSS link to public\index.html
<link rel="stylesheet" href="//cdn.jsdelivr.net/npm/semantic-ui@2.4.2/dist/semantic.min.css" />

#install react-widgets & date
npm install react-widgets react-widgets-date-fns

#install date-fns according to the required version
npm install date-fns@2.0.0-alpha.13

#install revalidate
npm install revalidate

#create new class library for netcore
dotnet new classlib -n Infrastructure

#adding new class library to the solution
dotnet sln add Infrastructure

#adding dependency to the project
cd Infrastructure
dotnet add reference ../Application/
cd API
dotnet add reference ../Infrastructure/

#save key to user store (only for development)
dotnet user-secrets set "TokenKey" "super secret key" -p API
