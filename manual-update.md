# Manual update

**1 - Read the release notes to know what had been changed.**

For each stable release we will have some notes, and extra steps,  
  developers need to do to update the last release to the new release.


For Example:


**2 - Backups**

> * Backup your project database.
>
> * Backup your project files.

**3 - Get the packaged files for the new version of Varbase 8.4.x**

> * **From Drupal website: **[https://www.drupal.org/project/varbase](https://www.drupal.org/project/varbase)
>
> * **Using Varbase-Build:**  [https://packagist.org/packages/vardot/varbase-build](https://packagist.org/packages/vardot/varbase-build)

**4 - From your terminal, change directory to the root directory of your project to do the update:**

**For Example:**

---

**Given** that we do have a project at the /var/www/html/projects/example folder  
  **And** we do have our custom themes, features, custom modules in  
         /var/www/html/projects/example/themes/custom/  
         /var/www/html/projects/example/modules/custom/  
         /var/www/html/projects/example/sites/default  
         so on ...  
         like contributed modules which we had theme added  
         while working on the project.

**And** we opened a terminal console window  
  **And** we changed directory to our project folder  
         cd /var/www/html/projects/example in Linux

**When** we delete all files and folders, except our changes on Varbase.  
 **Then** we will be left with only custom changes

**When** we copy all Varbase files  
  **And** we make sure that we do not have any overridden files or folders  
         only delete old ones and copy new folder of modules to the same place

---

** 5 - Set the right file permissions.**

** 6 - Update composer packages.**

* $ composer update

* Make sure that you do have modules in the right place.

** 7 -  Import Varbase Core Features and Bundles:**

---

**Given** that you are logged in with the "webmaster" user


**And** the "Features" module is enabled

 **And** the "Features UI" module is enabled

**When** you go to "admin/config/development/features"

**Then** you should not see any changed features in the Varbase core bundle.

**When** you click on all "Changed"

**Then** you will be able to see all changes

**And** you will be able to import new changes if you need them

---

**8 - Do your Drupal 8 database updates**

* By the terminal "drush updb".
* By the web browser  by going to "yousite.domain/update.php" 

**9 - Regression test the full site.**

* Done :\)



