# istio redirect non-www to www

~~~
curl -I http://abdidarmawan.com
HTTP/1.1 301 Moved Permanently
location: https://abdidarmawan.com/
date: Mon, 11 May 2020 04:17:18 GMT
server: istio-envoy
transfer-encoding: chunked
~~~

~~~
curl -I https://abdidarmawan.com
HTTP/2 301 
location: https://www.abdidarmawan.com/
date: Mon, 11 May 2020 04:17:26 GMT
server: istio-envoy
~~~

~~~
curl -I https://www.abdidarmawan.com
HTTP/2 200 
server: istio-envoy
date: Mon, 11 May 2020 07:40:56 GMT
content-type: text/html
expires: Mon, 11 May 2020 07:40:55 GMT
cache-control: no-cache
x-envoy-upstream-service-time: 0
~~~
