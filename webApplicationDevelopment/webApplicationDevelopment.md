# <span class="header">Basic Building Blocks of Web Application Development</span>

* Software Languages
* IP address
* Domain & Web Hosting
* HTTP / HTTPS
* Database
* Licenses

# <span class="header">Software Languages</span>

Here is a list of Software Programming Language.
* Python
* JavaScript
* Java
* C#
* C
* C++
* GO
* R
* Swift
* Dart
* Kotlin
* Ruby

## <span class="header2">Which Language to learn ?</span>

This question can spark much debate and much varies on preference of individuals. So a simple approach we can use is to identify what kind of work we need to do :-

* <span class="list">JavaScript</span> - Web-based work
* <span class="list"> C# or Java Work </span> - based on software app in Large companies
* <span class="list">PHP</span> - Work based on Web app in Large companies
* <span class="list">R and MATLAB</span> - Data analytics
* <span class="list">C, C++ or Rust</span> - Embedded devices
* <span class="list">Go or Scala</span> - Apps that run on cloud
* <span class="list">Swift, Kotlin or Dart</span> - Mobile Apps

# <span class="header">IP Address</span>

IP stands for 'Internet Protocol', which<span class="highlight"> means a set of rules for the format of data sent via Internet or local network</span>.
>An IP address is a unique address made up of string of numbers that identifies a device on the internet or local network.

These string of numbers are not random. They are mathematically produced and allocated by (IANA) Internet Assigned Numbers Authority, its a division of (ICANN) Internet Corporation for Assigned Names and Numbers.

## <span class="header2">Types of IP</span> 

There are two types of IP address :-

1. Public IP address. Public address can be further subdivided into 2 categories :-
   1. Static IP address
   2. Dynamic IP address
2. Private IP address 
   
## <span class="header2">Versions of IP address</span>

Currently, there are two versions of IP that coexist in the global internet. 
1. IP version 4 (IPv4)
2. IP version 6 (IPv6) 

<span class="highlight">IP address are made up of binary values</span>. IPv4 address are 32 bits long, and IPv6 address are 128 bits long.

### <span class="header3">IPv4</span>

| Class | Range | Used For |
| ------- | ----- | --- |
| Class A | 0 - 127 | Local system |
| Class B | 128 - 191 | Internet |
| Class C | 192 - 223 |  Local Network |
| Class D | 224 - 239 |  Not used/Reserved |
| Class E | 240 - 255 |  Not used |

### <span class="header3">IPv6</span>

IPv6 is the next generation Internet Protocol standard intended to eventually replace IPv4. Since at the start, it was thought that IPv4 that can support upto 4.3 billion devices would suffice however due to the growth of internet, personal computers and Smartphones this assumption was proved wrong. Which is why IPv6 are developed which can support upto 340 trillion trillion devices. Additionally, IPv6 can handle packets more efficiently, improve performance and increase security.

## <span class="header2">IP address Structure</span>

As we know IPv4 address is written in decimal digits, formatted as four 8-bit fields that are separated by '.'(period). Each 8-bit field represents a byte of the IPv4 address.

The bytes of IPv4 address are further classified into two parts :
* The network part
* The Host

Additional a port number can be attached to it, which altogether forms a socket address. <span class="highlight">It is only using these socket address that two device communicate with each other</span>.
 
<img src="../assests/IP_address.jpg" width="500">

To explain with an example, Think of ip address as a real life address in which the network part represents the street name and the host part represents the building name. The port number here represents the apartment number.

<img src="../assests/Letter.jpg" width="500">

## <span class="header2">Port Range Group</span>

**0 to 1023** - Only special companies like Apple QuickTime, MSN, SQL services, Gopher services and other prominent services have these port numbers.

**1024 to 49151** - Registered ports, means they can be registered to specific protocol by software corporations.(Application port)

**49152 to 65536** - Dynamic or private ports, means that they can be used by anyone.(Open port)

# <span class="header">Domain & Web Hosting</span>

So by now, we know that internet is a giant network of computer connected to each other and in order for communication to occur between them IP address are used.<span class="highlight"> IP address however are long strings of numbers, which can be quite difficult to remember, especially when multiple websites are involved</span>. This is why Domain names were invented to solve this problem. So instead of typing long string of numbers we just need to type the domain name associated to the IP address in our address bar. 

For eg :- `www.google.com` is the domain name whereas its IP address is 8.8.8.8

## <span class="header2">How Domain Name Works</span>

When we enter a domain name like google in our browser, it first sends request to the DNS (Domain Name System) which is global network of servers. These servers then look up for the name servers associated with domain and forward the request to those name servers.
 
For eg : If we host website on vulter, then its name server info will be :-

`ns1.vulter.com`

`ns2.vulter.com`

Theses name servers are computers managed by the hosting company. The hosting company then forwards our request to the computer where our website is stored.
This computer is called a web server. It has special software like Apache or Nginx installed in it. (Apache and Nginx are web server software which we will talk about later). The web server now fetches the web pages and info associated with it.

## <span class="header2">Difference Between Domain, Website and Web Hosting</span>

So often, I used to get confused between the concept of Domains, Website and Web Hosting. To clarify, Website is made up of files like HTML pages, images and more. <span class="highlight">If domain name is the web address of our website, then web hosting is the home where our website lives</span>. This is the actual computer where our website files are stored. Such computers are called servers and they are offered as a service by hosting companies.

> To create a website, we need both domain name and web hosting.

# <span class="header">HTTP & HTTPS</span>

<span class="highlight">HTTP stands for Hyper Text Transfer Protocol</span>. HTTP was invented along side HTML to create the first interactive, text-based web browser. It is a protocol which allows us a way to interact with web resources such as HTML files. HTTP generally uses Transmission Control Protocol (TCP) connection to communicate with servers.

HTTP utilizes specific request methods in order to perform various tasks. These request methods are also known as HTTP verbs. Some of the HTTP verbs are :- 
1. <span class="list">Get</span> - Fetch data from the server
2. <span class="list">Post</span> - Submit data to the server
3. <span class="list">Put</span> - Update data on the server
4. <span class="list">Delete</span> - Delete data from the server

Along with these verbs HTTP also uses  headers that can pass additional information between client and servers. Context-Wise there are three kinds of headers. They are :-
1. <span class="list">General Header</span> - Information not related to the client, server or HTTP.
2. <span class="list">Request Header</span> - Preferred document formats and server parameter.
3. <span class="list">Response Header</span> - Information about the server sending the response.

Now, Whenever clients make a request to the server, the server responds along with a HTTP status code. This code can help us to identify if our request was successful or not. There are five categories of status code, which goes like :-
1.  <span class="list">0-100</span> - Informational responses
2.  <span class="list">200-299</span> - Success responses
3.  <span class="list">300-399</span> - Redirect responses
4. <span class="list"> 400-499</span> - Client error responses
5. <span class="list"> 500-599</span> - Server error responses

# <span class="header">Database</span>

A database is a collection of information that is organized so that it can be easily accessed, managed and updated.

## <span class="header2">Types of Database</span>

### <span class="header3"> Relational Database</span>
 
It is a tabular database in which data is defined so that it can be reorganized and accessed in a number of different ways.

### <span class="header3">Non-Relational Database</span>

It uses a storage model optimized for specific requirements of the type of data being stored. 

There are four popular non relational database types :-
1. Document data stores
2. Columnar data stores
3. Key-value stores
4. Graph databases

###  <span class="header3">Cloud database</span>

A cloud database is a database that has been optimized or built for a virtualized environment, either in a hybrid cloud, public cloud or private cloud.

# <span class="header">Licenses</span>

<span class="highlight">The license is a text document designed to protect the intellectual property of the software developer</span> .

Most software falls under one of two categories :-
* <span class="list">Proprietary</span> – also referred to as “closed source”
* <span class="list">Free and open-source software</span> (FOSS) – referred to as “open source”

Some Popular open source Licenses are :-
* Apache 2.0
* MIT
* GPL
* BSD
* Mozilla

<style>
.highlight{
  color: #75FF33
}
.list{
  color: #FF8080
}
.header3{
  color: #E6D100
}
.header{
  color: #EE82EE
}
.header2{
  color: #00FFFF
}
</style>