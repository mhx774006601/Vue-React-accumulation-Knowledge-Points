路由hash模式：是利用#号这种模式，它不会让页面刷新，它会监听hash的变化，每次变化的时候它会动态的去做事情－－这是它的原理

　　history:比hash更好的方式　。在路由中配置：mode:'history'。　地址中不带#　,使用:localhost:8080/page1 页面还不会刷新。利用了h5中的history　API　。
  
  好处：首先比较友好，搜索引擎也比较好，hash这个是搜索引擎是不关心的，但是localhost:8080/page1这样的地址搜索引擎是可以关注到的。
  在维护的时候更加直观一些。用户在读的时候，可读性更强。
　　但是这种方式有一个问题：就是往服务器上布署的时候，需要服务器特别的支持，比如说我们使用nginx配置,我们需要把网址的前缀，
  根路由后面的地址以后的部分全部都指向根页面。比如：localhost:8080/page1/1/info  。需要把/page1/1/info指向根页面，然后网站才能正常。否则会出问题。
  
  获取参数用$route路由。路由跳转用$router路由器。
  查询参获取方式用：query来获取　
  
  params传参：如果是想传进去的参数做占位符的话，这些参数可读性比较强，它是有语义化的意思，
  （比如地址：localhost:8080/users/1/info 像这种就用路由的方式传参）首先它的可读性很强，其次它是必选参。如果不传的话，跳转不到这个地址。
　　　如果是query查询参的话，那这个参数就不是必须的了，传与不传都能跳转到这个地址。它是可选参。
