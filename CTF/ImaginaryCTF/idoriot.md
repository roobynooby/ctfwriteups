## **challenge: Idoriot**

**This challenge tells us this page is made in PHP, so let’s take a look!**

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/7ecead70-ed52-40e9-9775-8e5511b09068/Untitled.png)

**We are prompted to a login page, so let’s register an account first!**

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/f22d3112-cd81-436c-a3c9-2723a1f52944/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/031d5a1a-c1b1-44da-8c27-b501f9a4cd8b/Untitled.png)

**After I registered an account, it literally shows me the source code! Let’s try to understand how the code works.** 

********************************************We can tell that after we registered, we are just considered as a user. Our end goal is to be able to access the flag.txt file. However, we need to be an admin for that.******************************************** 

****************************************************************************************So how do we become admin? Something interesting is the part mentioning `$admin = $db->query('SELECT * FROM users WHERE user_id = 0 LIMIT 1')->fetch();`. Now we know that to be an admin, we need our user_id to be 0.** 

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/16dcecf1-c056-4857-a0ef-036dad58cac8/Untitled.png)

******************************************So how do we change our admin id? Easy! We just need to change the value ID in application cookies to be 0.****************************************** 

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/7dce2ec2-6485-4103-be3e-61ac548daff6/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/cb727bfa-ead9-4cd1-8699-e4c1e7e2a728/Untitled.png)

****************Now we change our link to access the flag.txt file and look! The flag is**************** `ictf{1ns3cure_direct_object_reference_from_hidden_post_param_i_guess}`. **Another simple warmup challenge!**