GitHub - opsworks-co/nexus-docker-images-cleaner: Python script to clean nexus 3 docker repository images
Link to the github repository for reference. 

Firstly we pushed some images in our nexus repository:
For that:
![image](https://user-images.githubusercontent.com/97760794/222100463-abf8497d-aeab-40c4-8993-fe485582199b.png)

Pull then tag then push into nexus repository.
![image](https://user-images.githubusercontent.com/97760794/222100546-df92d221-62a6-48ae-8f47-1f23dca040f2.png)


Then push:
![image](https://user-images.githubusercontent.com/97760794/222100599-df122beb-21d8-4bc4-b5bd-627cab1006bc.png)


We, can cleanup the docker images in nexus using different methods such as:
By creating cleanup policies on the UI itself:
There it will cleanup based on 
![image](https://user-images.githubusercontent.com/97760794/222100663-ddb0aae1-ca08-4fa0-a0c8-1f61c19d5941.png)


BUT,
We will prefer an automated approach as in companies there are thousands of repositories in their nexus registry.

So basically we used a python script for automation:
We did all the necessary changes such as port, username, password in the file.
![image](https://user-images.githubusercontent.com/97760794/222100718-90ac3243-db4a-4314-892b-a9f7897f394b.png)


After running these commands as we saw it got deleted: but when we'll see the nexus repository, it will not have got deleted from there. 
So, for that we need to create task on the nexus:
![image](https://user-images.githubusercontent.com/97760794/222100776-5278f8d8-f879-4933-8e17-0ff490a8ae63.png)
![image](https://user-images.githubusercontent.com/97760794/222100876-b50f9023-d10f-4c93-8de9-f316be3efbf2.png)


After running this particular task, we'll see in the blob storage that the space will get free and the images will get actually deleted.


Before:
![image](https://user-images.githubusercontent.com/97760794/222100958-6b324739-2304-4b21-aa22-5a5644021d37.png)

AFTER:
![image](https://user-images.githubusercontent.com/97760794/222101027-2a3f4418-b4b3-4444-8a43-c052e01ee9c4.png)
