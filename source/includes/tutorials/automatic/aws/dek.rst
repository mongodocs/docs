.. procedure::
   :style: connected

   .. step:: Add your AWS KMS Credentials

      Add the service account credentials to your CSFLE-enabled client
      code.

      .. include:: /includes/tutorials/automatic/aws/iam-credentials-note.rst

      .. tabs-drivers::

         .. tab::
            :tabid: java-sync

            .. literalinclude:: /includes/sample_apps/csfle/build/java/aws/reader/src/main/java/com/mongodb/csfle/makeDataKey.java
               :start-after: start-kmsproviders
               :end-before: end-kmsproviders
               :language: java
               :caption: makeDataKey.java
               :dedent:

         .. tab::
            :tabid: nodejs

            .. literalinclude:: /includes/sample_apps/csfle/build/node/aws/reader/make_data_key.js
               :start-after: start-kmsproviders
               :end-before: end-kmsproviders
               :language: javascript
               :caption: make_data_key.js
               :dedent:

         .. tab::
            :tabid: python

            .. literalinclude:: /includes/sample_apps/csfle/build/python/aws/reader/make_data_key.py
               :start-after: start-kmsproviders
               :end-before: end-kmsproviders
               :language: python
               :caption: make_data_key.py
               :dedent:

         .. tab::
            :tabid: csharp

            .. literalinclude:: /includes/sample_apps/csfle/build/dotnet/aws/reader/CSFLE/MakeDataKey.cs
               :start-after: start-kmsproviders
               :end-before: end-kmsproviders
               :language: csharp
               :caption: MakeDataKey.cs
               :dedent:

         .. tab::
            :tabid: go

            .. literalinclude:: /includes/sample_apps/csfle/build/go/aws/reader/make-data-key.go
               :start-after: start-kmsproviders
               :end-before: end-kmsproviders
               :language: go
               :caption: make-data-key.go
               :dedent:

      .. tip:: Learn More

         To learn more about the KMS provider object for AWS, see
         :ref:`csfle-reference-kms-providers-aws`.

   .. step:: Add Your Key Information

      Update the following code to specify your {+cmk-long+}:

      .. tip::

         You recorded your {+cmk-long+}'s {+aws-arn-abbr+} and Region
         in the :ref:`Create a {+cmk-long+} <aws-create-master-key>`
         step of this guide.

      .. tabs-drivers::

         .. tab::
            :tabid: java-sync

            .. literalinclude:: /includes/sample_apps/csfle/build/java/aws/reader/src/main/java/com/mongodb/csfle/makeDataKey.java
               :start-after: start-datakeyopts
               :end-before: end-datakeyopts
               :language: java
               :caption: makeDataKey.java
               :dedent:

         .. tab::
            :tabid: nodejs

            .. literalinclude:: /includes/sample_apps/csfle/build/node/aws/reader/make_data_key.js
               :start-after: start-datakeyopts
               :end-before: end-datakeyopts
               :language: javascript
               :caption: make_data_key.js
               :dedent:

         .. tab::
            :tabid: python

            .. literalinclude:: /includes/sample_apps/csfle/build/python/aws/reader/make_data_key.py
               :start-after: start-datakeyopts
               :end-before: end-datakeyopts
               :language: python
               :caption: make_data_key.py
               :dedent:

         .. tab::
            :tabid: csharp

            .. literalinclude:: /includes/sample_apps/csfle/build/dotnet/aws/reader/CSFLE/MakeDataKey.cs
               :start-after: start-datakeyopts
               :end-before: end-datakeyopts
               :language: csharp
               :caption: MakeDataKey.cs
               :dedent:

         .. tab::
            :tabid: go

            .. literalinclude:: /includes/sample_apps/csfle/build/go/aws/reader/make-data-key.go
               :start-after: start-datakeyopts
               :end-before: end-datakeyopts
               :language: go
               :caption: make-data-key.go
               :dedent:

   .. step:: Generate your {+dek-long+}

      .. _csfle-aws-create-dek:

      .. tabs-drivers::

         .. tab::
            :tabid: java-sync

            .. literalinclude:: /includes/sample_apps/csfle/build/java/aws/reader/src/main/java/com/mongodb/csfle/makeDataKey.java
               :start-after: start-create-dek
               :end-before: end-create-dek
               :language: java
               :caption: makeDataKey.java
               :dedent:

         .. tab::
            :tabid: nodejs

            .. literalinclude:: /includes/sample_apps/csfle/build/node/aws/reader/make_data_key.js
               :start-after: start-create-dek
               :end-before: end-create-dek
               :language: javascript
               :caption: make_data_key.js
               :dedent:

         .. tab::
            :tabid: python

            .. literalinclude:: /includes/sample_apps/csfle/build/python/aws/reader/make_data_key.py
               :start-after: start-create-dek
               :end-before: end-create-dek
               :language: python
               :caption: make_data_key.py
               :dedent:

         .. tab::
            :tabid: csharp

            .. literalinclude:: /includes/sample_apps/csfle/build/dotnet/aws/reader/CSFLE/MakeDataKey.cs
               :start-after: start-create-dek
               :end-before: end-create-dek
               :language: csharp
               :caption: MakeDataKey.cs
               :dedent:

         .. tab::
            :tabid: go

            .. literalinclude:: /includes/sample_apps/csfle/build/go/aws/reader/make-data-key.go
               :start-after: start-create-dek
               :end-before: end-create-dek
               :language: go
               :caption: make-data-key.go
               :dedent:

.. tip:: Learn More

   To view a diagram showing how your client application creates your
   {+dek-long+} when using an AWS KMS, see
   :ref:`csfle-reference-kms-providers-aws-architecture`.

   To learn more about the options for creating a {+dek-long+}
   encrypted with a {+cmk-long+} hosted in AWS KMS, see
   :ref:`csfle-kms-datakeyopts-aws`.