# wordpress-pricing-component

```
<iframe src="https://filterpixel.github.io/wordpress-pricing-component/" id="custom-pricing-css-0109"></iframe>
```

1. Using external CSS: insert the pricing-custom-media.css
2. Using script: Inject this script(uses event-listener)
    ```
    <script>
    let iframe = document.getElementById('custom-pricing-css-0109');
    function resizeIframe() {
       console.log(window.innerWidth);
        if (window.innerWidth <= 800) {
            iframe.style.width = '100%';
            iframe.style.height = '700px';
        } else {
            iframe.style.width = '800px';
            iframe.style.height = '400px';
        }
    }
    window.addEventListener('resize', resizeIframe);
    resizeIframe();
    </script>

    ```
3. Using only Script component:
    ```
    <div id="iframe-container"></div>

    <script>
        var iframe = document.createElement('iframe');
        iframe.src = 'http://127.0.0.1:5500/index.html';
        iframe.id = 'custom-pricing-iframe';
        iframe.style.width = '800px';
        iframe.style.height = '400px';
        iframe.style.border = 'none';
        iframe.style.overflow = 'hidden';

        var container = document.getElementById('iframe-container');
        container.appendChild(iframe);

        function resizeIframe() {
            if (container.offsetWidth <= 800) {
                iframe.style.width = '100%';
                iframe.style.height = '700px';
            } else {
                iframe.style.width = '800px';
                iframe.style.height = '400px';
            }
        }

        window.addEventListener('resize', resizeIframe);

        resizeIframe();
    </script>

    ```