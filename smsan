<?php

/*
 * bodytype 1: text message
 *          2: flash message
 *          3: binary message
 *          4: unicode message
 * 
 * dlr      0: no delivery report
 *          1: ada delivery report
 * 
 * validity 3: 3 hari (Default)
 */
$data = array(
    'username' => '<check in your dashboard>', //Required
    'password' => '<check with support>', //Required
    'destination' => '601xxxxxxxx', //Required
    'sender' => '<request for sender id and wait for approval>', //Required
    'body' => '<your messsage here>', //Required
    'bodytype' => 1,
    'reference' => 'untungle',
    'dlr' => 0,
    'validity' => 3
);

$process = curl_init("https://api.silverstreet.com/send.php");
curl_setopt($process, CURLOPT_TIMEOUT, 10);
curl_setopt($process, CURLOPT_RETURNTRANSFER, TRUE);
curl_setopt($process, CURLOPT_SSL_VERIFYPEER, FALSE);
curl_setopt($process, CURLOPT_POSTFIELDS, $data);
curl_setopt($process, CURLOPT_CONNECTTIMEOUT, 0);
$return = curl_exec($process);
curl_close($process);
var_dump($return);
