# Smart-Trolley-System

## Overview

The **Smart Trolley System with Automatic Billing** is a modernized shopping cart solution that automates the process of billing and item removal using **RFID technology** and **GSM** for payment notifications. This project uses an **Arduino Nano**, **RFID** for product detection, a **GSM Module** for SMS-based billing, and a **LCD** for displaying product details and total price.

### Key Features:

* **RFID Product Detection**: Each item is tagged with an RFID tag. When placed in the cart, the product details are displayed on an LCD screen.
* **Automatic Billing**: The system automatically updates the total price based on the products added or removed.
* **SMS Notification**: When the checkout is completed, a **GSM module** sends an SMS to the user with the bill details and payment instructions.
* **Item Removal**: Items can be removed by scanning the RFID tag and pressing a button.
* **Visual Indicators**: **LEDs** indicate actions (e.g., product added, removed, or errors).

## Components Used

* **Arduino Nano** – The main controller for processing data.
* **RFID Reader (EM-18)** – Detects the RFID tag attached to each product.
* **RFID Tags** – Each product is assigned a unique RFID tag for identification.
* **SIM800L GSM Module** – Sends the SMS notifications with the total bill.
* **20x4 LCD Display with I2C** – Displays product details, prices, and the total bill.
* **Push Buttons** – For removing items from the cart or sending the final bill.
* **LEDs (Red/Green)** – For indicating various states (item added/removed, error).
* **Buzzer** – To alert when an item is added or removed.
* **3.7V Li-ion Battery** – Powers the entire system.

## Bill of Materials

| S.No | Component                 | Quantity |
| ---- | ------------------------- | -------- |
| 1    | Arduino Nano              | 1        |
| 2    | 20x4 LCD Display with I2C | 1        |
| 3    | SIM800L GSM Module        | 1        |
| 4    | EM-18 RFID Reader         | 1        |
| 5    | EM-18 RFID Tag            | 4        |
| 6    | Push Button               | 2        |
| 7    | Red LED                   | 1        |
| 8    | Green LED                 | 1        |
| 9    | Buzzer                    | 1        |
| 10   | 3.7V Li-ion Battery       | 1        |

## Circuit Diagram

The circuit consists of:

* **Arduino Nano** connected to the **RFID reader**, **LCD Display**, **GSM module**, and other components.
* The **RFID reader** is connected via UART to the Arduino for serial communication.
* **Push buttons** for removing items or sending bills.
* **LEDs** and **buzzer** for visual/audio feedback.

Here’s a simple circuit diagram to visualize the wiring:

![Circuit Diagram](https://example.com/smart-trolley-circuit.png)

## Installation

### Prerequisites:

* **Arduino IDE**: Install the Arduino IDE from [here](https://www.arduino.cc/en/software).
* **Libraries**: Install the required libraries:

  * `LiquidCrystal_I2C`: For controlling the LCD.
  * `Wire`: For I2C communication.

### Setup:

1. **Clone the repository**:

   ```bash
   git clone https://github.com/your-username/smart-trolley-system.git
   cd smart-trolley-system
   ```

2. **Install Dependencies**:
   In the Arduino IDE, install the necessary libraries:

   * **LiquidCrystal\_I2C**: Available through Library Manager in Arduino IDE.

3. **Upload the Code**:
   Open the **smart\_trolley\_system.ino** file in the Arduino IDE and upload it to your Arduino Nano.

4. **Power the System**:
   Connect your **Arduino Nano** to a power source (e.g., a 3.7V Li-ion battery).

5. **Run the System**:
   When you power on the system, the LCD will display a welcome message, and you can start adding items by scanning the RFID tags.


## Working

* **Adding Items**: When an RFID tag is scanned, the corresponding product (e.g., Butter, Milk, Tea) is added to the cart. The product name, price, and updated total will be displayed on the LCD screen.
* **Removing Items**: If the user wants to remove an item, they press a button and scan the RFID tag again. The item is removed, and the total is updated accordingly.
* **Checkout**: The shopkeeper can press the checkout button, and an SMS with the total bill is sent to the customer's phone.

## Conclusion

The **Smart Trolley System with Automatic Billing** provides a convenient and efficient way for users to track their purchases in real-time. By integrating RFID and GSM technologies, the system enables an easy and automated checkout process.

### Future Work:

* Direct UPI payment integration for seamless payments.
* Improve security features like user authentication for more personalized experiences.


