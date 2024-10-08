# URL parts

https://developer.mozilla.org/en-US/docs/Web/API/URL/hostname

![image](https://github.com/user-attachments/assets/7ce6dffd-d37d-4de7-90c0-057d7f69e418)

![image](https://github.com/user-attachments/assets/05757a98-f246-4635-a300-d3a81a192f2c)

### 1. **Scheme (or Protocol)**:

#### Scheme
  - `http`
  - `https`
  - `mailto`

- The first part of the URL is the **scheme**, which indicates the protocol that the browser must use to request the resource (a protocol is a set method for exchanging or transferring data around a computer network).
**The scheme doesn't include `://`**

https://developer.mozilla.org/en-US/docs/Learn/Common_questions/Web_mechanics/What_is_a_URL

#### Protocol

The **protocol** defines the method by which the resource is accessed, usually specifying a network protocol. Common examples are:
   - `http://` – Hypertext Transfer Protocol (unsecure)
   - `https://` – Hypertext Transfer Protocol Secure (encrypted communication)
   - `ftp://` – File Transfer Protocol

**The protocol includes `://`**

---

### 2. **Hostname** (or Domain):
   The **hostname** indicates the specific domain name (or IP address) of the server that hosts the resource. The hostname can include subdomains and the main domain name:
   - **Domain**: This is the central part of the hostname, such as `example.com`.
   - **Subdomain** (optional): A part of the domain that can represent a specific section of the site, such as `www` or `blog`. 
   
---

### 3. **Port** (optional):
   The **port** is the number associated with a specific service or protocol on the server. If omitted, the default port for the protocol is assumed (e.g., 80 for `http` and 443 for `https`).
   - **Example:** `8080`, `3000`, etc.

---

### 4. **Path**:
   The **path** specifies the location of a specific resource on the server, often corresponding to the directory or file structure.
   - The path typically follows the hostname and is separated by `/` characters to indicate directories or pages.

---

### 5. **Query String** (optional):
   The **query string** is a set of key-value pairs, typically used to send data to the server (e.g., search terms, filters, parameters). It starts with a `?` and separates key-value pairs with `&`.

---

### 6. **Fragment** (optional):
   The **fragment** refers to a specific section within the web page, such as an anchor point or an element with a given ID. It starts with a `#` symbol.

---

### Full Example URL Breakdown:

Given the URL:  
`https://blog.example.com:8080/articles/page.html?q=search#top`

0. **Scheme**: `https`
1. **Protocol**: `https://`
2. **Hostname**: `blog.example.com`
   - Root domain: `.` (implicit)
   - TLD: `com`
   - Second level domain: `example`
   - **Subdomain** or Third level domain: `blog`
   - **Domain**: `example.com`
   - Fully-qualified domain name or Full domain or **Hostname**: `blog.example.com`
4. **Port**: `8080`
5. **Path**: `/articles/page.html`
6. **Query string**: `q=search`
7. **Fragment**: `#top`

### URL Structure Summary:
```
scheme://hostname[:port]/path?query#fragment
```

# Origin

`scheme + hostname + port`

https://developer.mozilla.org/en-US/docs/Glossary/Origin
