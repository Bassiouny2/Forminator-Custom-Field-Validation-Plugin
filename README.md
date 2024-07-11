# Forminator Custom Field Validation Plugin

This WordPress plugin provides custom validation for form fields in the Forminator plugin. It validates specific form fields based on predefined validation rules, such as ensuring a field contains exactly 14 numeric characters.

## Description

The `[Forminator] - Validation form fields` plugin allows you to define custom validation rules for specific fields in your Forminator forms. This example demonstrates how to validate a form field to ensure it contains exactly 14 numeric characters.

## Installation

1. **Download the Plugin:**
   - Clone the repository or download the zip file.
   - If downloading the zip file, extract it to get the plugin folder.

2. **Upload the Plugin:**
   - Upload the plugin folder to the `/wp-content/plugins/` directory of your WordPress site.

3. **Activate the Plugin:**
   - Activate the plugin through the 'Plugins' menu in WordPress.

## Usage

1. **Define Validation Rules:**
   - Edit the plugin file to set the form ID and field name you want to validate.
   - Customize the validation pattern and error message as needed.

2. **Example Configuration:**
   ```php
   private $form_custom_validation_list = array(
       array(
           'form_id'                  => '251', // form id.
           'field_name'               => 'forminator-field-text-1_668ffc99df9a1', // the field name that you want to validate.
           'field_validation_pattern' => array(
               '/^\d{14}$/', // Validation for exactly 14 numeric characters.
           ),
           'error_message'            => 'The national ID must be exactly 14 digits.', // error message.
       ),
   );
