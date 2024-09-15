# CTriStateChecked Component

## Overview

`CTriStateChecked` is a simple tri-state checkbox component designed for React applications. It allows users to toggle between three states: checked, unchecked, and indeterminate. This component supports dynamic interaction and can be integrated easily into forms or other UI elements.

## Features

- **Tri-State Functionality**: Allows for three states: checked, unchecked, and indeterminate.
- **Dynamic Enabling/Disabling**: The checkbox can be toggled between enabled and disabled states based on user interaction.
- **Customizable Label**: You can set a label next to the checkbox for better context.
- **Event Handling**: Provides an `onChange` callback to handle changes in state.

## Props

| Prop Name   | Type     | Description                                                                 |
|-------------|----------|-----------------------------------------------------------------------------|
| `txtLabel`  | `string` | Text displayed next to the checkbox.                                       |
| `disabled`  | `boolean`| Initial state of the checkbox (disabled or enabled). Clicking it will toggle the state. |
| `checked`   | `boolean`| Initial state of the checkbox (checked or unchecked).                      |
| `onChange`  | `function` | Callback function triggered when the checkbox state changes. The function receives two parameters: `is_enabled` and `is_checked`. |

### Parameters for `onChange`

- **is_enabled**: A boolean indicating whether the checkbox is currently enabled.
- **is_checked**: A boolean indicating the current checked state of the checkbox.

## Sample Usage

Here's a basic example of how to use the `CTriStateChecked` component in your application:

    
    import React, { useEffect } from 'react';
    import CTriStateChecked from './CTriStateChecked'; // Adjust the import path as necessary
    
    const Test = () => {
      useEffect(() => {
        // Any side effects can be placed here
      }, []);
    
      const onChanged = (is_enabled, is_checked) => {
        console.log("is_checked:", is_checked);
        console.log("is_enabled:", is_enabled);
      };
    
      return (
        <div>
          <CTriStateChecked 
            txtLabel='Server Comm' 
            disabled={false}   // Set to false to allow interaction
            checked={true}     // Initial state set to checked
            onChange={onChanged} // Pass the change handler
          />
        </div>
      );
    };
    
    export default Test;