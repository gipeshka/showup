<?php

$ch = curl_init();

curl_setopt_array($ch, array(CURLOPT_COOKIEFILE => 'cookie.txt',
                                CURLOPT_COOKIESESSION => true,
                                CURLOPT_RETURNTRANSFER => true,
                                CURLOPT_BINARYTRANSFER => true,
                                CURLOPT_URL => 'http://elibrary.misis.ru/login.php',
                                CURLOPT_POST => true,
                                CURLOPT_FOLLOWLOCATION => true,
                                CURLOPT_POSTFIELDS => 'username=login&password=password&language=ru_UN&action=login'));

$ret = curl_exec($ch);

echo $ret;