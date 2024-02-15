# SMART Voting System

The SMART Voting System is designed to streamline and secure the voting process, offering administrators and voters a convenient and efficient platform.

## Table of Contents
- [Introduction](#introduction)
- [Voter's Interface](#voters-interface)
- [Admin Interface](#admin-interface)
- [Key Features](#key-features)
- [Data Structures Used](#data-structures-used)
- [Advantages of Using SMART Voting System](#advantages-of-using-smart-voting-system)
- [Installation](#installation)
- [Contributing](#contributing)

## Introduction

The Smart Voting System facilitates secure and efficient voting processes, providing both administrators and voters with a user-friendly interface. Here are the two interfaces in the Smart voting system:

### Voter's Interface

Voter first needs to enter id and password for them to be able to access their portal. the user's information along with its encrypted password is saved in a CSV file (eligible_voters.csv). Once the user and password is matched with the one in the csv file the voter is allowed to access his portal. Following are the functionalities that the Voter has within its interface:

1. **See Location**
   - Description: View the polling station location.
   - Functionality: Allows the voter to see where their polling station is located. Additionally, provides an option to request a change of polling station if the voter is not in the area of voting stations.

2. **Change Password**
   - Description: Change the voter's password.
   - Functionality: Enables the voter to change their password for security purposes. and that password is further encrypted and then stored

3. **Vote**
   - Description: Cast a vote for a candidate.
   - Functionality: Allows the voter to cast their vote, but only if voting is currently allowed by the admin.

### Admin Interface

The admin is first required to enter user and password, the admin's user and password is hardcoded in the program. The password is: admin. Following is the functionality within the admin interface:

1. **Allow Voting**
   - Description: Enable or disable voting for voters.
   - Functionality: The admin can toggle the ability for voters to cast their votes. If voting is not allowed, voters will not be able to cast their votes until the admin enables it.

2. **Add Voter**
   - Description: Add a new voter to the system.
   - Functionality: Provides the admin with the authority to add new voters to the system, including their information such as ID, name, password, and location.

3. **Edit Voter's Info**
   - Description: Modify a voter's information.
   - Functionality: Allows the admin to edit the information of existing voters, including their name, password, and location.

4. **Check Notifications**
   - Description: Review change requests from voters.
   - Functionality: Displays notifications regarding change requests from voters, such as requests to change their polling station location. The admin can then choose to accept or reject these requests.

5. **Release Vote**
   - Description: Calculate votes and release results.
   - Functionality: Calculates the votes for each candidate and releases the results to determine the outcome of the voting process.

## Key Features

**Voter Management:** Stores voter information (ID, name, password, location, vote status) in a CSV file.

**Secure Password Storage:** Encrypts passwords using a simple Caesar cipher (can be enhanced for stronger security).

**Voting Queue:** Manages the order of voters casting their votes through a queue system.

**Vote Casting:** Simulates the voting process and stores votes in a CSV file.

**Vote Counting:** Counts votes for each candidate and provides results.

**Voting Queue:** A queue system processes votes efficiently, updating voter vote status upon completion. this system makes sure that nobody votes with dishonest means by mmaking sure that one person is not able to vote twice. a voter that has voyted once, ha sthe voting status update d and that ,means that he cannot vote again.

**Data Structures Used:**

- **Maps:** Used for storing voter details in the AdminInterface and VotersInterface for efficient retrieval and dynamic updates
- **Queues:** Used to implement a queue for processing votes in the VotingQueue class.
- **Vectors:** Used for temporarily storing lines read from files during the loading of voter and candidate data.
- **Stack:** Used to store the number of attempts of password of a voter and admin before denying their access.

## Advantages of Using SMART Voting System

### Efficiency & Convenience:
- Remote voting for user convenience.
- Efficient admin management of voter and candidate data.

### Transparency:
- Clear record of cast votes.
- Transparent candidate list for voters.

### Security:
- Password encryption using Caesar cipher.
- Secure access for eligible voters.

### Accessibility:
- Voter location change requests.
- Flexibility in managing account details.
- Real-time notifications for admin alerts and quick response to change requests.

## Installation

1. Clone the repository to your local machine.
2. Compile and run the SMART voting system using your preferred C++ compiler.
3. Follow the on-screen instructions to explore the functionalities.

## Contributing

Contributions are welcome! If you'd like to contribute, please follow the guidelines in the [CONTRIBUTING.md](CONTRIBUTING.md) file.

Good luck with exploring the SMART Voting system!
