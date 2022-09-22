## Creating an S3 bucket using AWS console

<img width="842" alt="Screenshot 2022-09-22 at 11 26 16" src="https://user-images.githubusercontent.com/102330725/191723565-4eb23d5f-bf23-4537-94b2-3dfece53ada3.png">
<img width="842" alt="Screenshot 2022-09-22 at 11 26 40" src="https://user-images.githubusercontent.com/102330725/191723638-5fa6a4a3-9a75-4243-a173-a2689e36aa0e.png">
<img width="842" alt="Screenshot 2022-09-22 at 11 27 35" src="https://user-images.githubusercontent.com/102330725/191723809-4cb30e8d-6333-4472-a516-2c4182789158.png">
<img width="842" alt="Screenshot 2022-09-22 at 11 28 10" src="https://user-images.githubusercontent.com/102330725/191723910-fbe39a66-e703-4b2a-92b8-bb874ab563f0.png">
<img width="842" alt="Screenshot 2022-09-22 at 11 28 27" src="https://user-images.githubusercontent.com/102330725/191723964-59fcf207-eed6-4ae8-b285-2d298cb6d52a.png">
<img width="1034" alt="Screenshot 2022-09-22 at 11 48 12" src="https://user-images.githubusercontent.com/102330725/191727642-ea98015c-a3f7-4625-bced-a2f86bf2aa29.png">
<img width="990" alt="Screenshot 2022-09-22 at 11 49 03" src="https://user-images.githubusercontent.com/102330725/191727794-5ca1d173-41d2-4d40-aa3f-ececa2134ff9.png">
<img width="990" alt="Screenshot 2022-09-22 at 11 54 27" src="https://user-images.githubusercontent.com/102330725/191729130-92c78e4b-d44a-452c-8097-8135041b35bd.png">
<img width="856" alt="Screenshot 2022-09-22 at 11 58 30" src="https://user-images.githubusercontent.com/102330725/191729489-bac628d0-96af-4a4b-a3ad-d2614f1c4602.png">
<img width="1380" alt="Screenshot 2022-09-22 at 11 59 21" src="https://user-images.githubusercontent.com/102330725/191729663-e7612e0d-2b9e-4141-a2d7-6066e5db5c53.png">
<img width="1380" alt="Screenshot 2022-09-22 at 12 02 44" src="https://user-images.githubusercontent.com/102330725/191730351-1fc6f654-9117-4784-a017-b38433bcfd88.png">

## Make S3 bucket public

1. Under permissions go to **Block all public access** and click on **Edit**

<img width="1025" alt="Screenshot 2022-09-22 at 12 41 03" src="https://user-images.githubusercontent.com/102330725/191737404-24c47a77-af87-4b78-ba5b-cd8049141f8b.png">

2. Un-Check the box and **Save Changes**
<img width="815" alt="Screenshot 2022-09-22 at 12 42 56" src="https://user-images.githubusercontent.com/102330725/191737758-39c3733d-222a-4e88-a5bb-adc3c9e1b22b.png">

3. Click on **Edit** under **Bucket Policy**
<img width="1271" alt="Screenshot 2022-09-22 at 13 54 41" src="https://user-images.githubusercontent.com/102330725/191752441-7fe93142-e2a1-40db-a1a3-a0157e476d13.png">

4. Click on **Policy Generator** 
<img width="1000" alt="Screenshot 2022-09-22 at 13 55 58" src="https://user-images.githubusercontent.com/102330725/191752783-3707211f-65e5-4c6a-a6af-3b6a64419a5b.png">

5. Select **S3 Bucket Policy** as the Type of Policy
<img width="1012" alt="Screenshot 2022-09-22 at 13 57 08" src="https://user-images.githubusercontent.com/102330725/191753020-bdf0eb60-f2fd-4e37-87f3-2a516b658872.png">

6. In **Add Statement**, Under Principal--> Allow all **(*)**,
   - Under Actions, Select **GetObject**

<img width="919" alt="Screenshot 2022-09-22 at 13 59 31" src="https://user-images.githubusercontent.com/102330725/191753525-38b41c1c-474f-41d8-804f-afca6a729688.png">

7. Add the bucket **ARN**, add a slash and asterik after the bucket name **(/*)**. 
   - Once Done, Click on **Add Statement**

<img width="906" alt="Screenshot 2022-09-22 at 14 03 51" src="https://user-images.githubusercontent.com/102330725/191754403-15ed3100-1a3d-428b-b98b-89a7ee9e4923.png">

  - Click on **Generate Policy**
<img width="994" alt="Screenshot 2022-09-22 at 14 05 11" src="https://user-images.githubusercontent.com/102330725/191754704-15d5b9c6-55eb-40bf-8d5b-fcbaa276136f.png">

8. Copy the generated policy and based it back under **Bucket Policy**
<img width="817" alt="Screenshot 2022-09-22 at 14 08 36" src="https://user-images.githubusercontent.com/102330725/191755492-63cb7ac1-d892-47bb-b087-df695945fd7b.png">

9. The policy 
<img width="1246" alt="Screenshot 2022-09-22 at 14 10 36" src="https://user-images.githubusercontent.com/102330725/191755935-f01ff3d3-eb48-4939-adad-aa8b27fbfae8.png">
<img width="997" alt="Screenshot 2022-09-22 at 14 12 24" src="https://user-images.githubusercontent.com/102330725/191756318-4e3598ad-6009-4d2b-85fc-117c484ea063.png">
