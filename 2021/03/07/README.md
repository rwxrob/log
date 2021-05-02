## Sunday, March 7, 2021, 11:41:46PM EST <1615178506>

Remembered today to not use `-f` with `ln` because you really should not
be creating a symlink at all if there is already one there. If you try
it you will end up with a link inside of the directory to which the link
points. I have had this happen with `.vim` and `.fonts` before because I
keep forgetting this (which is why I'm writing this down).

## Sunday, March 7, 2021, 11:19:58PM EST <1615177198>

TIL that `.uuid` files that are immediately recreated in a font
directory are probably the result of `fccache` creating them. The only
solution is to add `.uuid` to the `.gitignore` file. Apparently, this is
created by the `FcDirCacheCreateUUID` function (for reference).

## Sunday, March 7, 2021, 2:23:18AM EST <1615101798>

Today I saw the same asshole `nsa_hacker` on three different Twitch
channels trying to get people to visit `blank.com` where there is this
trojan that appears (on the surface) to exploit anyone running a certain
ad blocker. All I can think about is how fucking glad I am that I don't
use a shitty graphic browser that much. I reported them, but I'm sure
they have already hit a few unsuspecting suckers.

```html
<!DOCTYPE html><html data-adblockkey="MFwwDQYJKoZIhvcNAQEBBQADSwAwSAJBANDrp2lz7AOmADaN8tA50LsWcjLFyQFcb/P2Txc58oYOeILb3vBw7J6f4pamkAQVSQuqYsKx3YzdUHCvbVZvFUsCAwEAAQ==_y0t89QPQBQiaap2wXxKQ5kxi2uF09NfnGZpXaVY9hcQpQZH8fjtBzRk1BRRQh52DGXh81RoK7slMc6f7amTTdA=="><head><meta http-equiv="Content-Type" content="text/html; charset=utf-8"><title></title><meta name="viewport" content="width=device-width, initial-scale=1"><meta name="description" content="See related links to what you are looking for."/></head><!--[if IE 6 ]><body class="ie6"><![endif]--><!--[if IE 7 ]><body class="ie7"><![endif]--><!--[if IE 8 ]><body class="ie8"><![endif]--><!--[if IE 9 ]><body class="ie9"><![endif]--><!--[if (gt IE 9)|!(IE)]> --><body><!--<![endif]--><script type="text/javascript">g_pb=(function(){var
DT=document,azx=location,DD=DT.createElement('script'),aAC=false,LU;DD.defer=true;DD.async=true;DD.src="//www.google.com/adsense/domains/caf.js";DD.onerror=function(){if(azx.search!=='?z'){azx.href='/?z';}};DD.onload=DD.onreadystatechange=function(){if(!aAC&&LU){if(!window['googleNDT_']){}
LU(google.ads.domains.Caf);}
aAC=true;};DT.body.appendChild(DD);return{azm:function(n$){if(aAC)
n$(google.ads.domains.Caf);else
LU=n$;},bq:function(){if(!aAC){DT.body.removeChild(DD);}}};})();g_pd=(function(){var
azx=window.location,nw={},bH,azw=azx.search.substring(1),aAv,aAw;if(!azw)
return nw;aAv=azw.split("&");for(bH=0;bH<aAv.length;bH++){aAw=aAv[bH].split('=');nw[aAw[0]]=aAw[1]?aAw[1]:"";}
return nw;})();g_pc=(function(){var $is_ABP_whitelisted=null;var $Image1=new Image;var $Image2=new Image;var $error1=false;var $error2=false;var $remaining=2;var $random=Math.random()*11;function $imageLoaded(){$remaining--;if($remaining===0)
$is_ABP_whitelisted=!$error1&&$error2;}
$Image1.onload=$Image2.onload=$imageLoaded;$Image1.onerror=function(){$error1=true;$imageLoaded();};$Image2.onerror=function(){$error2=true;$imageLoaded();};$Image1.src='/px.gif?ch=1&rn='+$random;$Image2.src='/px.gif?ch=2&rn='+$random;return{azo:function(){return'&abp='+($is_ABP_whitelisted?'1':'0');},$isWhitelisted:function(){return $is_ABP_whitelisted;},$onReady:function($callback){function $poll(){if($is_ABP_whitelisted===null)
setTimeout($poll,100);else $callback();}
$poll();}}})();(function(){var aAo=screen,Rr=window,azx=Rr.location,aAB=top.location,DT=document,Sf=DT.body||DT.getElementsByTagName('body')[0],aAy=0,aAx=0,aAz=0,$IE=null;if(Sf.className==='ie6')
$IE=6;else if(Sf.className==='ie7')
$IE=7;else if(Sf.className==='ie8')
$IE=8;else if(Sf.className==='ie9')
$IE=9;function aAu($callback){aAz++;aAy=Rr.innerWidth||DT.documentElement.clientWidth||Sf.clientWidth;aAx=Rr.innerHeight||DT.documentElement.clientHeight||Sf.clientHeight;if(aAy>0||aAz>=5){$callback();}
else{setTimeout(aAu,100);}}
var $num_requirements=2;function $requirementMet(){$num_requirements--;if($num_requirements===0)
aAA();}
aAu($requirementMet);g_pc.$onReady($requirementMet);function aAA(){var ef=undefined,IQ=encodeURIComponent,aAt;if(aAB!=azx&&g_pd.r_s===ef)
aAB.href=azx.href;aAt=DT.createElement('script');aAt.type='text/javascript';aAt.src='/glp'+'?r='+(g_pd.r!==ef?g_pd.r:(DT.referrer?IQ(DT.referrer.substr(0,255)):''))+
(g_pd.r_u?'&u='+g_pd.r_u:'&u='+IQ(azx.href.split('?')[0]))+
(g_pd.gc?'&gc='+g_pd.gc:'')+
(g_pd.cid?'&cid='+g_pd.cid:'')+
(g_pd.query?'&sq='+g_pd.query:'')+
(g_pd.search?'&ss=1':'')+
(g_pd.a!==ef?'&a':'')+
(g_pd.z!==ef?'&z':'')+
(g_pd.z_ds!==ef?'&z_ds':'')+
(g_pd.r_s!==ef?'&r_s='+g_pd.r_s:'')+
(g_pd.r_d!==ef?'&r_d='+g_pd.r_d:'')+'&rw='+aAo.width+'&rh='+aAo.height+
(g_pd.r_ww!==ef?'&ww='+g_pd.r_ww:'&ww='+aAy)+
(g_pd.r_wh!==ef?'&wh='+g_pd.r_wh:'&wh='+aAx)+
(g_pd.ref_keyword!==ef?'&ref_keyword='+g_pd.ref_keyword:'')+
(g_pc.$isWhitelisted()?'&abp=1':'')+
($IE!==null?'&ie='+$IE:'')+
(g_pd.partner!==ef?'&partner='+g_pd.partner:'')+
(g_pd.subid1!==ef?'&subid1='+g_pd.subid1:'')+
(g_pd.subid2!==ef?'&subid2='+g_pd.subid2:'')+
(g_pd.subid3!==ef?'&subid3='+g_pd.subid3:'')+
(g_pd.subid4!==ef?'&subid4='+g_pd.subid4:'')+
(g_pd.subid5!==ef?'&subid5='+g_pd.subid5:'');Sf.appendChild(aAt);}})();</script></body></html>
```
