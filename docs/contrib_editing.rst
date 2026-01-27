.. _contrib_editing:

Editing the guidelines
----------------------
Found a typo or want to revise major parts of the guidelines? Editing the
guidelines can be done directly on GitHub.

1. Go to http://guidelines.openaire.eu and find the page you want to edit.

2. Click "Edit on GitHub" in the top right corner. This will take you directly
   to the source file on GitHub.

   .. image:: images/editongithub.png
      :align: center
      :scale: 100%

3. Click the edit icon. If it's grayed out, it's likely because you are not
   signed into your GitHub account.

   .. image:: images/editicon.png
      :align: center
      :scale: 100%

4. Edit the file. Note that the editor supports full-screen mode and allows you
   to preview your changes.

   .. image:: images/editfile.png
      :align: center
      :scale: 100%

5. Once your done editing the file, write a small commit message to
   propose the file change and finally click "Propose file change". This will
   allow you to create what is called a "pull request". See next section.


Submitting a pull request
-------------------------

1. After clicking "Propose file change", you can review your changes compared
   against the latest master version. If you're happy with the changes, go
   a head and click "Create pull request".

   .. image:: images/comparechanges.png
      :align: center
      :scale: 50%

2. Enter a title for your pull request and describe the changes made if
   necessary and finally click, "Create pull request".

   .. image:: images/openpr.png
      :align: center
      :scale: 50%


Discussing the pull request
---------------------------

1. Everyone can see your proposed changes, and the changes can be discussed.
   Every pull request is also automatically checked for errors in the
   documentation source files by an external service called TravisCI.

   .. image:: images/pr.png
         :align: center
         :scale: 50%


2. The tab "Files changed", others can see the changes to the files, and
   comment on individual lines as well.


Merging the pull request
------------------------

Once the changes have been approved, one of the editors will merge the changes
into the master version. After the merge, the changes are automatically
propagated to online version on http://guidelines.openaire.eu.
