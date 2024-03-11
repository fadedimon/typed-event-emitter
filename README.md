# typed-event-emitter
Empower a type-safety of events with a typed event-emitter

---

Provides an amazing experience of event handling by utilising incredible benefits of types.
It requires event-to-callback-argument map as first generic attribute and makes sure that
all methods are used correctly.

## Usage

**1. Define event-name to callback-argument type map**

Event name is a string, and callback argument can be any type. Use `void` if event doesn't require an argument.

```tsx
type EventsMap = {
  ping: { message: string };
}
```

**2. Instantiate** `TypedEventEmitter`

```tsx
const emitter = new TypedEventEmitter<EventsMap>();
```

**3. Subscribe to events**

```tsx
emitter.on('ping', (arg) => {
  console.log(`ping: "${arg.message}"`);
});
```

**4. Start emitting events**

```tsx
emitter.emit('ping', { message: 'hello!' });
```

## API

## TODO:

[-] Add tests \
[-] Add documentation \
[-] Publish npm package \
