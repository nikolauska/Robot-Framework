.. code:: robotframework

    *** Settings ***
    Documentation     A resource file with reusable keywords and variables.
    ...               This test is functionally identical to the example in
    ...               valid_login.txt file               
    Suite Setup  Open website
    Suite Teardown  Close Browser
    #Test Setup  Go To Main Page
    Resource  resource.txt

=======================================================================
  Contriboard Reference Product - Jaska's login morning
=======================================================================

Primary Actor: Jaska, Jonne

Other Actors:

Roles: Common Users

============
Introduction
============

Jaska on opiskelija JAMK:ssa ja hänen pitäisi etsiä tietoa kielikokeista

Etsiminen
------------------------
Jaska etsii kielikokeen jamkin sivuilta.

.. code:: robotframework

    *** Test Cases ***
    Open search
        Open website
        Input search text
        Click search

Valinta
------------------------
Jaska valitsee ensimmäisen linkin.

.. code:: robotframework

    *** Test Cases ***
    Select link
        Click first link

Pelikurssi
------------------------
Jaska huomasi mielenkiintoisen kurssin sivun reunasta. Linkin tekstissä luki pelikurssi ja ketä opiskelijaa sellainen ei muka kiinnostaisi.

.. code:: robotframework

    *** Test Cases ***
    Open pelikurssi
        Click pelikurssi

Lopppu
------------------------
Jaska mielestä pelikurssi näytti kiinnostavalta, mutta hän ei siihen pystynyt tällä hetkellä osallistumaan joten hän sulki selaimen ja päätti lähteä pois koneelta syömään.

.. code:: robotframework

    *** Test Cases ***
    Close
        Close page