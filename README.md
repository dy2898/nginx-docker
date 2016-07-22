# nginx+OpenSSL+ChaCha20/Poly1305+Certificate Transparency

This docker image contains the latest nginx (mainline). It is compiled with OpenSSL 1.0.2 having the 
ChaCha20/Poly1305 patch from [Cloudflare](https://github.com/cloudflare/sslconfig). It also includes
the [nginx Certificate Transparency module](https://github.com/grahamedgecombe/nginx-ct)

## Configuration

As the Dockerfile is a modification of the official nginx docker image, see its documentation. Also, see the
docs for the [Certificate Transparency module](https://github.com/grahamedgecombe/nginx-ct).

`ChaCha20/Poly1305` can be enabled by adding `EECDH+CHACHA20:EECDH+CHACHA20-draft` to the list of ciphers.
