# Copyright 2014 Pants project contributors (see CONTRIBUTORS.md).
# Licensed under the Apache License, Version 2.0 (see LICENSE).

java_protobuf_library(name='unpacked_jars',
  sources=from_target(':external-source'),
)

unpacked_jars(name='external-source',
  libraries=[':external-source-jars'],
  include_patterns=[
    'com/squareup/testing/**/*.proto',
  ],
)

jar_library(name='external-source-jars',
  jars=[
    jar(org='com.squareup.testing.protolib', name='protolib-external-test', rev='0.0.2'),
  ],
)
