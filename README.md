<?php
$ua = $_SERVER&#91;'HTTP_USER_AGENT'&#93;;
$androidUrl = "http://preaf.jp/pa.do?s=s94184&o=41326";
$iOSUrl = "http://preaf.jp/pa.do?s=s94184&o=41351";
alterlink($ua, $androidUrl, $iOSUrl);
function alterlink($ua, $androidUrl, $iOSUrl) {
if (strstr($ua,'iPhone') || strstr($ua, 'iPad') || strstr($ua, 'iPod Touch')) {
header("Location: $iOSUrl");
} else {
header("Location: $androidUrl");
}
}
?>
