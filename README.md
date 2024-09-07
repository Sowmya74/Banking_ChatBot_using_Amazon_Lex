# Banking ChatBot using Amazon Lex 
a practical chatbot, BankerBot, that can help bank's customers check their account balance and transfer money between accounts!

![Banker_Bot](https://www.flaticon.com/free-animated-icon/chatbot_11260829?term=chatbot&page=1&position=4&origin=search&related_id=11260829)

## Overview 

![Chatbot Icon](https://www.flaticon.com/free-animated-icon/chatbot_12205168?term=chatbot&page=1&position=7&origin=search&related_id=12205168)
This project demonstrates how to create a conversational interface for banking services using AWS technologies. BankerBot is designed to provide assistance and handle queries related to account balances, fund transfers, and other basic banking operations.

## Key Features

- Natural language understanding for banking queries
- Account balance inquiries
- Fund transfers between accounts
- Secure handling of sensitive banking information

## Technologies Used

- Amazon Lex: Used to build the conversational interface and handle natural language understanding.
- Amazon Lambda: Used to execute the backend logic and interact with external banking services.

### Intents and Slots

- Welcome: Greets the user and provides initial instructions.
- Fallback: Handles unexpected or unknown user inputs.
- CheckBalance: Checks the user's account balance.
                              Slot: accountType (e.g., "checking", "savings")
- FollowupCheckBalance: Handles follow-up questions related to account balance.
- TransferFunds: Transfers funds between accounts.
                            Slots: accountType, dateOfBirth, amount, recipientAccountType, recipientAccountNumber
### Lambda Function

- BankingBotEnglish: Handles the backend logic for each intent.
- Connects to the banking system (e.g., a REST API) to retrieve account information and perform transactions.
- Implements security measures to protect sensitive user data.
- Provides appropriate responses based on the intent and slot values.

## Documentation 

![BankerBot](https://www.flaticon.com/free-animated-icon/chat-bot_11184177?term=chatbot&page=1&position=3&origin=search&related_id=11184177)

For complete setup instructions, architecture details, and implementation guidelines, please refer to the following resources:

1. **Full Documentation PDF**: Find the comprehensive project documentation in the `docs` folder of this repository. This PDF contains detailed information on setting up the Lex bot, configuring the Lambda function, and integrating with banking systems.

2. **Canva**: For a visual overview of the project pdf, please view at [BankerBot Canva]([https://www.canva.com/design/DAFxyz123/view](https://www.canva.com/design/DAGP0o7PBG8/RGXvNBZOPrWKSw4K4dLceQ/view?utm_content=DAGP0o7PBG8&utm_campaign=designshare&utm_medium=link&utm_source=editor)) .

## Usage Examples

```
User: "What's my checking account balance?"
BankerBot: "Your checking account balance is $1,500.00."

User: "Transfer $100 from my savings to my checking account."
BankerBot: "Certainly! I'll need a few details to process that transfer..."
```

## Security Considerations

- Security: Implement robust security measures to protect sensitive user data, such as using encryption and authentication.
- Error Handling: Handle potential errors and provide informative feedback to the user.
- Scalability: Ensure your Lambda function can handle increased traffic.
- Integration: Consider integrating BankerBot with other banking systems or APIs for more advanced features.


## Future Enhancements

- Expand Functionality: Add more intents and banking features to BankerBot, such as checking account history, setting up recurring payments, or providing financial advice.
- Personalization: Customize responses based on user preferences or previous interactions.
- Integration with Other Services: Integrate BankerBot with other AWS services like Amazon Connect for voice-based interactions or Amazon DynamoDB for data storage.
