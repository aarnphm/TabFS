# TabFS

See <https://omar.website/tabfs/>.

The extension connects to the native host when the browser starts or the
extension loads. If the host exits, it reconnects with a delay from one to
30 seconds. A browser alarm checks the connection every minute so recovery
also works after the extension service worker stops.

After changing the native host, rebuild it with `make -C fs`. After changing
the extension, reload TabFS once in the browser's extensions page. The native
messaging manifest must point to the rebuilt `fs/tabfs` executable; see
`install.sh` for browser-specific installation.

(**update**: You can now **[sponsor further development of
TabFS](https://github.com/sponsors/osnr)**!)
