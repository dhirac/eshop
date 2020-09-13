#lauch to server issues
check folder uploaded sucessfully as uploading zip file from ftp also not working. make zip of missing file and upload again.


#put this to make public folder aviliable in public_html
public function register()
{
    $this->app->bind('path.public', function() {
        return realpath(base_path().'/../public_html');
    });
}


#redirect alll traffic to https put in htaccess
RewriteEngine On
RewriteCond %{HTTPS} off
RewriteRule ^(.*)$ https://%{HTTP_HOST}%{REQUEST_URI} [L,R=301]
