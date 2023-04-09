# Postman-collections

###   <h3 align="left"> :one: Тестирование API Restful-Booker (POST, GET, PUT, DELETE) в формате JSON. 
Документация API: <a href="http://restful-booker.herokuapp.com/apidoc/index.html#api-Auth">Restful Booker</a></h3>
###   <h3 align="left">:heavy_check_mark: Создание токена POST https://restful-booker.herokuapp.com/auth</h3> 
 
  ![Image alt](https://github.com/Aleks-vl/Postman-collections/blob/main/POST%20CreateToken.png)
  
###   <h3 align="left">:heavy_check_mark: Создать бронирование POST https://restful-booker.herokuapp.com/booking</h3> 
 
  ![Image alt](https://github.com/Aleks-vl/Postman-collections/blob/main/POST%20CreateBooking.png)
  
###   <h3 align="left">:heavy_check_mark: Получить информацию о бронировании GET https://restful-booker.herokuapp.com/booking/:id</h3> 
 
  ![Image alt](https://github.com/Aleks-vl/Postman-collections/blob/main/GET%20GetBooking.png)
  
###   <h3 align="left">:heavy_check_mark: Обновить информацию о бронировании PUT https://restful-booker.herokuapp.com/booking/:id</h3> 
 
  ![Image alt](https://github.com/Aleks-vl/Postman-collections/blob/main/PUT%20UpdateBooking.png)
  
###   <h3 align="left">:heavy_check_mark: Удалить бронирование DELETE https://restful-booker.herokuapp.com/booking/:id</h3> 
 
  ![Image alt](https://github.com/Aleks-vl/Postman-collections/blob/main/DELETE%20DeleteBooking.png)
  
  ###   <h3 align="left"> :two: Автоматизация в Postman 
  Документация API: https://reqres.in/</h3>
 ###   <h4 align="left">:heavy_check_mark: Тестирование response body. </h4> 
 ###   <h4 align="left"> Коллекция :arrow_right: https://github.com/Aleks-vl/Postman-collections/blob/main/Test%20response%20body.postman_collection.json </h4> 
 ###   <h4 align="left"> Run collection :arrow_right: https://github.com/Aleks-vl/Postman-collections/blob/main/Test%20response%20body.postman_test_run.json </h4> 
  ```js

pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});
  pm.test("Test response body", function () {
    var jsonData = pm.response.json();
    pm.expect(jsonData.data[0].id).to.be.a('number');
    pm.expect(jsonData.data[0].email).to.be.a('string');
    pm.expect(jsonData.data[0].first_name).to.be.a('string');
    pm.expect(jsonData.data[0].last_name).to.be.a('string');
    pm.expect(jsonData.data[0].avatar).to.be.a('string');
  });
pm.test("Test response body (values)", function () {
    var jsonData = pm.response.json();
    pm.expect(jsonData.data[0].id).to.eql(7);
    pm.expect(jsonData.data[0].email).to.eql('michael.lawson@reqres.in');
    pm.expect(jsonData.data[0].first_name).to.eql("Michael");
    pm.expect(jsonData.data[0].last_name).to.eql("Lawson");
    pm.expect(jsonData.data[0].avatar).to.eql("https://reqres.in/img/faces/7-image.jpg");
  });
  
  ```
  
  ###   <h3 align="left"> :three: Data-Driven Testing in Postman 
  Документация API: https://reqres.in/</h3>
  
  ![Документация API POST](https://user-images.githubusercontent.com/122369252/230072425-3e906e0d-1f22-48bc-b1f8-b07fcb8049b4.png)

 https://user-images.githubusercontent.com/122369252/230071832-f002d204-e599-42c5-8f82-8a5da5ccca35.mp4

 
