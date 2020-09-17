# Restful API - Detected Domain.
### **API purpose and motivation**
-----------------------------------------------------------
   * Nearly 10 years, there have been a lots of scammer use fraud website to bilk people, especially elder people.
   * On average, nearly 60 fraud cases occured per day in Taiwan. To prevent people from bilking again and again in our society, we decide to develope this 'Detect fraud API'.

### **Guideline for Detect Fraud Service**  
-----------------------------------------------------------
   - **First of all**, you need to sign up your username and password.
   - **Second**, when you pass our user certification proccess, we will give a number created by JWT as your api-key. This api-key will be vaild durning 10 days period, and it     will be limited for 50 times requests per minute. If you want datas more than these restrictions, you must pay a small amount to relax the lockdown restrictions.
   - **Thrid**, in our api, we use Swagger-2 to build API-document, so you can just input localhost/.../swagger-ui.html to get beautiful and clearly document that we set up before.
   - **Fourth**, we provide users for checking their suspicious domain/url by our databases. Apart from this, we provide users reported system when someone confused by simialr domain. And we also provide whois system to checkout domain/url which is very suspicious/likey suspicious/non suspicious. 

-----------------------------------------------------------
#### We provide the following interface:

url protocol                     | method | Description
---------------------------------|:------:| -----------------------------------------------
localhost/../api/blacklist       | GET    |  To fetch all blacklist database.
localhost/../api/blacklist       | POST   |  To add blacklist.
localhost/../api/{domain}        | PULL   |  To updated blacklist.
localhost/../api/{domain}        | DELETE |  To delete  blacklist.
localhost/../api/reported        | GET    |  To fetch all reported as suspicious domain/url.
localhost/../api/reported        | POST   |  To add reported as suspicious domain/url.
localhost/../api/whois/{domain}  | GET    |  To get whois result.
localhost/../api/authenticate    | POST   |  To get api-key if we verified that.

### If you want to use our API interface, please send email to me, or 
