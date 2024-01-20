# Staff Management Project

This project provides a method to save staff information to MongoDB with server-side validation and data sanitization.

## Getting Started

Follow the steps below to set up and run the project on your local machine.

### Prerequisites

- Node.js
- MongoDB

### Installation

Step 1: Clone the repository:

  command: git clone https://github.com/rajarammanikanta/HealTether-task.git


Step 2: Navigate to the project directory: 
  command: cd HealTether

Step 3: Install dependencies:   
   command: npm install  

Step 4: create a new cluster in mangodb atlas and get a connection string 
   note: make sure that you need you install mangodb compass in that paste the connection string and connect to mangodb    
   string is look example:  mongodb+srv://<username>:<password>@ClusterName.tmuuqhb.mongodb.net/  
   
   after it successfully connected you have to paste the connection string with your usename and password in the given code as it present in index.js file  

        code: 
        mongoose.connect("connectionString", {
            dbName: "databasename",
            
        useNewUrlParser: true,
        useUnifiedTopology: true,
        
        });

        
Step5: Now we have to run the code using command  
   command: node index.js    


Step6: once it is successfully done you can see the localhost url like  
   example:  https://localhost:3000   

Step 7: To validate data use postman API in that you have to use POST method and paste the url   
   example:  https://localhost:3000/savestaff   

Step 8: Create a dummy data for the object as we mentioned in the staff.model.js file once dummy data is created you have to paste it in the body choose raw>>JSON(as type)   
   
   dummy data example: 

    {

    "staffId": "S12345",
    "firstName": "John",
    "lastName": "Doe",
    "specialization": "General Physician",
    "isDoctor": true,
    "age": 35,
    "birthday": "1987-05-15",
    "gender": "Male",
    "mobile": "9876543210",
    "countryCode": "+91",
    "whatsapp": "9876543210",
    "email": "john.doe@example.com",
    "address": {
        "house": "123 Main Street",
        "street": "Downtown Avenue",
        "landmarks": "Near City Park",
        "city": "Metropolis",
        "pincode": "56789"
    },
    "documentType": "Aadhar Card",
    "documentNumber": "1234-5678-9012",
    "upiId": "john.doe@upi",
    "bankName": "City Bank",
    "accountName": "John Doe",
    "accountNo": "9876543210",
    "ifsc": "CITY012345",
    "isAdmin": false,
    "created": {
        "on": "2022-01-25T12:30:00Z",
        "by": {
        "id": "admin123",
        "name": "Admin User"
        }
    },
    "modified": {
        "on": "2022-01-26T15:45:00Z",
        "by": {
        "id": "admin456",
        "name": "Another Admin"
        }
    },
    "profilePic": "profile.jpg",
    "documents": ["document1.pdf", "document2.pdf"],
    "deleted": false
    }



Step 9: Once you click send button you can see "staff saved succesfully" messsage   



     