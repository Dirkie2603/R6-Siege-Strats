# R6-Siege-Strats
Strats for R6 Siege


<!DOCTYPE html>
<html>
<head>
    <title>R6 Strats - Real-time Tactics</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <meta name="description" content="Tacnet is a tool that lets teams construct tactics in real-time, without any registration or installation.">
    <meta name="keywords" content="Tacnet,tacticsharing,bf3,bf4,csgo,cod,lol,dota2,tactics live,collaborate,atc">
    <link rel="shortcut icon" href="/static/img/favicon.ico">
    <!-- Bootstrap -->
    
        <!-- CDN -->
        <link href="//netdna.bootstrapcdn.com/bootstrap/3.0.3/css/bootstrap.min.css" rel="stylesheet">
        <script src="//ajax.googleapis.com/ajax/libs/jquery/2.0.3/jquery.min.js"></script>
        <script src="//netdna.bootstrapcdn.com/bootstrap/3.0.0/js/bootstrap.min.js"></script>
    
    <link href="//netdna.bootstrapcdn.com/font-awesome/4.0.3/css/font-awesome.css" rel="stylesheet">
    <link href="/static/css/bootstrap-darkstrap.css" rel="stylesheet">
    <link rel="stylesheet" href="/static/css/main.css">
    <link rel="stylesheet" href="/static/css/auth_bar.css">

    <!--JS-->
    <script type='text/javascript'>
        $(document).ready(function () {
            if ($("[rel=tooltip]").length) {
                $("[rel=tooltip]").tooltip();
            }
        });
    </script>
    <!--[if lt IE 9]>
      <script src="https://oss.maxcdn.com/libs/html5shiv/3.7.0/html5shiv.js"></script>
      <script src="https://oss.maxcdn.com/libs/respond.js/1.3.0/respond.min.js"></script>
    <![endif]-->
</head>
<body>

<div id="auth_bar">

    <div class="container">

        <div class="row">
            <div class="col-xs-12 text-right text-holder">

                <a class="menu" style="display: none;" id="login-button" href="#"><span class="glyphicon glyphicon-log-in"></span> Login</a>
                <a class="menu" style="display: none;" id="user" href="#"><span class="glyphicon glyphicon-user"></span> <span id="user_usename"></span></a>
                <a class="menu" style="display: none;" id="logout-button" href="#"><span class="glyphicon glyphicon-log-out"></span> Logout</a>


                <div class="well" id="form-holder" style="display: none;">


                    <div class="login-form-holder">
                        <form method="POST" action="#" id="login-form" class="form-inline"><input type='hidden' name='csrfmiddlewaretoken' value='GbWbCo8skOLbWq5nFJ40ea8ozr22Kl5U' />

                            <div class="text-left">
                                <div id="allFields" class="alert alert-warning" style="display: none;">
                                  <strong>Warning!</strong> All fields are required.
                                </div>

                                <div id="progress" class="alert alert-info" style="display: none;">
                                  <strong>Information!</strong> Connecting to service...
                                </div>

                                <div id="error" class="alert alert-danger" style="display: none;">
                                  <strong>Error!</strong> Couldn't log in, please try again.
                                </div>
                            </div>

                            <div class="form-group">
                                <input name="username" class="form-control" type="text" placeholder="Username">
                            </div>
                            <div class="form-group">
                                <input name="password" class="form-control" type="password" placeholder="Password">
                            </div>


                           <div class="login-modal-text text-left">
                               <a href="#" class="register-user-link btn btn-primary"><span class="glyphicon glyphicon-user"></span> Register</a>
                               <a href="#" class="forgot-user-link btn btn-primary"><span class="glyphicon glyphicon-link"></span> Forgot Password</a>
                           </div>
                            <div class="buttons text-right login-modal-buttons">
                                <button type="submit" id="login-now" class="btn btn-success"><span class="glyphicon glyphicon-log-in"></span> Login</button>
                            </div>

                        </form>
                    </div>

                  <div class="register-form-holder">
                      <form method="POST" action="#" id="register-form" class="form-inline"><input type='hidden' name='csrfmiddlewaretoken' value='GbWbCo8skOLbWq5nFJ40ea8ozr22Kl5U' />

                            <div class="text-left">
                                <div id="register-allFields" class="alert alert-warning" style="display: none;">
                                  <strong>Warning!</strong> Username and password are required.
                                </div>

                                <div id="register-progress" class="alert alert-info" style="display: none;">
                                  <strong>Information!</strong> Connecting to service...
                                </div>

                                <div id="register-error" class="alert alert-danger" style="display: none;">
                                  <strong>Error!</strong> Couldn't register, please try again.
                                </div>
                            </div>

                            <div class="form-group">
                                <input name="register-username" class="form-control" type="text" placeholder="Username">
                            </div>
                            <div class="form-group">
                                <input name="register-password" class="form-control" type="password" placeholder="Password">
                            </div>

                            <div class="form-group">
                                <input name="register-retypepassword" class="form-control" type="password" placeholder="Retype Password">
                            </div>

                            <div class="form-group">
                                <input name="register-mail" class="form-control" type="text" placeholder="Mail (Optional)">
                            </div>


                           <div class="login-modal-text text-left">
                               <a href="#" class="register-user-login-link btn btn-primary"><span class="glyphicon glyphicon-log-in"></span> Login</a>
                           </div>
                            <div class="buttons text-right login-modal-buttons">
                                <button type="submit" id="register-now" class="btn btn-success"><span class="glyphicon glyphicon-log-in"></span> Register</button>
                            </div>


                      </form>
                  </div>


                    <div class="forgot-form-holder">
                      <form method="POST" action="#" id="forgot-form" class="form-inline"><input type='hidden' name='csrfmiddlewaretoken' value='GbWbCo8skOLbWq5nFJ40ea8ozr22Kl5U' />

                            <div class="text-left">
                                <div id="forgot-allFields" class="alert alert-warning" style="display: none;">
                                  <strong>Warning!</strong> Mail are required.
                                </div>

                                <div id="forgot-progress" class="alert alert-info" style="display: none;">
                                  <strong>Information!</strong> Connecting to service...
                                </div>

                                <div id="forgot-error" class="alert alert-danger" style="display: none;">
                                  <strong>Error!</strong> Couldn't recover user, please try again.
                                </div>
                            </div>

                            <div class="form-group">
                                <input name="forgot-mail" class="form-control" type="text" placeholder="Mail">
                            </div>


                           <div class="login-modal-text text-left">
                               <a href="#" class="register-user-login-link btn btn-primary"><span class="glyphicon glyphicon-log-in"></span> Login</a>
                           </div>
                            <div class="buttons text-right login-modal-buttons">
                                <button type="submit" id="forgot-now" class="btn btn-success"><span class="glyphicon glyphicon-link"></span> Recover</button>
                            </div>


                      </form>
                  </div>





                </div>




            </div>

        </div>

    </div>

</div>


<div id="body_content">

    

    <!--Loading layer-->
    <div id="loading_layer"></div>
    <script src="/static/js/spin.js"></script>
    <script type="text/javascript">
        var loggedIn = "";
    </script>
    <link rel="stylesheet" href="/static/js/loading_layer/loading.css">
    <script type="text/javascript" src="/static/js/loading_layer/loading.js"></script>

    <link rel="stylesheet" href="/static/css/dock.css">

    <script type="text/javascript"> 
        var csrf_token = "GbWbCo8skOLbWq5nFJ40ea8ozr22Kl5U";
    </script>




    <div class="container">
        <nav class="navbar navbar-default" role="navigation">
            <!-- Brand and toggle get grouped for better mobile display -->
            <div class="navbar-header">
                <button type="button" class="navbar-toggle" data-toggle="collapse" data-target="#bs-example-navbar-collapse-1">
                    <span class="sr-only">Toggle navigation</span>
                    <span class="icon-bar"></span>
                    <span class="icon-bar"></span>
                    <span class="icon-bar"></span>
                </button>
                <a class="navbar-brand" href="/"><span class="glyphicon glyphicon-eye-open"></span> Tacnet.io</a>
            </div>

            <div class="collapse navbar-collapse" id="bs-example-navbar-collapse-1">
                <ul class="nav navbar-nav">
                    <li class="visible-xs visible-lg"><a href="/"><span class="glyphicon glyphicon-home"></span> Home</a></li>
                    <li class="visible-xs visible-lg"><a href="/frontpage/about"><span class="glyphicon glyphicon-info-sign"></span> About</a></li>
                    <li class="visible-xs visible-lg"><a class="contact" href="#"><span class="glyphicon glyphicon-envelope"></span> Feedback</a></li>
                </ul>
                <ul class="nav navbar-nav navbar-right">
                    

    <li id="chooseBrush" data-original-title="Select Brush"><a href="#"><span class="glyphicon glyphicon-pencil"></span> Select Brush</a></li>
    <div id="chooseBrush_content_wrapper" style="display: none;">
         <div class="form-group" style="height: 46px; margin-bottom: 5px;">
            <div id="brushSizeForm">
                <label for="brushSize">Brush Size</label><br>
            </div>
            <div id="setAlphaForm">
                <label for="setAlpha">Opacity</label><br>
            </div>
          </div>

        <div class="btn-group btn-group-justified" style="width: 438px;">
            <a class="btn btn-success green-pick brush">Green</a>
            <a class="btn btn-warning yellow-pick brush">Yellow</a>
            <a class="btn btn-danger red-pick brush">Red</a>
            <a class="btn btn-info blue-pick brush">Blue</a>
            <a class="btn btn-inverse black-pick brush">Black</a>
        </div>

        <div class="btn-group btn-group-justified" style="width: 438px; margin-top: 10px;">
            <a class="btn btn-primary user-color-pick brush">User Color</a>
            <a class="btn btn-default eraser brush"><i class="fa fa-eraser"></i></a>
            <a class="btn btn-primary toggleTrailing"><i class="fa fa-chain"></i> Icon Trailing</a>
        </div>
    </div>
</li>

<li id="clearMenu" data-original-title="Clear"><a href="#"><span class="glyphicon glyphicon-remove-sign"></span> Clear</a></li>
 <div id="clearMenu_content_wrapper" style="display: none">
    <button class="btn btn-default clearCanvas" style="width: 360px;">Clear Drawings</button>

    <div class="btn-group btn-group-justified" style="width: 360px; margin-top: 10px;">
        <a class="btn btn-warning resetFabric">Reset Icons</a>
        <a class="btn btn-danger resetBackground">Reset Background</a>
    </div>

    </div>
</li>

<li class="undo"><a href="#"><i class="fa fa-undo"></i> Undo</a></li>
<li class="redo"><a href="#"><i class="fa fa-repeat"></i> Redo</a></li>
<li class="deleteIcon"><a href="#"><span class="glyphicon glyphicon-trash"></span> Delete</a></li>


                </ul>
            </div>
        </nav>
    </div>

    

    <!--JS alert-->
    <noscript>
    <div class="container">
        <div class="alert alert-danger" style="color: darkred !important;">
            <strong>Error!</strong> This website relies on javascript. Please enable javascript in your browser.
        </div>
    </div>
    </noscript>


    <!-- Mobile user --->
    <div class="container mobile-show">
        <div class="alert alert-warning" style="color: #000000 !important;">
            <strong>Warning!</strong> Tacnet does not currently support mobile devices. The sketch site is disabled.
        </div>
    </div>

    <div class="container messages-container">
        
    </div>


    <div class="modal fade" id="contactModal" tabindex="-1" role="dialog" aria-labelledby="contact" aria-hidden="true">
        <div class="modal-dialog">
            <div class="modal-content">
                <form id="ContactForm" action="/frontpage/contact/" method="post" role="form">
                    <input type='hidden' name='csrfmiddlewaretoken' value='GbWbCo8skOLbWq5nFJ40ea8ozr22Kl5U' />

                    <div class="modal-header">
                        <button type="button" class="close" data-dismiss="modal" aria-hidden="true">&times;</button>
                        <h4 class="modal-title" id="myModalLabel"><span class="glyphicon glyphicon-envelope"></span> Contact</h4>
                    </div>
                    <div class="modal-body">

                        <div class="alert alert-success contactformSuccess" style="display: none;">
                            <strong>Success!</strong> We received your message.
                        </div>

                        <div class="alert alert-warning contactformWarning" style="display: none;">
                            <strong>Warning!</strong> Couldn't send the message, please give all the fields a value.
                        </div>

                        <div id="contactFormContainer">
                            

<div id="div_id_email" class="form-group"> <label for="id_email" class="control-label  requiredField">
                Email<span class="asteriskField">*</span> </label> <div class="controls "> <input class="textinput textInput form-control" id="id_email" name="email" type="text" /> </div> </div> <div id="div_id_message" class="form-group"> <label for="id_message" class="control-label  requiredField">
                Message<span class="asteriskField">*</span> </label> <div class="controls "> <textarea class="textarea form-control" cols="40" id="id_message" name="message" rows="10"></textarea> </div> </div> <div id="div_id_captcha" class="form-group"> <label for="id_captcha" class="control-label  requiredField">
                Captcha<span class="asteriskField">*</span> </label> <div class="controls "> <script src='https://www.google.com/recaptcha/api.js?hl=en'></script>
<div class="g-recaptcha" data-sitekey="6LeZThYUAAAAACitNUGFa0S3gphfg5G-rWTWouSG" ></div>
<noscript> <div style="width: 302px; height: 352px;"> <div style="width: 302px; height: 352px; position: relative;"> <div style="width: 302px; height: 352px; position: absolute;"> <iframe src="https://www.google.com/recaptcha/api/fallback?k=6LeZThYUAAAAACitNUGFa0S3gphfg5G-rWTWouSG"
                frameborder="0" scrolling="no"
                style="width: 302px; height:352px; border-style: none;"> </iframe> </div> <div style="width: 250px; height: 80px; position: absolute; border-style: none;
                  bottom: 21px; left: 25px; margin: 0px; padding: 0px; right: 25px;"> <textarea id="g-recaptcha-response" name="g-recaptcha-response"
                  class="recaptcha_challenge_field"
                  style="width: 250px; height: 80px; border: 1px solid #c1c1c1;
                         margin: 0px; padding: 0px; resize: none;" value=""> </textarea> <input type='hidden' name='recaptcha_response_field' value='manual_challenge' /> </div> </div> </div>
</noscript> </div> </div>

                        </div>

                    </div>
                    <div class="modal-footer">
                        <button type="button" class="btn btn-default" data-dismiss="modal">Close</button>
                        <button type="button" class="btn btn-primary submitContactForm">Send</button>
                    </div>
                </form>
            </div>
        </div>
    </div>


    
    <div class="container">
        <canvas id="background" style="z-index: -1 !important;"></canvas>
        <canvas id="fabric" style="z-index: 1 !important;"></canvas>
        <canvas id="sketch" style="z-index: 0 !important; border: 1px solid grey;"></canvas>
    </div>


    
    <div id="opt-archeage" style="display: none;">
        <option></option>
        
            <optgroup label="Auroria PvP">
                
                    <option value="/media/maps/Calmlands.jpg|223">Calmlands</option>
                
                    <option value="/media/maps/exeloch.jpg|224">Exeloch</option>
                
                    <option value="/media/maps/Heedmar.jpg|225">Heedmar</option>
                
                    <option value="/media/maps/Marcala.jpg|226">Marcala</option>
                
                    <option value="/media/maps/Nuimari.jpg|227">Numiari</option>
                
            </optgroup>
        
    </div>

    <div id="opt-arma-3" style="display: none;">
        <option></option>
        
            <optgroup label="Arma 3">
                
                    <option value="/media/maps/Altis_map.png|300">Altis</option>
                
            </optgroup>
        
    </div>

    <div id="opt-battalion-1944" style="display: none;">
        <option></option>
        
            <optgroup label="Battalion 1944">
                
                    <option value="/media/maps/aimmap.png|301">AimMap_01</option>
                
                    <option value="/media/maps/battery.png|303">Battery</option>
                
                    <option value="/media/maps/coastal.png|302">Coastal</option>
                
                    <option value="/media/maps/derailed.png|304">Derailed</option>
                
                    <option value="/media/maps/liberation.png|305">Liberation</option>
                
                    <option value="/media/maps/manorhouse_v1.png|306">Manorhouse__V1</option>
                
                    <option value="/media/maps/manorhouse_v2.png|307">Manorhouse_V2</option>
                
                    <option value="/media/maps/output.png|308">Output</option>
                
            </optgroup>
        
    </div>

    <div id="opt-battlefield-4" style="display: none;">
        <option></option>
        
            <optgroup label="Conquest">
                
                    <option value="/media/maps/Dawnbreaker_C.jpg|11">Dawnbreaker</option>
                
                    <option value="/media/maps/Flood_Zone_1.jpg|12">Flood Zone</option>
                
                    <option value="/media/maps/Golmund_Railway_C.jpg|13">Golmud Railway</option>
                
                    <option value="/media/maps/original.jpg|149">Guilin Peaks</option>
                
                    <option value="/media/maps/hainan_resort_conquest_small.jpg|209">Hainan Resort</option>
                
                    <option value="/media/maps/Lancang_Dam.jpg|14">Lancang Dam</option>
                
                    <option value="/media/maps/Operation_Locker.jpg|15">Operation Locker</option>
                
                    <option value="/media/maps/Paracel_Storm_C.jpg|16">Paracel Storm</option>
                
                    <option value="/media/maps/Rogue_Transmission_C.jpg|17">Rogue Transmission</option>
                
                    <option value="/media/maps/Siege_of_Shanghai_C.jpg|18">Siege of Shanghai</option>
                
                    <option value="/media/maps/Zavod_311.jpg|19">Zavod 311</option>
                
            </optgroup>
        
            <optgroup label="Domination">
                
                    <option value="/media/maps/Dawnbreaker_Dom_1.jpg|1">Dawnbreaker</option>
                
                    <option value="/media/maps/Flood_Zone_D.jpg|2">Flood Zone</option>
                
                    <option value="/media/maps/Golmund_Railway_D_1.jpg|3">Golmud Railway</option>
                
                    <option value="/media/maps/Hainan_Resort_D_1.jpg|4">Hainan Resort</option>
                
                    <option value="/media/maps/Lancang_Dam_D_1.jpg|5">Lancang Dam</option>
                
                    <option value="/media/maps/Operation_Locker_D_1.jpg|6">Operation Locker</option>
                
                    <option value="/media/maps/Paracel_Storm_D_1.jpg|7">Paracel Storm</option>
                
                    <option value="/media/maps/Rogue_Transmission_D_1.jpg|8">Rogue Transmission</option>
                
                    <option value="/media/maps/Siege_of_Shanghai_D_1.png|10">Siege of Shanghai</option>
                
                    <option value="/media/maps/Zavod_D_1.jpg|9">Zavod 311</option>
                
            </optgroup>
        
            <optgroup label="Squad Obliteration">
                
                    <option value="/media/maps/Dawnbreaker_CN.jpg|249">Dawnbreaker CN</option>
                
                    <option value="/media/maps/Dawnbreaker_US.jpg|250">Dawnbreaker US</option>
                
                    <option value="/media/maps/Golmud_Railway_CN.jpg|251">Golmud Railway CN</option>
                
                    <option value="/media/maps/Golmud_Railway_RU.jpg|252">Golmud Railway RU</option>
                
                    <option value="/media/maps/Hainan_Resort_CN.jpg|253">Hainan Resort CN</option>
                
                    <option value="/media/maps/Hainan_Resort_US.jpg|254">Hainan Resort US</option>
                
                    <option value="/media/maps/Operation_Locker_RU.jpg|255">Operation Locker RU</option>
                
                    <option value="/media/maps/Operation_Locker_US.jpg|256">Operation Locker US</option>
                
                    <option value="/media/maps/Paracel_Storm_CN.jpg|257">Paracel Storm CN</option>
                
                    <option value="/media/maps/Paracel_Storm_US.jpg|258">Paracel Storm US</option>
                
                    <option value="/media/maps/Siege_Of_Shanghai_CN.jpg|259">Siege of Shanghai CN</option>
                
                    <option value="/media/maps/Siege_Of_Shanghai_US.jpg|260">Siege of Shanghai US</option>
                
                    <option value="/media/maps/Zavod_311_RU.jpg|261">Zavod 311 RU</option>
                
                    <option value="/media/maps/Zavod_311_US.jpg|262">Zavod 311 US</option>
                
            </optgroup>
        
    </div>

    <div id="opt-call-of-duty-advanced-warfare" style="display: none;">
        <option></option>
        
            <optgroup label="S&amp;D, S&amp;R and Domination">
                
                    <option value="/media/maps/01_-_2efVm0U.jpg|210">Ascend</option>
                
                    <option value="/media/maps/02_-_gX0bftg.jpg|211">Bio Lab</option>
                
                    <option value="/media/maps/03_-_J3nLCAM.jpg|212">Comeback</option>
                
                    <option value="/media/maps/04_-_Oag0yWn.jpg|213">Defender</option>
                
                    <option value="/media/maps/05_-_MNr3s7w.jpg|214">Detroit</option>
                
                    <option value="/media/maps/06_-_bqFfAaB.jpg|215">Greenband</option>
                
                    <option value="/media/maps/07_-_u2qI3Xb.jpg|216">Horizon</option>
                
                    <option value="/media/maps/08_-_nKfogPk.jpg|217">Instinct</option>
                
                    <option value="/media/maps/09_-_6UOR8gb.jpg|218">Recovery</option>
                
                    <option value="/media/maps/10_-_Etv1cpJ.jpg|219">Retreat</option>
                
                    <option value="/media/maps/11_-_rNo0kLi.jpg|220">Riot</option>
                
                    <option value="/media/maps/12_-_36cpfOX.jpg|221">Solar</option>
                
                    <option value="/media/maps/13_-_0lx5cJo.jpg|222">Terrace</option>
                
            </optgroup>
        
    </div>

    <div id="opt-csgo" style="display: none;">
        <option></option>
        
            <optgroup label="Defuse">
                
                    <option value="/media/maps/de_aztec_4.jpg|38">de_aztec</option>
                
                    <option value="/media/maps/de_cache_3.jpg|39">de_cache</option>
                
                    <option value="/media/maps/de_cbble_radar_Pa7j3wF.png|208">de_cbble</option>
                
                    <option value="/media/maps/de_dust2_3.jpg|41">de_dust2</option>
                
                    <option value="/media/maps/de_inferno_radar.jpg|42">de_inferno</option>
                
                    <option value="/media/maps/de_mirage_1.jpg|44">de_mirage</option>
                
                    <option value="/media/maps/de_nuke_3.jpg|45">de_nuke</option>
                
                    <option value="/media/maps/de_overpass_radar.jpg|228">de_overpass</option>
                
                    <option value="/media/maps/de_season_2.jpg|46">de_season</option>
                
                    <option value="/media/maps/de_train__xNAqv0v.jpg|47">de_train</option>
                
                    <option value="/media/maps/tuscanoverview.jpg|231">de_tuscan</option>
                
                    <option value="/media/maps/de_zoo.jpg|246">de_zoo</option>
                
            </optgroup>
        
            <optgroup label="Rescue">
                
            </optgroup>
        
    </div>

    <div id="opt-dayz" style="display: none;">
        <option></option>
        
            <optgroup label="Large">
                
                    <option value="/media/maps/Chernarus.jpg|49">Chernarus</option>
                
                    <option value="/media/maps/Chernarus_1.jpg|61">Chernarus+</option>
                
                    <option value="/media/maps/ChernarusNE.jpg|63">C+ Northeast</option>
                
                    <option value="/media/maps/ChernarusNW.jpg|62">C+ Northwest</option>
                
                    <option value="/media/maps/Chernarus_SE.jpg|65">C+ Southeast</option>
                
                    <option value="/media/maps/ChernarusSW.jpg|64">C+ Southwest</option>
                
            </optgroup>
        
            <optgroup label="Small">
                
                    <option value="/media/maps/Balota.png|50">Balota</option>
                
                    <option value="/media/maps/Berezino.png|51">Berezino</option>
                
                    <option value="/media/maps/Chernogorsk.png|52">Chernogorsk</option>
                
                    <option value="/media/maps/Electrozavodsk.jpg|58">Electrozavodsk</option>
                
                    <option value="/media/maps/Gorka.png|53">Gorka</option>
                
                    <option value="/media/maps/Krasnostav.png|54">Krasnostav</option>
                
                    <option value="/media/maps/Krasnostav_Airstrip.png|56">Krasnostav Airstrip</option>
                
                    <option value="/media/maps/NWAF.png|55">NWAF</option>
                
                    <option value="/media/maps/Solnichniy.jpg|60">Solnichniy</option>
                
                    <option value="/media/maps/Vybor.png|57">Vybor</option>
                
                    <option value="/media/maps/Zelenogorsk.jpg|59">Zelenogorsk</option>
                
            </optgroup>
        
    </div>

    <div id="opt-dota-2" style="display: none;">
        <option></option>
        
            <optgroup label="Dota 2">
                
                    <option value="/media/maps/dota_map_full_compress2.jpg|34">Detailed Map</option>
                
                    <option value="/media/maps/map.jpg|33">Regular Map</option>
                
            </optgroup>
        
    </div>

    <div id="opt-dungeon-defenders" style="display: none;">
        <option></option>
        
            <optgroup label="Dungeon Defenders">
                
                    <option value="/media/maps/Akatiti_Jungle.png|160">Akatiti Jungle</option>
                
                    <option value="/media/maps/Karathiki_Jungle.png|161">Karathiki Jungle</option>
                
            </optgroup>
        
    </div>

    <div id="opt-footballfifa" style="display: none;">
        <option></option>
        
            <optgroup label="Football/FIFA">
                
                    <option value="/media/maps/soccer_field.jpg|263">Football Field</option>
                
            </optgroup>
        
    </div>

    <div id="opt-insurgency" style="display: none;">
        <option></option>
        
            <optgroup label="Insurgency">
                
                    <option value="/media/maps/Insurgency_District_Overview.jpg|233">District</option>
                
                    <option value="/media/maps/Insurgency_Heights_Overview.jpg|234">Heights</option>
                
                    <option value="/media/maps/Insurgency_Market_Overview.jpg|236">Market</option>
                
                    <option value="/media/maps/Insurgency_Ministry_Overview.jpg|230">Ministry</option>
                
                    <option value="/media/maps/Panj.png|238">Panj</option>
                
                    <option value="/media/maps/Insurgency_Siege_Overview.jpg|235">Siege</option>
                
                    <option value="/media/maps/Insurgency_Uprising_Overview.jpg|232">Uprising</option>
                
                    <option value="/media/maps/Insurgency_Verticality_Overview.jpg|237">Verticality</option>
                
            </optgroup>
        
    </div>

    <div id="opt-league-of-legends" style="display: none;">
        <option></option>
        
            <optgroup label="3v3">
                
                    <option value="/media/maps/TwistedTreeline.jpg|88">Twisted Treeline</option>
                
            </optgroup>
        
            <optgroup label="5v5">
                
                    <option value="/media/maps/Summoners_Rift_1.jpg|66">Summoner&#39;s Rift 1</option>
                
                    <option value="/media/maps/Summoners_Rift_1341x1078.jpg|32">Summoner&#39;s Rift 2</option>
                
                    <option value="/media/maps/SummonersRift.png|67">Summoner&#39;s Rift Simple</option>
                
            </optgroup>
        
    </div>

    <div id="opt-overwatch" style="display: none;">
        <option></option>
        
            <optgroup label="Overwatch">
                
                    <option value="/media/maps/blizzworld_map.png|311">Blizzard World</option>
                
                    <option value="/media/maps/dorado_map.png|312">Dorado</option>
                
                    <option value="/media/maps/eich_map.png|313">Eichenwalde</option>
                
                    <option value="/media/maps/hana_map.png|314">Hanamura</option>
                
                    <option value="/media/maps/holly_map.png|315">Hollywood</option>
                
                    <option value="/media/maps/horizon_map.png|316">Horizon Lunar Colony</option>
                
                    <option value="/media/maps/ilios_map.png|319">Ilios</option>
                
                    <option value="/media/maps/junk_map.png|318">Junkertown</option>
                
                    <option value="/media/maps/kings_map.png|317">King&#39;s Row</option>
                
                    <option value="/media/maps/lijiang_map.png|322">Lijiang Tower</option>
                
                    <option value="/media/maps/nepal_map.png|324">Nepal</option>
                
                    <option value="/media/maps/numbani_map.png|320">Numbani</option>
                
                    <option value="/media/maps/oasis_map.png|325">Oasis</option>
                
                    <option value="/media/maps/route_map.png|321">Route 66</option>
                
                    <option value="/media/maps/anubis_map.png|310">Temple of Anubis</option>
                
                    <option value="/media/maps/volskaya_map.png|323">Volskaya</option>
                
                    <option value="/media/maps/watchpoint_map.png|309">Watchpoint Gibraltar</option>
                
            </optgroup>
        
    </div>

    <div id="opt-rust" style="display: none;">
        <option></option>
        
            <optgroup label="Rust">
                
                    <option value="/media/maps/Rust_Map.jpeg|68">Labeled</option>
                
            </optgroup>
        
    </div>

    <div id="opt-smite" style="display: none;">
        <option></option>
        
            <optgroup label="Smite">
                
                    <option value="/media/maps/duosolo.png|48">Duo - Solo</option>
                
                    <option value="/media/maps/soloduo.png|248">Solo - Duo</option>
                
            </optgroup>
        
    </div>

    <div id="opt-star-wars-battlefront" style="display: none;">
        <option></option>
        
            <optgroup label="Blast">
                
                    <option value="/media/maps/Endor_Blast.jpg|264">Endor</option>
                
                    <option value="/media/maps/Hoth_Blast.jpg|277">Hoth</option>
                
                    <option value="/media/maps/Sullust_Blast.jpg|287">Sullus</option>
                
                    <option value="/media/maps/Tatooine_Blast.jpg|296">Tatooine</option>
                
            </optgroup>
        
            <optgroup label="Cargo">
                
                    <option value="/media/maps/Endor_Cargo.jpg|269">Endor</option>
                
                    <option value="/media/maps/Hoth_Cargo.jpg|274">Hoth</option>
                
                    <option value="/media/maps/Sullust_Cargo.jpg|284">Sullus</option>
                
                    <option value="/media/maps/Tatooine_Cargo.jpg|293">Tatooine</option>
                
            </optgroup>
        
            <optgroup label="Droid Run">
                
                    <option value="/media/maps/Endor_Droid_Run.jpg|270">Endor</option>
                
                    <option value="/media/maps/Hoth_Droid_Run.jpg|275">Hoth</option>
                
                    <option value="/media/maps/Sullust_Droid_Run.jpg|285">Sullus</option>
                
                    <option value="/media/maps/Tatooine_Droid_Run.jpg|295">Tatooine</option>
                
            </optgroup>
        
            <optgroup label="Drop Zone">
                
                    <option value="/media/maps/Endor_Dropzone.jpg|265">Endor</option>
                
                    <option value="/media/maps/Hoth_Dropzone.jpg|278">Hoth</option>
                
                    <option value="/media/maps/Sullust_Dropzone.jpg|288">Sullus</option>
                
                    <option value="/media/maps/Tatooine_Dropzone.jpg|297">Tatooine</option>
                
            </optgroup>
        
            <optgroup label="Fighter Squadron">
                
                    <option value="/media/maps/Hoth_Fighter_Squadron.jpg|272">Hoth</option>
                
                    <option value="/media/maps/Sullust_Fighter_Squadron.jpg|281">Sullus</option>
                
                    <option value="/media/maps/Tatooine_Fighter_Squadron.jpg|291">Tatooine</option>
                
            </optgroup>
        
            <optgroup label="Heroes vs Villains">
                
                    <option value="/media/maps/Endor_Heroes_vs_Villains.jpg|266">Endor</option>
                
                    <option value="/media/maps/Hoth_Heroes_vs_Villains.jpg|279">Hoth</option>
                
                    <option value="/media/maps/Sullust_Heroes_vs_Villains.jpg|289">Sullus</option>
                
                    <option value="/media/maps/Tatooine_Heroes_vs_Villains.jpg|298">Tatooine</option>
                
            </optgroup>
        
            <optgroup label="Hero Hunt">
                
                    <option value="/media/maps/Endor_Hero_Hunt.jpg|267">Endor</option>
                
                    <option value="/media/maps/Hoth_Hero_Hunt.jpg|280">Hoth</option>
                
                    <option value="/media/maps/Sullust_Heroes_Hunt.jpg|290">Sullus</option>
                
                    <option value="/media/maps/Tatooine_Hero_Hunt.jpg|299">Tatooine</option>
                
            </optgroup>
        
            <optgroup label="Supremacy">
                
                    <option value="/media/maps/Endor_Supremacy.jpg|268">Endor</option>
                
                    <option value="/media/maps/Hoth_Supremacy.jpg|273">Hoth</option>
                
                    <option value="/media/maps/Sullust_Supremacy.jpg|283">Sullus</option>
                
                    <option value="/media/maps/Tatooine_Supremacy.jpg|292">Tatooine</option>
                
            </optgroup>
        
            <optgroup label="Turning Point">
                
                    <option value="/media/maps/Jakku_Turning_point.jpg|282">Jakku</option>
                
            </optgroup>
        
            <optgroup label="Walker Assault">
                
                    <option value="/media/maps/Endor_Walker_Assault.jpg|271">Endor</option>
                
                    <option value="/media/maps/Hoth_Walker_Assault.jpg|276">Hoth</option>
                
                    <option value="/media/maps/Sullust_Walker_Assault.jpg|286">Sullus</option>
                
                    <option value="/media/maps/Tatooine_walker_assault.jpg|294">Tatooine</option>
                
            </optgroup>
        
    </div>

    <div id="opt-team-fortress-2" style="display: none;">
        <option></option>
        
            <optgroup label="Badlands">
                
                    <option value="/media/maps/badlands_mid.jpg|169">Middle</option>
                
                    <option value="/media/maps/badlands_overview.png|171">Overview</option>
                
                    <option value="/media/maps/badlands_yard.jpg|170">Yard</option>
                
            </optgroup>
        
            <optgroup label="Capture Point">
                
                    <option value="/media/maps/cp_badlands.jpg|152">cp_badlands</option>
                
                    <option value="/media/maps/cp_dustbowl.jpg|153">cp_dustbowl</option>
                
                    <option value="/media/maps/Cp_glassworks_overview.jpg|247">cp_glassworks_rc6a</option>
                
                    <option value="/media/maps/cp_granary.jpg|154">cp_granary</option>
                
                    <option value="/media/maps/cp_gravelpit.jpg|155">cp_gravelpit</option>
                
            </optgroup>
        
            <optgroup label="Capture the Flag">
                
                    <option value="/media/maps/ctf_2fort.jpg|158">ctf_2fort</option>
                
                    <option value="/media/maps/ctf_turbine.jpg|159">ctf_turbine</option>
                
            </optgroup>
        
            <optgroup label="Granary">
                
                    <option value="/media/maps/granary_last.jpg|165">Last</option>
                
                    <option value="/media/maps/granary_middle.jpg|167">Middle</option>
                
                    <option value="/media/maps/cp_granary_1.jpg|168">Overview</option>
                
                    <option value="/media/maps/granary_yard.jpg|166">Yard</option>
                
            </optgroup>
        
            <optgroup label="Gullywash">
                
                    <option value="/media/maps/gullywash_middle.jpg|162">Middle</option>
                
                    <option value="/media/maps/1024px-Gullywash_overview.png|164">Overview</option>
                
                    <option value="/media/maps/gullywash_yard.jpg|163">Yard</option>
                
            </optgroup>
        
            <optgroup label="King of the Hill">
                
                    <option value="/media/maps/Harvest_overview_1.png|151">koth_harvest</option>
                
            </optgroup>
        
            <optgroup label="Payload">
                
                    <option value="/media/maps/pl_badwater_1.jpg|156">pl_badwater</option>
                
                    <option value="/media/maps/pl_goldrush.jpg|157">pl_goldrush</option>
                
                    <option value="/media/maps/Upward_overview.jpg|205">pl_upward</option>
                
            </optgroup>
        
            <optgroup label="Process">
                
                    <option value="/media/maps/process_choke.jpg|175">Choke/Yard</option>
                
                    <option value="/media/maps/process_last.jpg|176">Last</option>
                
                    <option value="/media/maps/process_mid.jpg|174">Middle</option>
                
                    <option value="/media/maps/Process_final_Overview.png|173">Overview</option>
                
            </optgroup>
        
            <optgroup label="Turbine (Pro)">
                
                    <option value="/media/maps/turbine_overview.jpg|172">Overview</option>
                
            </optgroup>
        
    </div>

    <div id="opt-the-elder-scrolls-online" style="display: none;">
        <option></option>
        
            <optgroup label="The Elder Scrolls Online">
                
                    <option value="/media/maps/RvR_Map_Full.jpg|150">Cyrodiil</option>
                
            </optgroup>
        
    </div>

    <div id="opt-titanfall" style="display: none;">
        <option></option>
        
            <optgroup label="Overview">
                
                    <option value="/media/maps/01_-_HBAWyeZ_1.jpg|177">Airbase</option>
                
                    <option value="/media/maps/02_-_f6GeWpV_1.jpg|178">Angel City</option>
                
                    <option value="/media/maps/03_-_LSGc5m4_1.jpg|179">Bone Yard</option>
                
                    <option value="/media/maps/04_-_fKsnSas_1.jpg|180">Colony</option>
                
                    <option value="/media/maps/05_-_BwUNAzf_1.jpg|181">Corporate</option>
                
                    <option value="/media/maps/06_-_DZxyT0f_1.jpg|182">Demeter</option>
                
                    <option value="/media/maps/07_-_SbyodkT_1.jpg|183">Fracture</option>
                
                    <option value="/media/maps/08_-_XPdwLOz_1.jpg|184">Lagoon</option>
                
                    <option value="/media/maps/09_-_d4w64k0_1.jpg|185">Nexus</option>
                
                    <option value="/media/maps/10_-_fW8emvQ_1.jpg|186">Outpost</option>
                
                    <option value="/media/maps/11_-_JeqApW7_1.jpg|187">Overlook</option>
                
                    <option value="/media/maps/12_-_46oi017_1.jpg|188">Relic</option>
                
                    <option value="/media/maps/13_-_4tnQjpT_1.jpg|189">Rise</option>
                
                    <option value="/media/maps/14_-_OgMKR3W_1.jpg|190">Smuggler&#39;s Cove</option>
                
                    <option value="/media/maps/15_-_1fqOrAo_1.jpg|191">Training Ground</option>
                
            </optgroup>
        
    </div>

    <div id="opt-warface" style="display: none;">
        <option></option>
        
            <optgroup label="Plant the Bomb">
                
                    <option value="/media/maps/Bridges.jpg|239">Bridges</option>
                
                    <option value="/media/maps/D17.jpg|240">D17</option>
                
                    <option value="/media/maps/Destination.jpg|241">Destination</option>
                
                    <option value="/media/maps/District.jpg|242">District</option>
                
                    <option value="/media/maps/Factory.jpg|243">Factory</option>
                
                    <option value="/media/maps/Palace.jpg|244">Palace</option>
                
                    <option value="/media/maps/Yard.jpg|245">Yard</option>
                
            </optgroup>
        
    </div>

    <div id="opt-world-of-tanks" style="display: none;">
        <option></option>
        
            <optgroup label="World of Tanks">
                
                    <option value="/media/maps/Airfield.jpg|115">Airfield</option>
                
                    <option value="/media/maps/Arctic_Region.jpg|116">Arctic Region</option>
                
                    <option value="/media/maps/Cliff.jpg|127">Cliff</option>
                
                    <option value="/media/maps/Dragon_Ridge.jpg|120">Dragon Ridge</option>
                
                    <option value="/media/maps/El_Hallouf.jpg|121">El Hallouf</option>
                
                    <option value="/media/maps/Ensk.jpg|122">Ensk</option>
                
                    <option value="/media/maps/Erlenberg.jpg|123">Erlenberg</option>
                
                    <option value="/media/maps/Fishermans_Bay.jpg|124">Fisherman&#39;s Bay</option>
                
                    <option value="/media/maps/Fjords.jpg|125">Fjords</option>
                
                    <option value="/media/maps/Highway.jpg|126">Highway</option>
                
                    <option value="/media/maps/Himmelsdorf.jpg|129">Himmelsdorf</option>
                
                    <option value="/media/maps/Karelia.jpg|130">Karelia</option>
                
                    <option value="/media/maps/Lakeville.jpg|131">Lakeville</option>
                
                    <option value="/media/maps/Live_Oaks.jpg|132">Live Oaks</option>
                
                    <option value="/media/maps/Malinovka.jpg|133">Malinovka</option>
                
                    <option value="/media/maps/Hills.jpg|128">Mines</option>
                
                    <option value="/media/maps/Monastery.jpg|134">Monastery</option>
                
                    <option value="/media/maps/Mountain_Pass.jpg|135">Mountain Pass</option>
                
                    <option value="/media/maps/Murovanka.jpg|137">Murovanka</option>
                
                    <option value="/media/maps/Asia_Miao.jpg|118">Pearl River</option>
                
                    <option value="/media/maps/Port.jpg|138">Port</option>
                
                    <option value="/media/maps/Prohorovka.jpg|140">Prohorovka</option>
                
                    <option value="/media/maps/Province.jpg|139">Province</option>
                
                    <option value="/media/maps/Redshire.jpg|141">Redshire</option>
                
                    <option value="/media/maps/Ruinberg.jpg|144">Ruinberg</option>
                
                    <option value="/media/maps/Asia_Korea.jpg|117">Sacred Valley</option>
                
                    <option value="/media/maps/Desert.jpg|119">Sand River</option>
                
                    <option value="/media/maps/Severogorsk.jpg|145">Severogorsk</option>
                
                    <option value="/media/maps/Siegfried_Line.jpg|147">Siegfried Line</option>
                
                    <option value="/media/maps/South_Coast.jpg|142">South Coast</option>
                
                    <option value="/media/maps/Steppes.jpg|143">Steppes</option>
                
                    <option value="/media/maps/Swamp.jpg|146">Swamp</option>
                
                    <option value="/media/maps/Westfeld.jpg|148">Westfeld</option>
                
                    <option value="/media/maps/Munchen.jpg|136">Wide Park</option>
                
            </optgroup>
        
    </div>

    <div id="opt-world-of-warcraft" style="display: none;">
        <option></option>
        
            <optgroup label="Siege of Orgimmar Detailed">
                
                    <option value="/media/maps/05_Galakras_map_1.jpg|92">Galakras</option>
                
                    <option value="/media/maps/14_GarroshHellscream_map_1.jpg|101">Garrosh Hellscream</option>
                
                    <option value="/media/maps/08_GeneralNazgrim_map_1.jpg|95">General Nazgrim</option>
                
                    <option value="/media/maps/01_Inmerseus_map_1.jpg|89">Immerseus</option>
                
                    <option value="/media/maps/06_IronJuggernaut_1.jpg|93">Iron Juggernaut</option>
                
                    <option value="/media/maps/07_KorkronDarkShaman_map_1.jpg|94">Kor&#39;kron Dark Shaman</option>
                
                    <option value="/media/maps/09_Malkorok_map_1.jpg|96">Malkorok</option>
                
                    <option value="/media/maps/03_Norushen_map_1.jpg|91">Norushen</option>
                
                    <option value="/media/maps/13_ParagonsKlaxxi_map_1.jpg|100">Paragons of the Klaxxi</option>
                
                    <option value="/media/maps/04_Sha_of_Pride_map.jpg|114">Sha of Pride</option>
                
                    <option value="/media/maps/12_SiegecrafterBlackfuse_map_1.jpg|99">Siegecrafter Blackfuse</option>
                
                    <option value="/media/maps/10_SpoilsofPandaria_1.jpg|97">Spoils of Pandaria</option>
                
                    <option value="/media/maps/02_FallenProtector_map_1.jpg|90">The Fallen Protectors</option>
                
                    <option value="/media/maps/11_Thok_1.jpg|98">Thok the Bloodthirsty</option>
                
            </optgroup>
        
            <optgroup label="Siege of Orgimmar Simple">
                
                    <option value="/media/maps/orgrimmarraid03.jpg|72">Galakras &amp; Iron Juggernaut</option>
                
                    <option value="/media/maps/orgrimmarraid11.jpg|79">Garrosh Hellscream</option>
                
                    <option value="/media/maps/orgrimmarraid06.jpg|74">General Nazgrim</option>
                
                    <option value="/media/maps/orgrimmarraid01_2.jpg|69">Immerseus</option>
                
                    <option value="/media/maps/orgrimmarraid04.jpg|73">Kor&#39;kron Dark Shaman</option>
                
                    <option value="/media/maps/orgrimmarraid07.jpg|75">Malkorok</option>
                
                    <option value="/media/maps/orgrimmarraid02.jpg|71">Norushen &amp; Sha of Pride</option>
                
                    <option value="/media/maps/orgrimmarraid10.jpg|78">Paragons of the Klaxxi</option>
                
                    <option value="/media/maps/orgrimmarraid09.jpg|77">Siegecrafter Blackfuse</option>
                
                    <option value="/media/maps/orgrimmarraid08.jpg|76">Spoils of Pandaria &amp; Thok the Bloodthirsty</option>
                
                    <option value="/media/maps/orgrimmarraid00.jpg|70">The Fallen Protectors</option>
                
            </optgroup>
        
            <optgroup label="Throne of Thunder Detailed">
                
                    <option value="/media/maps/03.-Council_base_logo.jpg|104">Council of Elders</option>
                
                    <option value="/media/maps/09.-DarkAnimus_base_logo.jpg|110">Dark Animus</option>
                
                    <option value="/media/maps/07.-Durumu_base_logo.jpg|108">Durumu the Forgotten</option>
                
                    <option value="/media/maps/02.-Horridon_base_logo.jpg|103">Horridon</option>
                
                    <option value="/media/maps/10.-IronQon_base_logo.jpg|111">Iron Qon</option>
                
                    <option value="/media/maps/06.-JiKun_base_logo.jpg|107">Ji&#39;Kun</option>
                
                    <option value="/media/maps/01.-Jinrokh_base_logo.jpg|102">Jin&#39;rokh the Breaker</option>
                
                    <option value="/media/maps/12.-LeiShen_base_logo.jpg|113">Lei Shen</option>
                
                    <option value="/media/maps/05.-Megaera_base_logo.jpg|106">Megaera</option>
                
                    <option value="/media/maps/08.-Primordius_base2_logo.jpg|109">Primordius</option>
                
                    <option value="/media/maps/04.-Tortos_base_logo.jpg|105">Tortos</option>
                
                    <option value="/media/maps/11.-QueenConsorts_base_logo.jpg|112">Twin Consorts</option>
                
            </optgroup>
        
            <optgroup label="Throne of Thunder Simple">
                
                    <option value="/media/maps/WorldMap-ThunderKingRaid5_1.jpg|84">Durumu the Forgotten &amp; Primordius &amp; Dark Animus</option>
                
                    <option value="/media/maps/WorldMap-ThunderKingRaid2_1.jpg|81">Horridon &amp; Council of Elders</option>
                
                    <option value="/media/maps/WorldMap-ThunderKingRaid6.jpg|85">Iron Qon &amp; Twin Consorts</option>
                
                    <option value="/media/maps/WorldMap-ThunderKingRaid4_1.jpg|83">Ji-Kun</option>
                
                    <option value="/media/maps/WorldMap-ThunderKingRaid1_1.jpg|80">Jin&#39;rokh the Breaker</option>
                
                    <option value="/media/maps/WorldMap-ThunderKingRaid7.jpg|86">Lei Shen</option>
                
                    <option value="/media/maps/WorldMap-ThunderKingRaid8.jpg|87">Ra-Den</option>
                
                    <option value="/media/maps/WorldMap-ThunderKingRaid3_1.jpg|82">Tortos &amp; Megaera</option>
                
            </optgroup>
        
    </div>

    <div id="opt-wurm-online" style="display: none;">
        <option></option>
        
            <optgroup label="Epic">
                
                    <option value="/media/maps/Epic_-_Affliction.jpg|204">Affliction</option>
                
                    <option value="/media/maps/Epic_-_Desertion.jpg|203">Desertion</option>
                
                    <option value="/media/maps/Epic_-_Elevation.jpg|202">Elevation</option>
                
                    <option value="/media/maps/Epic_-_Serenity.jpg|201">Serenity</option>
                
            </optgroup>
        
            <optgroup label="Freedom">
                
                    <option value="/media/maps/Freedom_-_Celebration.jpg|200">Celebration</option>
                
                    <option value="/media/maps/Freedom_-_Chaos.jpg|199">Chaos</option>
                
                    <option value="/media/maps/Freedom_-_Deliverence.jpg|198">Deliverence</option>
                
                    <option value="/media/maps/Freedom_-_Exodus.jpg|197">Exodus</option>
                
                    <option value="/media/maps/Freedom_-_Golden_Valley.jpg|196">Golden Valley</option>
                
                    <option value="/media/maps/Freedom_-_Independence.jpg|195">Independence</option>
                
                    <option value="/media/maps/Freedom_-_Pristine.jpg|194">Pristine</option>
                
                    <option value="/media/maps/Freedom_-_Release.png|206">Release</option>
                
                    <option value="/media/maps/Xanadu.png|207">Xanadu</option>
                
            </optgroup>
        
            <optgroup label="Wurm Online">
                
            </optgroup>
        
    </div>


    <!-- Load tactics modal -->
<div class="modal fade" id="loadCloudTactic" tabindex="-1" role="dialog" aria-labelledby="myModalLabel" aria-hidden="true">
    <div class="modal-dialog">
        <div class="modal-content">
            <div class="modal-header">
                <button type="button" class="close" data-dismiss="modal" aria-hidden="true">&times;</button>
                <h4 class="modal-title" id="myModalLabel">Load Tactic from Cloud</h4>
            </div>
            <div class="modal-body">
                <div style="height: 200px; overflow-y: scroll;">

                    <table class="tac-save-table table table-curved">
                        <thead>
                        <tr>
                            <th>Name</th>
                            <th>Map</th>
                            <th>Game</th>
                            <th style="width: 60px;">Actions</th>
                        </tr>
                        </thead>
                        <tbody class="tac-table-content">
                        </tbody>
                    </table>

                </div>
            </div>
            <div class="modal-footer">
                <button type="button" class="btn btn-default" data-dismiss="modal">Close</button>
            </div>
        </div>
    </div>
</div>


    <input type="file" id="loadMapScaleInput" style="visibility:hidden;position:absolute;top:-50;left:-50">
    <input type="file" id="loadMapNoScaleInput" style="visibility:hidden;position:absolute;top:-50;left:-50">
    <input type="file" id="loadDrawingsInput" style="visibility:hidden;position:absolute;top:-50;left:-50">

    <!-- scripts -->

    <!-- fabric.js -->
    <script src="/static/js/fabric.min.js"></script>

    <!-- TogetherJS -->
    <link rel="stylesheet" href="/static/css/dock.css">
    <script src="/static/js/TogetherJSConfig.js"></script>
    
        <script>
            TogetherJSConfig_ignoreMessages = true;
        </script>
        <script src="/static/js/togetherjs-min.js"></script>
    

    <!-- Mouse Weel Plugin -->
    <script src="/static/js/jquery.mouseweel.js"></script>

    <!-- Select2 -->
    <link href="/static/js/select2/select2.css" rel="stylesheet"/>
    <script src="/static/js/select2/select2.js"></script>
    <script src="/static/js/icons.js"></script>

    <!--Slider-->
    <link href="/static/js/slider/slider.css" rel="stylesheet"/>
    <script src="/static/js/slider/slider.js"></script>

    <!-- scripts -->
    <script src="/static/js/tacsketch.js"></script>
    <script src="/static/js/tacquery.js"></script>
    <script src="/static/js/tgjslisteners.js"></script>
    <script src="/static/js/local-save.js"></script>



    <!-- Footer -->
    <div class="container footer">
        <div class="row">
            <hr/>

            <div class="col-md-12" style="margin-bottom: 30px;">
                <p>Tacnet.io - <a href="/frontpage/about/">Developed by the Tacnet Team</a>.</p>
            </div>

        </div>
    </div>

</div>



       <div id="sidebar">
    <div id="select-map" class="bar-element">
         <div class="row">
            <div class="col-xs-12"><h5><i class="fa fa-gamepad"></i> Maps</h5><hr/></div>
        </div>

        <div class="row">
            <div class="col-xs-12">
                <p><select id="gameslist" style="width: 100%;">
                <option></option>
                
                    <option value="opt-archeage">ArcheAge</option>
                
                    <option value="opt-arma-3">Arma 3</option>
                
                    <option value="opt-battalion-1944">Battalion 1944</option>
                
                    <option value="opt-battlefield-4">Battlefield 4</option>
                
                    <option value="opt-call-of-duty-advanced-warfare">Call of Duty: Advanced Warfare</option>
                
                    <option value="opt-csgo">CS:GO</option>
                
                    <option value="opt-dayz">DayZ</option>
                
                    <option value="opt-dota-2">Dota 2</option>
                
                    <option value="opt-dungeon-defenders">Dungeon Defenders</option>
                
                    <option value="opt-footballfifa">Football/FIFA</option>
                
                    <option value="opt-insurgency">Insurgency</option>
                
                    <option value="opt-league-of-legends">League of Legends</option>
                
                    <option value="opt-overwatch">Overwatch</option>
                
                    <option value="opt-rust">Rust</option>
                
                    <option value="opt-smite">Smite</option>
                
                    <option value="opt-star-wars-battlefront">Star Wars: Battlefront</option>
                
                    <option value="opt-team-fortress-2">Team Fortress 2</option>
                
                    <option value="opt-the-elder-scrolls-online">The Elder Scrolls Online</option>
                
                    <option value="opt-titanfall">Titanfall</option>
                
                    <option value="opt-warface">Warface</option>
                
                    <option value="opt-world-of-tanks">World of Tanks</option>
                
                    <option value="opt-world-of-warcraft">World of Warcraft</option>
                
                    <option value="opt-wurm-online">Wurm Online</option>
                
                </select></p>


                <p><select id="mapslist" style="width: 100%;">
                    <option></option>
                </select></p>

                <p class="text-right" style="margin-top: 10px; text-align: center; font-size: 20px;"><i class="fa fa-gamepad"></i> <a class="contact" href="#">Suggest a map</a></p>
                <p style="margin-top: 10px; font-size: 15px;">We try to support as many games as possible. If you've got any additional suggestions, feel free to contact us through the contact form.</p>
                <div style="margin-top: 50px;">
                    <a href="#" type="button" id="loadMapButton" class="btn btn-block btn-default btn-success"><span class="glyphicon glyphicon-floppy-open"></span> Load Custom Map</a>
                    <div id="loadMapScaleDiv" class="btn-group btn-group-justified" style="display: none;">
                        <a href="#" id="loadMapScale" class="btn btn-success loadMapFromPath"><i class="fa fa-compress"></i> Scaled</a>
                        <a href="#" id="loadMapNoScale" class="btn btn-danger loadMapFromPath"><i class="fa fa-expand"></i> Original</a>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <div id="icon-picker" class="bar-element">

        <div class="row">

            <div class="col-xs-12"><h5><i class="fa fa-flag"></i> Icons</h5><hr/></div>

        </div>

        <div class="row">

            <div class="col-xs-12">

                <p><input type="text" id="iconsearch" class="form-control input-sm" placeholder="Search.."></p>

                <p><select id="gamesearch" style="width: 100%;">
                 <option value="">All Games</option>
                </select></p>

            </div>

        </div>

        <div class="scrollable">

        <div class="row icon-holder">


        </div>

        </div>

        <div class="row">
            <div class="col-xs-12">
                <div class="element-separator"></div>
            </div>
        </div>

        <div class="row">
            <div class="col-xs-12">
                <div class="btn-group btn-group-justified">
                    <a class="btn btn-success generic-color generic-green"></a>
                    <a class="btn btn-warning generic-color generic-yellow"></a>
                    <a class="btn btn-danger generic-color generic-red"></a>
                    <a class="btn btn-info generic-color generic-blue"></a>
                    <a class="btn generic-color generic-black"></a>
                    <a class="btn generic-color generic-white"></a>
                </div>
            </div>
        </div>

        <div class="generic-icons">

            <div class="row generic-icon-holder">

                <div name="Circle" class="circleFilled icon"><a href="#" title="" rel="tooltip" data-placement="bottom" data-toggle="tooltip" data-original-title="Circle"><img src="/static/img/fabric/circle.png" class="img-thumbnail"></a></div>
                <div name="Rectangle" class="rectFilled icon"><a href="#" title="" rel="tooltip" data-placement="bottom" data-toggle="tooltip" data-original-title="Rectangle"><img src="/static/img/fabric/rect.png" class="img-thumbnail"></a></div>
                <div name="Triangle" class="triangleFilled icon"><a href="#" title="" rel="tooltip" data-placement="bottom" data-toggle="tooltip" data-original-title="Triangle"><img src="/static/img/fabric/triangle.png" class="img-thumbnail"></a></div>
                <div name="Circle Strole" class="circle icon"><a href="#" title="" rel="tooltip" data-placement="bottom" data-toggle="tooltip" data-original-title="Circle Stroke"><img src="/static/img/fabric/circle_stroke.png" class="img-thumbnail"></a></div>
                <div name="Rectangle Stroke" class="rect icon"><a href="#" title="" rel="tooltip" data-placement="bottom" data-toggle="tooltip" data-original-title="Rectangle Stroke"><img src="/static/img/fabric/rect_stroke.png" class="img-thumbnail"></a></div>
                <div name="Triangle Stroke" class="triangle icon"><a href="#" title="" rel="tooltip" data-placement="bottom" data-toggle="tooltip" data-original-title="Triangle Stroke"><img src="/static/img/fabric/triangle_stroke.png" class="img-thumbnail"></a></div>
                <div name="Numbers" class="number icon"><a href="#" title="" rel="tooltip" data-placement="bottom" data-toggle="tooltip" data-original-title="Numbers"><img src="/static/img/fabric/numbers.png" class="img-thumbnail"></a></div>
                <div name="Reset Numbers" class="resetNumbers icon"><a href="#" title="" rel="tooltip" data-placement="bottom" data-toggle="tooltip" data-original-title="Reset Numbers"><img src="/static/img/fabric/reset_numbers.png" class="img-thumbnail"></a></div>

            </div>

        </div>

        <div class="row">
            <div class="col-xs-12">
                <a href="#" type="button" class="btn btn-primary addText" style="width: 230px; margin-top: 6px; margin-right: 10px;"><i class="fa fa-font"></i> Add Text</a>
            </div>
        </div>

    </div>

    <div id="cloud-menu" class="bar-element">
        <div class="row">
            <div class="col-xs-12"><h5><i class="fa fa-flag"></i> Cloud Save</h5><hr/></div>
        </div>

        <div class="row" id="save-cloud">
            <div class="col-xs-12">
                <h5 style="text-align: center; margin-top: 25px;">Tactic Name:</h5>
                <input type="text" class="form-control tacticName" style="margin-top: 20px; height: 50px; color: #FFF !important; font-size: 24px !important;" placeholder="Enter tactic name..">

                <p style="margin-top: 20px;">Note that you need to be logged in to cloud save tactics.</p>

                <div class="btn-group btn-group-justified" style="margin-top: 40px;">
                    <a class="btn btn-success cloudSave" style="padding: 10px 10px; font-size: 20px;"><span class="glyphicon glyphicon-cloud-upload"></span> Save</a>
                    <a class="btn btn-info select-cloud-load" style="padding: 10px 10px; font-size: 20px;"><span class="glyphicon glyphicon-cloud-download"></span> Load</a>
                </div>
            </div>
        </div>
    </div>

    <div id="save-menu" class="bar-element">
        <div class="row">
            <div class="col-xs-12"><h5><i class="fa fa-flag"></i> Save/Load</h5><hr/></div>
        </div>
        <div class="row">
            <div class="col-xs-12">
                <h5 style="text-align: center;">Tactics:</h5>
                <div class="btn-group btn-group-justified" style="width: 230px; margin-top: 20px; margin-right: 10px;">

                    <a href="#" type="button" class="btn btn-info" id="saveLocal"><span class="glyphicon glyphicon-floppy-save"></span> Save</a>
                    <a href="#" type="button" class="btn btn-default" id="loadLocal"><span class="glyphicon glyphicon-floppy-open"></span> Load</a>

                </div>
            </div>
        </div>
        <div class="row">
            <div class="col-xs-12">
                <h5 style="text-align: center; margin-top: 30px;">Screenshot:</h5>
                <a href="#" type="button" class="btn btn-success saveScreenshot" style="width: 230px; margin-top: 20px; margin-right: 10px;"><i class="fa fa-camera"></i></a>
                <p style="margin-top: 20px; font-size: 15px;">Screenshots are just images and cannot be loaded. </p>
            </div>
        </div>
    </div>

    <div id="restrictions-menu" class="bar-element">
        <div class="row">
            <div class="col-xs-12"><h5><i class="fa fa-minus-circle"></i> Access Control</h5><hr/></div>
        </div>

        <div class="row">
            <div class="col-xs-12">
                <div class="restrict-scroll">
                    <table id="peerList" class="table table-curved">
                        <thead>
                            <tr>
                                <th>Nickname</th>
                                <th>Rights</th>
                            </tr>
                        </thead>
                        <tbody id="peerBody"></tbody>
                    </table>
                </div>
            </div>
        </div>


    </div>

    <div class="dock">

        <ul class="button-list">

            <li class="icon-button select-map" data-toggle="tooltip" data-placement="right" title="Select Map" rel="tooltip"><i class="fa fa-gamepad"></i></li>
            <li class="icon-button select-icon" data-toggle="tooltip" data-placement="right" title="Icons" rel="tooltip"><i class="fa fa-flag"></i></li>
            <li class="icon-button select-restrictions" data-toggle="tooltip" data-placement="right" title="Restrictions" rel="tooltip"><i class="fa fa-users"></i></li>
            <li class="icon-button select-cloud-save" data-toggle="tooltip" data-placement="right" title="Cloud Saving" rel="tooltip"><span class="glyphicon glyphicon-cloud"></span></li>
            <li class="icon-button select-save" data-toggle="tooltip" data-placement="right" title="Save Drawings" rel="tooltip"><span class="glyphicon glyphicon-floppy-disk"></span></li>

        </ul>

    </div>

</div>




    <script src="//cdnjs.cloudflare.com/ajax/libs/bootstrap-growl/1.0.0/jquery.bootstrap-growl.min.js"></script>

<script src="/static/js/auth.js"></script>

<script src="/static/js/jquery.mobile.js"></script>
<script src="/static/js/googleanalytics.js"></script>
<script src="/static/js/base.js"></script>



</body>
</html>
