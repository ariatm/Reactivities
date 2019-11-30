#install chocolatey
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
