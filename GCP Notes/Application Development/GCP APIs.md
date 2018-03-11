# GCP APIs

1. **Google Cloud Client libraries** the current and and recommended way to make requests

    See [https://storage.googleapis.com/cloud-training/gcpdev/1.2/Student/(online)%2002_Client%20Libraries%20and%20SDKs.pdf](https://storage.googleapis.com/cloud-training/gcpdev/1.2/Student/(online)%2002_Client%20Libraries%20and%20SDKs.pdf)

    Google Cloud client libraries handle low level communication with the server, including authentication with Google, and they can be installed using familiar installation packages such as NPM and Pip. The Client Libraries also provide retry logic for transit network failures. May use gRPC. 

    You can pull the repo for the Cloud Client Libraries for each of the supported
    programming languages. The GitHub Repo page lists the services/APIs supported by
    each language’s Cloud Client library and provides installation instructions. You can
    also download Cloud Client Libraries for individual Cloud Platform services.

    Reference libraries contain links to documentation and relevant StackOverflow posts
    and provide code examples. The reference libraries provide information on a language-specific Cloud Client Library.

    For direct links to GitHub Repos and Reference Libraries, see
    [https://cloud.google.com/apis/docs/cloud-client-libraries](https://cloud.google.com/apis/docs/cloud-client-libraries).

    If your application is running on App Engine or Compute Engine, authentication for your application will “just work.” If you don’t explicitly provide credentials, the Client will reuse the
    credentials from the gcloud tool, assuming it has already been installed and
    authorized. See also [https://cloud.google.com/docs/authentication](https://cloud.google.com/docs/authentication/)

2. **Google API Client** — Only if Cloud Client Lib are not available in your language of choice (RESTful only)
3. Cloud SDK — cli tools. See docs  

    [Google Cloud SDK documentation](https://cloud.google.com/sdk/docs/)

    1. gcloud. create and manage GCP resources
    2. bq.  primary purpose is running queries and it can also be used to manage data sets, tables and other big query entities
    3. gsutil  perform tasks in Google Cloud Storage
4. Firebase SDK - use for user federated authentication in applications. Firebase is a dev platform for mobile and web applications. Firebase SDK also include support for Cloud Storage, App Engine (std), Cloud Functions, and Cloud Vision/Speech