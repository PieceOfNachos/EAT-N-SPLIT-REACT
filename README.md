# EAT-N-SPLIT

This React application allows users to manage their friends and split bills between them. The app features:

- Adding and selecting friends
- Splitting bills between selected friends
- Tracking debts and balances with friends

## Table of Contents
- [Installation](#installation)
- [Usage](#usage)
- [Components](#components)
  - [App](#app)
  - [Button](#button)
  - [FriendsList](#friendslist)
  - [Friend](#friend)
  - [FormAddFriend](#formaddfriend)
  - [FormSplitBill](#formsplitbill)
- [Contributing](#contributing)
- [License](#license)

## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/your-username/friends-split-bill-app.git
    ```
2. Navigate to the project directory:
    ```bash
    cd friends-split-bill-app
    ```
3. Install the required dependencies:
    ```bash
    npm install
    ```
4. Start the development server:
    ```bash
    npm start
    ```

## Usage

Once the server is running, you can interact with the app through your browser. You can:

- View a list of friends with their balances.
- Add a new friend by clicking the "Add friend" button.
- Select a friend to split a bill.
- Split a bill by entering the bill amount and how much you paid.

## Components

### App

The main component that manages the application's state, including the list of friends, adding new friends, selecting a friend, and splitting bills.

- **State:**
  - `friends`: Manages the list of friends and their balances.
  - `showAddFriend`: Controls whether the "Add Friend" form is visible.
  - `selectedFriend`: Tracks the currently selected friend for splitting bills.

- **Functions:**
  - `handleShowAddFriend`: Toggles the visibility of the "Add Friend" form.
  - `handleAddFriend`: Adds a new friend to the list.
  - `handleSelection`: Selects or deselects a friend.
  - `handleSplitBill`: Adjusts the balance after splitting a bill.

### Button

A reusable button component. It accepts the following props:

- `children`: The label displayed inside the button.
- `onClick`: A function that is triggered when the button is clicked.

### FriendsList

Renders a list of friends and allows selecting a friend. It receives the following props:

- `friends`: An array of friend objects.
- `onSelection`: A callback to handle friend selection.
- `selectedFriend`: The currently selected friend.

### Friend

Renders an individual friend's details, such as their name, image, and balance. It receives the following props:

- `friend`: A friend object containing id, name, image, and balance.
- `onSelection`: A callback for selecting a friend.
- `selectedFriend`: The currently selected friend to show different styles.

### FormAddFriend

Allows the user to add a new friend. It handles the form state, including:

- `name`: The name of the friend.
- `image`: The image URL of the friend.
- `handleSubmit`: A function to add a new friend when the form is submitted.

### FormSplitBill

Handles splitting the bill between the user and a selected friend. It manages:

- `bill`: The total value of the bill.
- `paidByUser`: How much the user paid.
- `paidByFriend`: Automatically calculated based on the bill and user’s payment.
- `whoIsPaying`: Tracks whether the user or friend is paying the bill.
- `handleSubmit`: Submits the split bill calculation.

## Contributing

Contributions are welcome! If you'd like to contribute to this project, please fork the repository and submit a pull request.

## License

This project is licensed under the MIT License.
