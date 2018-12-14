# AJAX based Contact Form with PHP and Email responder

This project contains a simple php-based ajax contact form with email autoresponder.

This project served as an addtion to the website created for wiregalaxy-based clients.  

# Table of Contents

- [Features](#features)
- [Requirements](#requirements)
- [Setup](#setup)
- [Usage](#usage)
- [License](#license)
- [Credits](#credits)


## Features

- A configurable script for doing as mentioned above.

## Requirements

1. Generic web server with PHP installed.

## Setup

Open a terminal window and execute one of the following setup sequences :

Install the required software packages:

    sudo apt install zip

Download the contents to your desired path:

    sudo git clone https://github.com/muzikmyth/ajax-contact-php.git
    cd ajax-contact-php
    sudo unzip upload.zip

Alternatively,
    
    sudo wget https://github.com/muzikmyth/ajax-contact-php/raw/master/upload.zip
    sudo unzip upload.zip

## Usage

1. `ssh` to your server or VM.
2. Navigate to extracted folder.
3. Open config.php in your favourite editor and edit the following entries as per your records:
    
        <?php

            // Database server details
            define('DB_HOST', 'localhost'); 
            define('DB_PASSWORD', '');
            define('DB_NAME', 'contact-form');



            //Email layout and options related details
            define('CF_HOST', 'smtp.gmail.com');//your email host here
            define('CF_USERNAME', 'user');//your email here
            define('CF_PASSWORD', 'password');//your password here
            define('CF_SECURE', 'tls');
            define('CF_PORT', '587');
            define('CF_ADDCC', 'cc@example.com');
            define('CF_ADDBCC', 'bcc@example.com');

            define('CF_EMAIL_FROM', 'abk@abhijitkrm.site'); 
            define('CF_EMAIL_FROM_NAME', 'Abhijit Kumar'); //email from
            define('CF_EMAIL_REPLYTO', 'abk@abhijitkrm.site');//email that receive email when use click on reply to
            define('CF_EMAIL_REPLYTO_NAME', 'Abhijit Kumar');
            define('CF_EMAIL_CC', '');        //cc email
            define('CF_EMAIL_BCC', '');        //bcc email
            define('CF_CLIENT_EMAIL_TITLE',"Thank you for contacting us!");
            define('CF_CLIENT_EMAIL_END_MESSAGE',"We will reply your contact ASAP.");
            define('CF_ADMIN_EMAIL_TITLE',"New Contacting Email!");

            //sitekey captcha google for your website
            define('CF_RECAPTCHA',true);//enable google recaptcha
            define('CF_RECAPTCHA_KEY', '6Lc93s8SAAAAAHfqBv-DoE1XSAcFMKYHGk0YBEYV');//'Your generated Key'


        ?>
4. Open database/information.sql and edit the following entries:

            INSERT INTO `information` (`id`, `name`, `email`, `subject`, `message`, `gender`, `file_upload`) VALUES (1, 'abk', 'abk@abhijitkrm.site', 'Select one', 'e', 'male', '');

5. Now you can use index.php and index-dev.php to use the application.


## License

MIT License. Read [LICENSE](LICENSE.md) for details.


## Credits

Developed by [Abhijit Kumar](http://abhijitkrm.site) at Wiregalaxy @ 2016.
