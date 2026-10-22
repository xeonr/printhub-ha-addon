# Print Hub worker

Print Hub runs on the internet, so it can't reach printers on your home network
by itself. This add-on is the worker that does: it connects out to Print Hub
(no ports to open) and passes Print Hub's connections on to printers on your
network, and to nothing else. One worker serves all your printers.

It also puts Print Hub in Home Assistant's sidebar.

## Setting it up

1. Start the add-on, then open **Print Hub** in the sidebar (or **Open web UI**
   on this page). The first time, it shows a pairing code.
2. Click **Pair in Print Hub** and sign in (or, in Print Hub, go to
   **Settings → Workers → Add worker** and enter the code). The code works for
   10 minutes; a new one follows when it runs out.
3. The page then says **Connected**. When you add a printer in Print Hub, pick
   this worker.

Printers that use Prusa Connect (Prusa MINI, MK4, XL, CORE One…) connect to
Print Hub themselves and don't need a worker.

## Print Hub in the sidebar

Once the worker is paired, **Print Hub** in the sidebar is Print Hub itself.
The first time, it shows a sign-in code: click **Open Print Hub to approve**,
check the code matches, and click **Sign it in**. The sidebar stays signed in
as you until you sign out there (it's signed in separately from Print Hub in
your browser).

Print Hub's pages pass through the worker, so they work in the Home Assistant
apps too. Turn **Print Hub in the sidebar** off to show only the worker's
settings there.

## The worker's settings

In the sidebar, your avatar menu → **Worker settings** (or **Open web UI**
before it's paired) shows whether it's connected, the account it belongs to,
and the printers it serves.

**Unlink from Print Hub** removes it from Print Hub and shows a new code, to
pair it again in the same account or another. Its printers stop working until
you pick a worker for them again.

## Options

- **Print Hub address** (`hub`): leave it as it is.
- **Name** (`name`): what the worker is called in Print Hub.
- **Print Hub in the sidebar** (`sidebar`): on by default.
- **More addresses** (`allow`): addresses or networks it may reach besides
  private (home network) ones, comma-separated. Usually empty; `127.0.0.1`
  for a service on Home Assistant itself.
