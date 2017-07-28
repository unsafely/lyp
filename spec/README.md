Lightweight Yabber Protocol
=========

Lightweight Yabber Protocol, a.k.a LYP, is a simplified messaging protocol
which refers many modern instant messaging system and architecture. It is
also one of the protocols powering [unsafechat](https://github.com/unsafely/chat).

## General explanation

This specification is only about the schema of LYP, you can simply apply these
schema to any of the general formats like JSON, ProtoBuf, msgpack etc., also you
can use any of the transmission protocol like TCP, HTTP or via WebSocket.

Typically, LYP uses single endpoint to process all of the messages and produce
the respose, but as its schema is very tight and unified, you can easily translate
it to more advanced protocol like HTTP, e.g. using HTTP header to store common fields
of a LYP message, using HTTP body to store the body, and using HTTP path for
LYP actions.

LYP uses unified message model to stands for every messages, this model composed by
a common header, you can see `spec/message.spec.json`.

The format uses [JSONSpec](http://spec.kimleo.net).
