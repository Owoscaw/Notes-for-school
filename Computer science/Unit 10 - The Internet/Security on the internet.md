If information is transmitted over the internet in plain, unencrypted text, then anyone can tap in on the transmission and see the contents of the information. Someone could intercept the transmission, intercept the contents and change them before resending it.

## Firewalls:

A firewall can be used to control the data flow inbound and outbound from a network. A firewall can take the form of software or hardware, sometimes both. This firewall monitors data and controls the opening of ports so that only certain data traffic is allowed through.

Packets of data are inspected by the firewall to check which port they are attempting to access. Diffferent network protocols use different ports, for example HTTP traffic uses ports 80 or 8080. If this traffic is allowed through, the port is opened for the duration of the connection, otherwise it is rejected entry.

Stateful inspection examines the payload of a packet before allowing access, and then remembers actions for future decisions (will allow packets from previously allowed sources).

## Proxy servers:

Proxy servers make up a web request on behalf of your own computer, hiding the true request IP address from the recipient. This enables anonymous web surfing, as there is no identifying information sent out for a given client's web request, as the IP being used if that of the proxy server, not the client. A proxy server can also be used in a network to whitelist or blacklist certain websites. It also provices a cache of previously visited sites that can speed up access for frequently accessed websites.

## Encryption:

Encyrption is the act of encoding a plaintext message so that it cannot be deciphered unless you have a numerical key to decrypt it. Symmetric encryption uses the same key to encrypt and decrypt a message. This key has to be sent along with the message, so it is not very secure. A man in the middle attack can intercept the key when it is transmitted as well as the encrypted text, as the same key works to decrypt as was used to encrypt.

Asymmetric encryption uses two keys, a public and private key. The recipient's public key is used to encrypt a message, which is then transmitted. This message can only be decypted using the recipient's private key, only known to the recipient. The recipient's public key as well as the message can be intercepted, however the public key cannot be used to decrypt the message.

Symettric encryption is generally faster than asymettric encryption, as the same key is used for both encryption and decryption. Small area networks often use a pre-shared key for encryption.

Asymmettric encryption is used to initiate TLS connections. This is slower than symettric encryption. Hybrid encryption is often used, where the beggining of the session uses asymettric encryption to share a private key that will be used for symettric encryption. This keeps communication secure and fast.

## Digital signatures/certificates:

Digital signatures are used to verify the integrity of a message. The sender adds a digital signatured to a message before it is sent. This signature is created by irreversibly reducing the unencrypted message to produce a hash. This hash is encrypted using the senders private key. The signature and message are then bundled together and encrypted using the recipient's public key.

The recipient of this message uses their private key to decrypt the message bundle. The sender's public key then decrypts the digital signatures. This hash is compared to the hash that is generated from the message that was recieved. If the hashes match, the integrity of the message is verified. 

A digital certificate is sent along with a digital signature in a message. A trusted company known as a Certificate Authority (CA) authorises digital certificates. These can include a serial number, the CA's name, expiry data, name of holder, subject's public key, ect. These are used to verify the identity of the owner of each public key and are used to obtain the key itself.
