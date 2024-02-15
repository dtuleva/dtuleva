### 👋 Hello there!

```python
class HumanModel(tf.keras.Model):

  def __init__(self, about_me):
    super().__init__()

    self.name_embedding = tf.keras.layers.StringLookup()
    self.location_embedding = tf.keras.layers.StringLookup()

  def call(self, inputs):
    return tf.concat([
        self.name_embedding(inputs["name"]),
        self.location_embedding(inputs["location"]),
    ], axis=1)


me = HumanModel()
me({"name": tf.constant("Diana"), "location": tf.constant("Bulgaria")})
```

Thanks for looking at what I've written! 👀

If you really need to write back: 
📫 dtuleva@students.softuni.bg



