# reimagined-design-patterns

Give a summary description of Four design patterns that you choose from the following design patterns: **Adapter,  Builder, Composite, Decorator, Observer, Interpreter, State, Mediator, Memento, Prototype, Proxy**. In your summaries say:

- what kind of problem(s) you can solve with that pattern and when you use it, maybe with a short example
- how the pattern works, what the basic idea of the pattern is
- what the main advantage and what the the main disadvantage is of using this pattern
- Write a short summary for each of the four patterns, about half a page for each pattern (rather less than more). 

> Do not add diagrams, and do not try to give a complete description of the patterns as found in the books. Rather think of how you would explain the essential ideas of these patterns in a few sentences to a colleague while drinking coffee.

**Proxy:**

Summary:
This design pattern will act as a substitute for another object. The proxy object acts as an intermediate object that controls the access to original object. The proxy will perform some actions before or after the request goes to the actual object.object.

Example:
When data needs to be send between 2 ECUs, there is a particular protocol that needs to be followed(like message CRC, message cunter for the data stream that needs to be send). Different ECUs send the data stream to proxy, proxy will make the data stream alligned to protocol and then send to the target.

Advantages:
Reusabliity of the functions.
New proxies can be introduced without changing the objects at both ends.

Disadvantages:
Performance Issues.

**State:**

Summary:
This design pattrn is used when the object have different behaviours in each of the internal states of the object where the state can switch in between.
This design pattern helps to design in a particular manner where the adding/deletion of states can be acheived without much changes.

Example:
Instrument cluster backlight that needs to be controlled according to the state of ignition key status. The SW component can have different states like Init, Inactive state where the I/P is not available, Normal operation where Backlight needs to be turned ON/OFF based on different conditions.

Advantges:
Easy to add/delete states ie OCP.
Each state have a pure function.

Disadvantages:
Code complexity in case of simple state machines where it can be acheived in a simple switch statement.

**Observer:**

Summary:
This design pattern is used when ever n-objects are dependent on the state change of another object. All the dependent components are notified automatically.

Example:
In case of many SW components needs to read a particular HW register when its value is updated by a different compoennt. Instead of every component, reading the HW register cyclically, we can configure an interrupt/callback to all the dependent SW components whenever the value is updated in the HW register.

Advantages:
Can add new subscribers with less effort.
Performance- no need to read it cyclically, read is done only on need basis.

Disdvantaes:
Prority handling for the subscribers to get notified.


**Adapter:**

Summary:
This design pattern hepls to interconnect 2 incompatable interfaces. It basically converts the interface from one type to another that suits the server.

Example:
When cluster needs to send some data to Head unit, wrapper classes will be used, so that the data from cluster is converted to different type and provided to head unit.

Advantages:
Even in case of change in adapter, no changes required in client side ie OCP.
Reusabliity of code

Disadvantages:
Code complexity and error prone due to multiple conversions.
