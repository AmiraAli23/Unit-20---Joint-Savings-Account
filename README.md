# Unit 20 - Joint-Savings-Account


![image](https://user-images.githubusercontent.com/99091066/179320705-4eea9782-020b-4c43-96e3-242dbe59f283.png)

In this project, we were tasked to create a Solidity smart contract that accepts two user addresses. These addresses will be able to control a joint savings account. The smart contract will use ether management functions to implement a financial institution’s requirements for providing the features of the joint savings account. These features will consist of the ability to deposit and withdraw funds from the account.


Step 1: Create a Joint Savings Account Contract in Solidity



Define a new contract named JointSavings.


Define the following variables in the new contract:


Two variables of type address payable named accountOne and accountTwo, a variable of type address public named lastToWithdraw, and two variables of type uint public named lastWithdrawAmount and contractBalance.

<img width="719" alt="Screen Shot 2022-07-16 at 3 39 50 PM" src="https://user-images.githubusercontent.com/99091066/179369686-51cdc022-1f0c-490d-bd9b-abb774f24aa6.png">


Define a require statement that checks if recipient is equal to either accountOne or accountTwo. If it isn’t, the require statement returns the “You don't own this account!” text.


<img width="692" alt="Screen Shot 2022-07-16 at 3 41 12 PM" src="https://user-images.githubusercontent.com/99091066/179369711-2eeb9da9-4cb2-4739-b621-bde418559848.png">



Define a require statement that checks if balance is sufficient for accomplishing the withdrawal operation. If there are insufficient funds, it returns the “Insufficient funds!” text.


<img width="521" alt="Screen Shot 2022-07-16 at 3 41 41 PM" src="https://user-images.githubusercontent.com/99091066/179369722-6de33c53-26ff-45bf-bf2e-883bd2d86545.png">


Add an if statement to check if lastToWithdraw is not equal (!=) to recipient. If it’s not equal, set it to the current value of recipient.

<img width="307" alt="Screen Shot 2022-07-16 at 3 42 27 PM" src="https://user-images.githubusercontent.com/99091066/179369742-2e5d2ed4-4531-4e14-9ac1-4436c2c5a491.png">

Call the transfer function of the recipient, and pass it the amount to transfer as an argument.

<img width="268" alt="Screen Shot 2022-07-16 at 3 42 58 PM" src="https://user-images.githubusercontent.com/99091066/179369757-a171eb74-ec8b-47c4-8c29-a3a04269e8b8.png">

Set lastWithdrawAmount equal to amount.

<img width="228" alt="Screen Shot 2022-07-16 at 3 43 11 PM" src="https://user-images.githubusercontent.com/99091066/179369772-73fbeaa7-9820-474d-a656-516027d879c4.png">


Set the contractBalance variable equal to the balance of the contract by using address(this).balance to reflect the new balance of the contract.

<img width="305" alt="Screen Shot 2022-07-16 at 3 43 21 PM" src="https://user-images.githubusercontent.com/99091066/179369792-e1d9a7f9-e637-4b20-9746-a0fe0b4b206d.png">


Define a public payable function named deposit. In this function, code the following:

Set the contractBalance variable equal to the balance of the contract by using address(this).balance.

<img width="525" alt="Screen Shot 2022-07-16 at 3 43 50 PM" src="https://user-images.githubusercontent.com/99091066/179369824-7009d41b-30eb-48c6-8f4b-3b93325a341b.png">



Define a public function named setAccounts that takes two address payable arguments, named account1 and account2. In the body of the function, set the values of accountOne and accountTwo to account1 and account2, respectively.

<img width="179" alt="Screen Shot 2022-07-16 at 3 44 29 PM" src="https://user-images.githubusercontent.com/99091066/179369847-aa8c5861-aa44-476d-aa62-4c3ab34558a7.png">


Add a fallback function so that your contract can store ether that’s sent from outside the deposit function.

<img width="249" alt="Screen Shot 2022-07-16 at 3 44 41 PM" src="https://user-images.githubusercontent.com/99091066/179369859-d4cd171d-70e3-44cb-b07b-deb59e247a85.png">












