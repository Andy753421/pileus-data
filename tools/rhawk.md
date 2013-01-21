rhawk is a IRC bot written in GNU Awk.

Source Code
-----------
Source code is available in git and [gitweb](/git/?p=~andy/rhawk)

    git clone git://pileus.org/~andy/rhawk

Components
----------
<dl>
  <dt>rhawk</dt>
  <dd>rhawk is the main awk script that starts up the IRC bot. It requires a
      network connection as standard input and output. The suggested way to do
      this is by using socat as shown in rhawk.sh</dd>

  <dt>irc.awk</dt>
  <dd><p>IRC protocol handling is done in the irc awk script. In addition to
         the pure protocol things, irc.awk also provides some framework code to
         handle starting, stopping, and reloading the client.</p>

      <p>When included, the irc script will spawn a child instance of rhawk.
         This is done so that the client can be reloaded without dropping the
         existing IRC connection.</p></dd>

  <dt>json.awk</dt>
  <dd>A simple json parser is included, it has no external dependencies, so it
      can be used by other awk scripts as well.</dd>

  <dt>email.awk</dt>
  <dd>The email component provides notifications to IRC users if someone says
      their name while they are away.</dd>

  <dt>spades.awk</dt>
  <dd>Spades is a great card game. As such, rhawk lets you play spades by
      joining the #rhspades channel on freenode.net and issuing the .newgame
      command. Note, you'll have to get three other players as well.
      The '.help spades' command provides a list of spades commands.</dd>
</dl>

rhsed
-----
Awk is a great language for writing an IRC bot.

Sed, on the other hand, is not so a great at it.

* [gitweb](/git/?p=~andy/rhawk;f=rhsed;a=blob)
