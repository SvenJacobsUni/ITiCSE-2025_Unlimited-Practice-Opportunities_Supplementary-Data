# Input
- Programming Concept: While loops;Boolean and None
- Context: Streaming Services

# Generated Task Components
## Task Description
### Practice Task: Streaming Services and Subscription Status

Write a function named `check_subscription_status(user_status)`, which checks the subscription status of a user in a streaming service. The function should use a while loop to check the status until the user either has an active subscription or the status is `None`.

- If the status is `True`, the function should output "Subscription active".
- If the status is `False`, the function should output "Subscription inactive".
- If the status is `None`, the function should output "Status unknown" and end the loop.

Example call:
```python
check_subscription_status([False, False, True, None])
```

Expected output:
```
Subscription inactive
Subscription inactive
Subscription active
```

## Code Framework
```python
def check_subscription_status(user_status):
    ## Insert code here
```

## Model Solution
```python
def check_subscription_status(user_status):
    i = 0
    while i < len(user_status):
        status = user_status[i]
        if status is True:
            print("Subscription active")
            break
        elif status is False:
            print("Subscription inactive")
        elif status is None:
            print("Status unknown")
            break
        i += 1

check_subscription_status([False, False, True, None])
```

## Unit Tests
```python
import unittest
from main import check_subscription_status
from io import StringIO
import sys

class TestCheckSubscriptionStatus(unittest.TestCase):
    def test_subscription_active(self):
        captured_output = StringIO()
        sys.stdout = captured_output
        check_subscription_status([False, False, True, None])
        sys.stdout = sys.__stdout__
        self.assertEqual(captured_output.getvalue().strip(), "Subscription inactive\nSubscription inactive\nSubscription active")

    def test_subscription_inactive(self):
        captured_output = StringIO()
        sys.stdout = captured_output
        check_subscription_status([False, None])
        sys.stdout = sys.__stdout__
        self.assertEqual(captured_output.getvalue().strip(), "Subscription inactive\nStatus unknown")

    def test_status_unknown(self):
        captured_output = StringIO()
        sys.stdout = captured_output
        check_subscription_status([None])
        sys.stdout = sys.__stdout__
        self.assertEqual(captured_output.getvalue().strip(), "Status unknown")

    def test_empty_list(self):
        captured_output = StringIO()
        sys.stdout = captured_output
        check_subscription_status([])
        sys.stdout = sys.__stdout__
        self.assertEqual(captured_output.getvalue().strip(), "")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 551
