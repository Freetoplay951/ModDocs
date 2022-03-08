.. _moderation:

==========
Moderation
==========

.. _moderation_befehle:

Befehle
=======

Folgende Befehle sind  für Moderatoren.
Um diese auszuführen, benötigen Mitglieder entweder die Moderator\*innen-Rolle oder
müssen über ein entsprechendes Recht bei Discord verfügen.

.. _moderation_ban:

ban
^^^

Syntax: ``w#ban [@Mitglied] [Grund]``

Bannt ein Mitglied dauerhaft vom Server.
Sofern Weemo dem Mitglied eine DM schicken kann, wird der Grund für den Ban an das Mitglied gesendet.
Das Mitglied kann nach einem Ban dem Server nicht wieder beitreten.
Dies löscht alle neueren Nachrichten des Mitglieds.

.. _moderation_idban:

idban
^^^^^

Syntax: ``w#idban [ID] [Grund]``

Bannt eine Nutzerin / einen Nutzer dauerhaft vom Server.
Die Person kann nach einem Ban dem Server nicht beitreten.
Der Befehl kann auch auf Personen angewandt werden, die den Server bereits verlassen oder noch nie betreten haben.
Dies löscht alle neueren Nachrichten der Person.
Dazu wird die :ref:`ID<id>` der Person benötigt.

.. _moderation_tempban:

tempban
^^^^^^^

Syntax: ``w#tempban [@Mitglied] [Dauer] [Grund]``

Bannt eine Nutzerin / einen Nutzer für die angegebene Zeit vom Server.
Nach Ablauf der Zeit, wird das Mitglied entbannt.
Dies löscht alle neueren Nachrichten des Mitglieds.

.. _moderation_unban:

unban
^^^^^

Syntax: ``w#unban [ID]``

Entbannt eine gebannte Person.
Dazu wird die :ref:`ID<id>` der Person benötigt.

.. _moderation_mute:

mute
^^^^

Syntax: ``w#mute [@Mitglied] [Dauer] <Grund>``

Gibt einem Mitglied für die angegebene Dauer die Mute-Rolle und
verweigert dem Mitglied auf diese Weise das schreiben und sprechen.


.. _moderation_unmute:

unmute
^^^^^^

Syntax: ``w#unmute [@Mitglied]``

Entfernt die Mute-Rolle vom Mitglied.

.. _moderation_kick:

kick
^^^^

Syntax: ``w#kick [@Mitglied] [Grund]``

Alias: ``raus``

Entfernt ein Mitglied vom Server.
Sofern Weemo dem Mitglied eine DM schicken kann, wird der Grund für den Kick an das Mitglied gesendet.
Das Mitglied kann nach einem Kick den Server wieder beitreten.
Dies löscht keine Nachrichten des Mitglieds.

.. _moderation_warn:

warn
^^^^

Syntax: ``w#warn [@Mitglied] [Grund]``

Verwarnt ein Mitglied.
Sofern Weemo dem Mitglied eine DM schicken kann, wird der Grund für die Verwarnung an das Mitglied gesendet.
Verwarnungen werden gespeichert und können mit punishments_ von Moderator\*innen abgerufen werden.

.. _moderation_purge:

purge
^^^^^

Syntax: ``w#purge [Anzahl]``

Alias: ``cc``

Löscht die letzten Nachrichten in einem Kanal.
Die ``Anzahl`` der zu löschenden Nachrichten muss zwischen 1 und 150 liegen.

Nachrichten, die zu alt sind, können nicht von Weemo gelöscht werden.

.. _moderation_punishments:

punishments
^^^^^^^^^^^

Syntax: ``w#punishments <Mitglied>``

Zeigt die Verwarnungen eines Mitglieds an.


Syntax: ``w#punishments id <ID>``

Zeigt die Verwarnung mit der angegebenen ID an.


.. _modlog:

Modlog
======

Das Modlog speichert Ereignisse ab, die auf dem Server passieren.
Es speichert gelöschte und geänderte Nachrichten, was der Automod gelöscht hat, wer verwarnt wurde und warum,
wann welche Einstellungen geändert wurden und vieles mehr.
Dies ist für Moderator\*innen nützlich, um gelöschte Beleidigungen oder veränderte Gespräche nachzuvollziehen.

Der Modlog sollte ein eigener Textkanal sein, kann aber mit dem Log anderer Bots kombiniert werden.
Wir empfehlen, den Modlog zu einem privatem Kanal zu machen, auf den nur Moderator\*innen zugriff haben.

Einstellungen
^^^^^^^^^^^^^

Mit ``w#modlog setchannel [logchannel]`` kann ein Textkanal als Modlog-Kanal eingestellt werden.

Eine Übersicht, welche Module aktiv sind, kann mit ``w#modlog`` abgefragt werden.
Durch die Eingabe von ``w#modlog``, gefolgt von der Nummer den Moduls durch das Klicken eines Knopfes,
kann eine Modul aktiviert/deaktiviert werden.

Es existieren folgende Module:

+--------+-----------------------------+------------------------------------------+
| Nummer | Log für                     | Beinhaltet                               |
+========+=============================+==========================================+
|      1 | Gilden                      | - Serverregion aktualisiert              |
|        |                             | - Serverinhaber\*in gewechselt           |
|        |                             | - Servername geändert                    |
|        |                             | - Servericon geändert                    |
|        |                             | - Verifizierungsstufe verändert          |
|        |                             | - Mitglied gebannt                       |
|        |                             | - Mitglied entbannt                      |
|        |                             | - moderativer Befehl ausgeführt          |
+--------+-----------------------------+------------------------------------------+
|      2 | Sprachkanal                 | - Sprachkanal betreten                   |
|        |                             | - Sprachkanal verlassen                  |
|        |                             | - Sprachkanal gewechselt                 |
+--------+-----------------------------+------------------------------------------+
|      3 | Kanal                       | - Textkanal erstellt                     |
|        |                             | - Textkanal gelöscht                     |
|        |                             | - Sprachkanal erstellt                   |
|        |                             | - Sprachkanal gelöscht                   |
+--------+-----------------------------+------------------------------------------+
|      4 | Bearbeitete Nachrichten     | - Mitglied hat eine Nachricht bearbeitet |
+--------+-----------------------------+------------------------------------------+
|      5 | Server betreten & verlassen | - Mitglied hat den Server betreten       |
|        |                             | - Mitglied hat den Server verlassen      |
+--------+-----------------------------+------------------------------------------+
|      6 | Rollen                      | - Rolle erhalten                         |
|        |                             | - Rolle entfernt                         |
|        |                             | - Rolle erstellt                         |
|        |                             | - Rolle gelöscht                         |
+--------+-----------------------------+------------------------------------------+
|      7 | Nachrichten gelöscht        | - Mitglied hat Nachricht gelöscht        |
+--------+-----------------------------+------------------------------------------+
|      8 | Mitglieder                  | - Nickname geändert                      |
+--------+-----------------------------+------------------------------------------+
|      9 | Einladungen                 | - Einladung erstellt / gelöscht          |
+--------+-----------------------------+------------------------------------------+

.. _automod:

Automod
=======

Eine Übersicht, welche Module aktiv sind, kann mit ``w#automod`` abgefragt werden.
Durch die Eingabe von ``w#automod``, gefolgt von der Nummer den Moduls durch das Klicken eines Knopfes,
kann ein Modul aktiviert/deaktiviert werden.

Es existieren folgende Module:

+--------+-----------------------------+--------------------------------------------------------------------------------------+
| Nummer | Log für                     | Funktion                                                                             |
+========+=============================+======================================================================================+
|      1 | Aktivieren / Deaktivieren   | - De-/aktiviert den AutoMod                                                          |
+--------+-----------------------------+--------------------------------------------------------------------------------------+
|      2 | Einladungsfilter            | - De-/aktiviert den Einladungsfilter                                                 |
+--------+-----------------------------+--------------------------------------------------------------------------------------+
|      3 | Wortfilter                  | - De-/aktiviert den Wortfilter                                                       |
+--------+-----------------------------+--------------------------------------------------------------------------------------+
|      4 | Capslockfilter              | - De-/aktiviert den Capslockfilter                                                   |
+--------+-----------------------------+--------------------------------------------------------------------------------------+
|      5 | Scamfilter                  | - De-/aktiviert den Scamfilter                                                       |
+--------+-----------------------------+--------------------------------------------------------------------------------------+
|      6 | Wortliste                   | - Listet alle Wörter auf, die zum AutoMod hinzugefügt wurden.                        |
+--------+-----------------------------+--------------------------------------------------------------------------------------+

.. csv-table::
    :widths: auto
    :align: left
    :header: "Befehl", "Beschreibung"

    "automod ignore [@Rolle]", "Fügt eine Rolle hinzu, die nicht vom AutoMod beachtet werden soll. Entfernt diese, sofern sie hinzugefügt wurde."
    "automod filter [Wort]", "Fügt ein Wort zum Wortfilter hinzu. Entfernt das Wort, sofern es hinzugefügt wurde."
    "automod maxcaps [Max. Caps]", "Konfiguriert die Prozentanzahl, die eine Nachricht maximal an Caps beinhalten darf."
    "automod message [Nachricht]", "Konfiguriert die Nachricht, die gesendet werden soll, wenn ein Mitglied vom AutoMod verwarnt wird."

Wortfilter
^^^^^^^^^^

Der Wortfilter schlägt an, falls eines der Wörter in einer Nachricht vorkommt. 
Mit ``w#automod filter [Wort]`` können Wörter hinzugefügt und entfernt werden.

Einladungsfilter
^^^^^^^^^^^^^^^^

Der Einladungsfilter erfasst Discord-Einladungslinks.

Capslockfilter
^^^^^^^^^^^^^^

Der Capslockfilter löscht Nachrichten, deren Inhalt zu einem großteil aus Großbuchstaben besteht.
``w#automod maxcaps [Prozentwert (Standardmäßig 50%)]`` aktiviert oder deaktiviert den Capslockfilter.

Scamfilter
^^^^^^^^^^^^^^

Der Scamfilter löscht Links zu Phishing-Seiten. Klicke **niemals** auf diese Links, dein Discord-Account kann dadurch gestohlen werden!
Was Phishing-Seiten sind: https://de.wikipedia.org/wiki/Phishing.

Nachricht
^^^^^^^^^

Falls der Automod durchgreift, sendet Weemo eine Nachricht in den entsprechenden Chat. Diese Nachricht kann mit
``w#automod message [Nachricht]`` eingestellt werden.
Durch das Einfügen von Platzhaltern in die Nachricht, wird diese beim senden auf die Nutzer personalisiert.

.. csv-table::
    :widths: auto
    :align: left
    :header: "Platzhalter", "Beschreibung"

    "``%user%``", "Name des Nutzers / der Nutzerin"
    "``%mention%``", "Erwähnung des Nutzers / der Nutzerin"
