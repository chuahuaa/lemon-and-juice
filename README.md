<!DOCTYPE html>
<!--
Follow me!
dribbble.com/gsvineeth
twitter.com/gsvineeth
-->
<html lang="en">
<head>
    <!-- jQuery from CDN -->
<script src="http://ajax.googleapis.com/ajax/libs/jquery/1.9.1/jquery.min.js"></script>
      <script src="js/jribbble.js"></script>
      <script src="js/bootstrap.js"></script>
<script>

$(document).ready(function()
    //Paste your Client Access Token in the line below within quotes - you can build your API from https://dribbble.com/account/applications 
    $.jribbble.setToken('31ab7fc9c25cbe4122efa08d82d5ee0998685a63cd93f0fd763045abb4bbd67d');
    $.jribbble.users('gsvineeth').shots({per_page: 36}).then(function(shots) {
    var html = [];
  
    shots.forEach(function(shot) {
        html.push('<div class="col-sm-6 col-md-4 col-lg-4"> <div class="grid-list">');
        html.push('<a href="' + shot.html_url + '" target="_blank">');
        html.push('<img class="img-responsive" src="' + shot.images.normal + '" alt="' + shot.title + '"><\/a>');
        html.push('<div class="overlay"><a target="_blank"  href="' + shot.html_url + '">');
        html.push('<h2>' + shot.title + '<\/h2>');
        html.push('<\/a> <\/div><\/div><\/div>');
    });
  
    $('#shots').html(html.join(''));
    });
});
 
        </script>
    <meta charset="utf-8">
    <meta content="IE=edge" http-equiv="X-UA-Compatible">
    <meta content="width=device-width, initial-scale=1" name="viewport">
    
    <title>Portfolio Theme by gsvineeth.com </title>
    
    <!-- Bootstrap + Font Awesome + Main CSS -->
    <link href="http://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.2.0/css/font-awesome.min.css" rel="stylesheet">
    <link href="css/bootstrap.css" rel="stylesheet">
    <!-- customize this file if needed -->
    <link href="css/main.css" rel="stylesheet">
    
    <!-- HTML5 Shim and Respond.js IE8 support of HTML5 elements and media queries -->
    <!-- WARNING: Respond.js doesn't work if you view the page via file:// -->
    <!--[if lt IE 9]>
      <script src="https://oss.maxcdn.com/html5shiv/3.7.2/html5shiv.min.js"></script>
      <script src="https://oss.maxcdn.com/respond/1.4.2/respond.min.js"></script>
    <![endif]-->
    
</head>

<body>
    <div class="wrapper">
        <div class="container">
            <header>
                <div class="row">
                    <div class="navbar">
                        <div class="navbar-header">
                            <button class="navbar-toggle collapsed" data-target=".navbar-collapse" data-toggle="collapse" type="button"><span class="sr-only">Toggle navigation</span> <span class="icon-bar"></span> <span class="icon-bar"></span> <span class="icon-bar"></span></button> <a class="navbar-brand" href="#">DRIBBBLEFOLIO</a>
                        </div>

                        <div class="collapse navbar-collapse">
                            <ul class="nav navbar-nav">
                                <li>
                                    <a href="#">About</a>
                                </li>

                                <li>
                                    <a href="#">Blog</a>
                                </li>

                                <li>
                                    <a href="#">Resume</a>
                                </li>

                                <li>
                                    <a href="#">Contact</a>
                                </li>
                            </ul>

                            <ul class="nav navbar-nav social">
                                      <li><a href="#"> <i class="fa fa-facebook"></i> </a></li>
                                      <li><a href="#"> <i class="fa fa-twitter"></i> </a></li>
                                      <li><a href="#"> <i class="fa fa-github"></i> </a> </li>  
                                      <li><a href="#"> <i class="fa fa-linkedin"></i> </a></li>
                                      <li><a href="#"> <i class="fa fa-envelope"></i> </a></li>
                            </ul>
                        </div><!-- /.nav-collapse -->
                    </div><!-- /.navbar -->
                </div>

                <div class="row">
                    <div class="col-md-12 col-lg-12">
                        <h1 class="intro"><span>Hello</span> <span>I’m</span> John Doe <span>, Designer &amp; Coder </span></h1>
                    </div>
                </div>
            </header>

            <div class="row grid-list-wrapper no-gutter-space" id="shots"></div>
         </div>
    </div>

    <footer>
        <div class="container">
            <nav class="nav-footer">
                <ul>
                    <li>
                        <a href="#">About</a>
                    </li>

                    <li>
                        <a href="#">Blog</a>
                    </li>

                    <li>
                        <a href="#">Resume</a>
                    </li>

                    <li>
                        <a href="#">Contact</a>
                    </li>
                </ul>

                                  <ul>
                                      <li><a href="#"> <i class="fa fa-facebook"></i> </a></li>
                                      <li><a href="#"> <i class="fa fa-twitter"></i> </a></li>
                                      <li><a href="#"> <i class="fa fa-github"></i> </a> </li>  
                                      <li><a href="#"> <i class="fa fa-linkedin"></i> </a></li>
                                      <li><a href="#"> <i class="fa fa-envelope"></i> </a></li>
                                  </ul>

                <p class="credits text-center">&copy; All Rights Reserved 2015</p>
            </nav>
        </div>

    </footer>
</body>
</html>
