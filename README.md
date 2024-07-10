# Celebrity Manager

This project is a user interface for managing a list of the world's most famous celebrities. The interface allows you to view, edit, and delete celebrity details while hiding their public presence.

## Project Demonstration Video
https://github.com/shivanshu-srm/RA2111003010931_Factwise_BE/assets/103733101/31d82d53-ec87-4520-bf56-76308ae0fc7a

## Features

1. **User Interface**: The UI is designed based on the provided design specifications.
2. **Search Functionality**: A search bar is available to search the list by celebrity name.
3. **Accordion List**: The user list is displayed as an accordion.
    - Clicking on an item enlarges it and collapses all others.
    - Clicking the same item again will collapse it.
    - Accordion items manage + and - icons to indicate their state.
4. **Fetch and Display Data**: Celebrity details are fetched from a JSON file.
    - Age is calculated based on the date of birth.
    - Gender is a dropdown field.
    - Country is a text field.
    - Description is a text area.
5. **Edit and Delete Functionality**:
    - **Edit Mode**: Allows editing of details in place.
        - Only adults can be edited.
        - Validation prevents text input in the age field, numbers in the nationality field, and empty fields.
        - Save button is disabled until changes are made.
        - Save button updates details, while Cancel reverts to the last known state.
        - No other accordion can be opened in edit mode.
    - **Delete Mode**: Prompts confirmation before deletion.

## Setup Instructions

1. **Clone the repository**:
    ```sh
    git clone https://github.com/yourusername/celebrity-manager.git
    ```
2. **Navigate to the project directory**:
    ```sh
    cd celebrity-manager
    ```
3. **Install dependencies**:
    ```sh
    npm install
    ```
4. **Start the development server**:
    ```sh
    npm start
    ```

## Project Structure

- `src/`
  - `components/`
    - `AccordionItem.tsx`: Component for individual accordion items.
    - `CelebrityList.tsx`: Component for the list of celebrities.
    - `SearchBar.tsx`: Component for the search bar.
  - `utils/`
    - `calculateAge.ts`: Utility function to calculate age from date of birth.
    - `validators.ts`: Utility functions for form validation.
  - `App.tsx`: Main application component.
  - `index.tsx`: Entry point for the React application.
  - `styles/`: Folder containing all the CSS files.

## Main Functionalities

### User Interface

The user interface is designed to match the provided design specifications, featuring a clean and intuitive layout for managing celebrity details.

### Search Bar

The search bar allows users to quickly find a celebrity by typing their name. The list updates dynamically as the user types.

### Accordion List

- Clicking on an accordion item expands it, showing the details, while collapsing all other items.
- Clicking the same item again will collapse it.
- The + and - icons indicate whether the accordion is open or collapsed.

### Fetch and Display Data

- The application fetches celebrity data from a JSON file.
- Age is calculated using the provided date of birth.
- Gender is displayed as a dropdown menu.
- Country and description are displayed in text fields and text areas respectively.

### Edit and Delete Functionality

- **Edit Mode**:
  - Only adults (age 18 and above) can be edited.
  - Input validation prevents text in the age field, numbers in the nationality field, and empty fields.
  - The Save button is disabled until changes are made.
  - Clicking Save updates the details; clicking Cancel reverts changes.
  - No other accordion can be opened while in edit mode.
- **Delete Mode**:
  - A confirmation prompt ensures the user wants to delete the celebrity.
  - Confirming the deletion removes the celebrity from the list.

## Technologies Used

- ReactJS
- TypeScript (optional but recommended)
- CSS

