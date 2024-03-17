# SKILL-TEST-WEBSITE
Andres Gutierrez Application 

## Fix verification issue on register and login.
The issue related to verification was due to the configuration of a valid email provider for sending emails. This involved changing the values either in the emailer service in the backend or in the environment variables.

<img src="https://github.com/anfegu/skill-test-website/assets/7240030/5f8fbb77-0f4a-4552-8b89-eea692932cf4" width="45%">
<img src="https://github.com/anfegu/skill-test-website/assets/7240030/08edde31-a333-449c-be2f-9f0920b5bf3b" width="45%">
<img src="https://github.com/anfegu/skill-test-website/assets/7240030/e2b0e1ad-8831-42a4-afa0-f438050da4a8" width="45%">
<img src="https://github.com/anfegu/skill-test-website/assets/7240030/c77eda29-c8e4-4d7d-8283-8cd7a064ae3a" width="45%">
<img src="https://github.com/anfegu/skill-test-website/assets/7240030/931d8ac1-ada3-4716-b0d8-545f64d8a03b" width="45%">
<img src="https://github.com/anfegu/skill-test-website/assets/7240030/24ae0f1c-6e85-4063-9dd3-3bfe13c6241f" width="45%">
<img src="https://github.com/anfegu/skill-test-website/assets/7240030/a57b4faf-b146-4c65-b352-9d996a7a2d97" width="45%">
<img src="https://github.com/anfegu/skill-test-website/assets/7240030/0aee5f5b-eb68-47d6-9900-fec2a03824ee" width="45%">
<img src="https://github.com/anfegu/skill-test-website/assets/7240030/48229c24-d399-49c6-adab-8e85a6bb6129" width="45%">
<img src="https://github.com/anfegu/skill-test-website/assets/7240030/0aebe7f1-d4df-47d7-a8cb-ef8d371f2b7c" width="45%">
<img src="https://github.com/anfegu/skill-test-website/assets/7240030/709cc265-0e7e-469f-a6ef-a4b8358e7f0d" width="45%">

> [!NOTE]
> Regarding sensitive information exposed in environment variables such as API keys, improvements were made both in the backend (DB, emailer, etc.) and in the frontend (firebaseConfig), as can be seen in the repository commits.

## Add current Eth price on profile page.
The current Ethereum price is added to the profile page by querying the asset and position in the WalletPortfolio view through `props.tokensInfo`. This was facilitated by adding the Ethereum network to the wallet table.

<img src="https://github.com/anfegu/skill-test-website/assets/7240030/795fa9a7-8d92-4487-8029-7c5ead1ab1b1">
<img src="https://github.com/anfegu/skill-test-website/assets/7240030/b69cf95d-203f-4199-b8f5-73a030252d34" width="25%">
<img src="https://github.com/anfegu/skill-test-website/assets/7240030/7ca51680-7868-481d-a861-e048aeda9e0d" width="55%">
<img src="https://github.com/anfegu/skill-test-website/assets/7240030/7cbf534e-66c1-4e3f-b584-5532b425b6dc" width="55%">
<img src="https://github.com/anfegu/skill-test-website/assets/7240030/0ddf4ffa-d7d4-4c7f-8221-f2a456c50e82" width="90%">

> [!NOTE]
> Design patterns or database-driven dynamism could be applied to optimize blockchain network scaling.

## Add Wallet connect on profile page.
Integrating WalletConnect functionality enables secure communication between wallets and Dapps. WalletConnect establishes a remote connection between two apps/devices, with data transmitted through a bridge server. The connection is initiated by one peer displaying a QR Code or deep link with a standard WalletConnect URI and is established when the counter-party approves the connection request.

**Components:**
A "Connect with WalletConnect" button has been added to the wallet profile page. Evidence of the implementation can be found in repo commit and provided video.

**Example URI:**
wc:e0d3bcf6-6727-4103-89a2-2d1ba7cd727b@1?bridge=https%3A%2F%2F3.bridge.walletconnect.org&key=8e5ed284153adab543b75f25093878593768eacfd618c5484b7d2987bb5fb9d6

<img src="https://github.com/anfegu/skill-test-website/assets/7240030/a07050e7-852c-440e-b78e-d33a4bd687bd" width="70%">
<img src="https://github.com/anfegu/skill-test-website/assets/7240030/233e3f31-0b25-4469-bea0-ecd7e4b6a2ec" width="60%">

> [!NOTE]
> GENERAL: Remember to execute the updated scripts (`new_mgldefi.sql`) from the database to simulate the changes. Using the root user in MySQL is discouraged due to security risks. It's best practice to create separate users with specific permissions for each database task. This adheres to the principle of least privilege, enhances security, facilitates auditing, isolates system components, and simplifies scalability and maintenance. Storing credentials securely in a .env file adds an extra layer of protection against unauthorized access. For the operational convenience of the application, I've decided to retain the .env file within the project. it's important to upholding robust security practices, including the creation of distinct MySQL users with limited privileges:
-- Create a new user
CREATE USER 'myuser'@'localhost' IDENTIFIED BY 'mypassword';

-- Grant permissions to the user on a specific database
GRANT SELECT, INSERT, UPDATE, DELETE ON mydatabase.* TO 'myuser'@'localhost';

-- Flush privileges to apply changes
FLUSH PRIVILEGES;

> 
[Screencast from 2024-03-17 02-19-26.webm](https://github.com/anfegu/skill-test-website/assets/7240030/fbba236e-c5e9-4f8c-8654-623a6a002848)

