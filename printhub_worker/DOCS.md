# Print Hub worker

Print Hub runs on the internet, so it can't reach printers on your home network
by itself. This add-on is the worker that does: it connects out to Print Hub
(no ports to open) and passes Print Hub's connections on to printers on your
network, and to nothing else. One worker serves all your printers.

## Setting it up

1. Start the add-on, then open **Print Hub** in the sidebar (or **Open web UI**
   on this page). It shows a pairing code.
2. Click **Pair in Print Hub** and sign in (or, in Print Hub, go to
   **Settings → Workers → Add worker** and enter the code). The code works for
   10 minutes; a new one follows when it runs out.
3. The page then says **Connected**. When you add a printer in Print Hub, pick
   this worker.

Printers that use Prusa Connect (Prusa MINI, MK4, XL, CORE One…) connect to
Print Hub themselves and don't need a worker.

## Options

- **Print Hub address** (`hub`): leave it as it is.
- **Name** (`name`): what the worker is called in Print Hub.
- **More addresses** (`allow`): addresses or networks it may reach besides
  private (home network) ones, comma-separated. Usually empty; `127.0.0.1`
  for a service on Home Assistant itself.

## Moving it to another account

Click **Pair again** on its page and enter the new code in the other account.
Remove the old entry from the first account's **Settings → Workers**.
