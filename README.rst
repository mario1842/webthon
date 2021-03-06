webthon
=======

.. image:: https://discord.com/api/guilds/570368779150688266/embed.png
   :target: https://discord.com/invite/uynSzaTAF3
   :alt: Discord server invite
.. image:: https://img.shields.io/pypi/v/webthon.svg
   :target: https://pypi.org/project/webthon/
   :alt: PyPI version info


This is simple html generator for flask or django


Installing
~~~~~~~~~~

**Python 3.8 or higher is required**


.. code:: sh

    # Linux/macOS
    pip3 install -U webthon

    # Windows
    pip install -U webthon


Flask Code Example
~~~~~~~~~~~~~~~~~~~

.. code:: py

    from flask import Flask
    import index
    app = Flask(__name__)
    
    @app.route("/")
    def home():
        return index.create()


    if __name__ == "__main__":
        app.run(debug=True)

index.py Example
~~~~~~~~~~~~~~~~

.. code:: py

    from webthon import website

    index = website()

    index.set_title("webthon example")
    index.set_description("webthon site example")
    index.set_keywords(["webthon","web"])
    index.set_author("mario1842")


    index.heading("Welcome!",1,"id","welcome")
    index.paragraph("This is simple example","class","example")

    def create():
        return index.generate()

Generated Site
~~~~~~~~~~~~~~
.. image:: https://github.com/mario1842/webthon/blob/main/site.png
   :target: https://github.com/mario1842/webthon/blob/main/site.png
   :alt: Created site from example code.

Links
-----
- `Github <https://github.com/mario1842/webthon/>`_
- `Youtube Channel <https://www.youtube.com/channel/UC4vtx0j0wcP6s4n7hCTUs7A>`_
- `My Discord Server <https://discord.com/invite/uynSzaTAF3>`_
- `Download <https://pypi.org/project/webthon/>`_
