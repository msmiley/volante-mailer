# Volante Mailer Spoke

volante module for nodemailer

Provides simple setup of nodemailer through volante framework.
All events follow the Volante hub/spoke model and are emitted on the hub.

## Usage

```bash
npm install volante-mailer
```

Volante modules are automatically loaded and instanced if they are installed locally and `hub.attachAll()` is called.

## Props

Options are changed using the `VolanteMongo.update` event with an options object:

```js
hub.emit('VolanteMailer.update', {
  transport: {
    host: "smtpserver",
    port: 587,
    auth: {
      user: "",
      pass: "",
    },
  },
});
```

> The module will automatically start a connection when the props are changed.

## Events

### Handled

- `VolanteMailer.send` - send an email message, needs { from, to, subject, text || html } fields, takes a callback parameter passed directly to nodemailer


## License

ISC