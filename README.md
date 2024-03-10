# turso-local

Management tool for libsql databases, spin up local databases for development and testing as easily as using the `turso` cli.

## Usage

To install dependencies:

```bash
bun install
```

To start the server you can run the following command:

```bash
bun turso-local start
```

You can stop the server along with all the databases at any time by running `bun turso-local stop`.

You will need to create the database by running the following command:

```bash
bun turso-local create <database-name>
```

This will start a new libsql database server and store it in the file `~/.turso-local/<database-name>/<database-name>.db`, which will be created if it doesn't exist.

This will also output the database url, which you will use to connect. _The authentication tokens are not required for local databases, so you can omit them when connecting._

If you want to get the database url again you can run the following command:

```bash
bun turso-local show <database-name>
```

Or list all the databases by running:

```bash
bun turso-local list
```

If you'd like to open a database shell you can run the following command:

```bash
bun turso-local shell <database-name>
```

For more information on the commands you can run `bun turso-local help`.
