Localization
============

oTree's participant interface has been translated to the following languages:

- Chinese (simplified)
- French
- German
- Hungarian
- Italian
- Japanese
- Russian
- Spanish


This means that all built-in text that gets displayed to participants is
available in these languages. This includes things like:

-   Form validation messages
-   Wait page messages
-   Dates, times and numbers (e.g. "1.5" vs "1,5")

So, as long as you write your app's text in one of these languages,
all text that participants will see will be in that language.
For more information, see the Django documentation on
`translation <https://docs.djangoproject.com/en/1.8/topics/i18n/translation/>`__
and `format localization <https://docs.djangoproject.com/en/1.8/topics/i18n/formatting/>`__.


However, oTree's admin/experimenter interface is currently only available in English,
and the existing sample games have not been translated to any other languages.

Changing the language setting
-----------------------------

Go to ``settings.py``, change ``LANGUAGE_CODE``, and restart the server.

Writing your app in multiple languages
--------------------------------------

You may want your own app to work in multiple languages.
For example, let's say you want to run the same experiment with English and Chinese participants.

For this, you can use Django's `translation <https://docs.djangoproject.com/en/1.8/topics/i18n/translation/>`__
system.

A quick summary:

- In templates, use ``{% blocktrans trimmed %}...{% endblocktrans %}``
- In Python code, use ``ugettext``.
- Run ``django-admin makemessages`` to create the ``.po`` files
- Edit the ``.po`` file in `Poedit <http://poedit.net/>`__
- Run ``django-admin compilemessages``
- Go to ``settings.py``, change ``LANGUAGE_CODE``, and restart the server.

Volunteering to localize oTree
------------------------------

You are invited to contribute support for your own language in oTree.

It's a simple task; you provide translations of about 20 English phrases.
Currently we are only translating the participant interface,
although we plan to translate the admin interface and launcher later.

`Here <https://github.com/oTree-org/otree-core/blob/master/otree/locale/fr/LC_MESSAGES/django.po>`__
is an example of an already completed translation to French. These files can be edited in `Poedit <https://poedit.net/>`__.

Please contact chris@otree.org for more details.

