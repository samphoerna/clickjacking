# clickjacking
script to exploit website iframes function

<img width="200" heigh="200" alt="jack" src="https://github.com/samphoerna/clickjacking/assets/139729508/24fe8f1d-ed05-400d-b4f0-3dab65e60b37">

---

Clickjacking, also known as a UI (User Interface) Redress Attack or a "UI Clickjacking Attack," is a malicious technique where an attacker tricks a user into clicking on a seemingly harmless element on a web page, while actually performing unintended actions or interacting with hidden elements. The attacker achieves this by overlaying or framing the target web page with another transparent or disguised page that contains the attacker's malicious content.

**Exploit:**
The clickjacking exploit takes advantage of the fact that web browsers allow iframes and similar techniques to load and display content from other domains. By placing an invisible or disguised iframe on top of a legitimate web page, the attacker can effectively overlay their own content on top of the original content.

**How it works:**
1. The attacker creates a web page that contains an iframe or an element with a transparent background.
2. The attacker then positions this iframe or element over a specific part of another web page, usually where the user is expected to click or interact.
3. The transparent iframe remains hidden to the user, and the attacker's content remains unseen.
4. The attacker then tricks the user into clicking on an element on the attacker's page, which is actually the same location as a legitimate button or link on the underlying page.
5. As the user interacts with the invisible iframe, the attacker's page captures the clicks and other interactions, causing the user to unintentionally perform actions on the underlying page without their knowledge.

**Preventing Clickjacking:**
To defend against clickjacking attacks, website owners can implement several security measures:

- **X-Frame-Options Header**: Use the `X-Frame-Options` header to restrict which domains are allowed to embed your website using iframes. Setting the `X-Frame-Options` header to `DENY` or `SAMEORIGIN` can help prevent clickjacking attacks.
- **Content Security Policy (CSP)**: Implement a Content Security Policy that specifies the allowed sources for content on your website. A well-configured CSP can prevent unauthorized iframes from loading on your site.
- **Frame-Busting Scripts**: Include frame-busting scripts in your web pages to prevent your site from being loaded within iframes on other websites.
- **Frame-Options in Iframe Tags**: For individual iframes, you can set the `sandbox` attribute or use the `frameborder` attribute with a value of 0 to prevent clickjacking.
