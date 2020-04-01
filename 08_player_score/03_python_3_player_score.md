Let's start coding, Find the `catch-me-if-you-can/catch_me_if_you_can.py` file, and add the following:

```python
class Score:
    def __init__(self, level_selection, name):
        self.level_selection = level_selection
        self.word = len(random_word) 
        self.bonus = 5
        self.name = name

    def get_score(self):
        if self.level_selection == 1:
            return (self.level_selection) * (10 + self.word + self.bonus)
        elif self.level_selection == 2:
            return (self.level_selection) * (20 + self.word + self.bonus)
        else:
            return (self.level_selection) * (30 + self.word + self.bonus)

    def __str__(self):
        return "\n+---------------+\nName: %s \nLevel: %s \nScore: %s \n+---------------+" % (self.name, self.level_selection, self.get_score())

```

### Let me explain this code step by step:
