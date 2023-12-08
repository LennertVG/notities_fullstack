#architectuur 
Design patronen voor veel-voorkomende problemen
[Site with info on these four and more design patterns](https://anuraghazra.dev/blog/design-patterns-everyday#Day-15)
![[Pasted image 20231204153140.png]]
- Singleton
	- creational design that a class will only have one instance
	- Vergelijking: ![[Pasted image 20231204151431.png]]
Example singleton
```js
class Singleton {
  static instance = new Singleton();
  static getInstance() {
    return this.instance;
  }

  showMessage() {
    console.log('Hello singleton');
  }
}

let instance1 = Singleton.getInstance();
let instance2 = Singleton.getInstance();
console.log(instance1 === instance2); // true

instance2.showMessage();
```
- Strategy
	- Let's us define different algorithms for doing a particular action and interchange them as we wish
		=> switch between different types of behaviour and implementation
	- vergelijking: ![[Pasted image 20231204151506.png]]
Example Strategy
```ts
// Strategy pattern
interface IStrategy {
  authenticate(...args: any): any;
}

class Authenticator {
  strategy: any;
  constructor() {
    this.strategy = null;
  }

  setStrategy(strategy: any) {
    this.strategy = strategy;
  }

  authenticate(...args: any) {
    if (!this.strategy) {
      console.log('No Authentication strategy provided');
      return;
    }
    return this.strategy.authenticate(...args);
  }
}

class GoogleStrategy implements IStrategy {
  authenticate(googleToken: string) {
    if (googleToken !== '12345') {
      console.log('Invalid Google User');
      return;
    }
    console.log('Authenticated with Google');
  }
}

class LocalStrategy implements IStrategy {
  authenticate(username: string, password: string) {
    if (username !== 'johnwick' && password !== 'gunslotsofguns') {
      console.log('Invalid user. you are `Excommunicado`');
      return;
    }
    console.log('Authenticated as Baba Yaga');
  }
}

const auth = new Authenticator();

auth.setStrategy(new GoogleStrategy());
auth.authenticate('invalidpass');

auth.setStrategy(new GoogleStrategy());
auth.authenticate('12345');

auth.setStrategy(new LocalStrategy());
auth.authenticate('anurag', '12345');

auth.setStrategy(new LocalStrategy());
auth.authenticate('johnwick', 'gunslotsofguns');
```
- Observer
	- behavioural design pattern which is a subscription system which notifies multiple objects about any changes to the object they are observing
	- vergelijking: ![[Pasted image 20231204151531.png]]
Example observer
```ts
import { consoleColor } from '../utils';

interface IPublisher {
  addSubscriber(subscriber: any): void;
  removeSubscriber(subscriber: any): void;
  notifyObservers(): void;
}
interface IObserver {
  notify(payload: any): void;
}

class Publisher implements IPublisher {
  subscribers: IObserver[];
  state: any;
  constructor(state: any = {}) {
    this.subscribers = [];
    this.state = state;
  }

  addSubscriber(subscriber: IObserver) {
    if (this.subscribers.includes(subscriber)) return;
    this.subscribers.push(subscriber);
  }

  removeSubscriber(subscriber: IObserver) {
    if (!this.subscribers.includes(subscriber)) return;
    let index = this.subscribers.indexOf(subscriber);
    this.subscribers.splice(index, 1);
  }

  notifyObservers() {
    this.subscribers.forEach(subs => {
      subs.notify(this.state);
    });
  }

  setState(newState: any) {
    this.state = newState;
    this.notifyObservers();
  }
}

class UserInterface implements IObserver {
  renderTodos(todos) {
    console.clear();
    todos.forEach(todo => {
      consoleColor('cyan', '-----');
      consoleColor(todo.isCompleted ? 'green' : 'red', `${todo.title} ${todo.isCompleted ? '[DONE]' : '[PENDING]'}`);
      consoleColor('cyan', '-----');
    });
  }

  notify(state: any) {
    this.renderTodos(state.todos);
  }
}

const store = new Publisher({
  todos: [
    { title: 'hello', isCompleted: false, id: 1 },
    { title: 'world', isCompleted: false, id: 2 },
  ],
});

const userInterface = new UserInterface();
store.addSubscriber(userInterface);

// add todo
store.setState({
  todos: [...store.state.todos, { title: 'new item', id: Math.random() }],
});

// remove todo
store.setState({
  todos: store.state.todos.filter(t => t.id !== 2),
});
```
- Decorator
	- enhance class/object with extra behaviour without having to define subclasses
	- use cases: ![[Pasted image 20231204151601.png]]
Example Decorator
```ts
// simplified example
function loggerDecorator(wrapped) {
  return function(...args) {
    console.log('******');
    console.log(wrapped.apply(this, args));
    console.log('******');
  };
}
function mapper(arr: any[], add: number) {
  return arr.map(i => i + add);
}

loggerDecorator(mapper)([1, 2, 3], 10);
```

[refactoring Guru, design pattern helper](https://refactoring.guru/design-patterns)

