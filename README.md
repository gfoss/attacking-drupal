#Attacking Drupal
greg . foss [at] LogRhythm . com

v0.2 Beta -- 1/28/2014

Scripts and a basic checklist used to augment the penetration testing and security process of Drupal web applications. These scripts and the drupal-security-checklist.pdf coincide with the 'Attacking Drupal' presentation, which covers many common configuration flaws associated with Drupal web applications.

     Presentation: http://www.slideshare.net/heinzarelli/attacking-drupal
     
--------------------------------------------------

#[account-forcer]
A Drupal account brute-forceing script.

There are two versions, Drupal 6 and Drupal 7 as each has slight differences in the code. This script will work with any wordlist against a Drupal 6 application, assuming that it does not have additional protections in place such as rate limiting, MFA, SSO, CAPTCHA (implemented properly) etc. Drupal 7 is a bit trickier, and will only work if a small wordlist is used.

     To run...
          Drupal 6     ./d6-account-forcer.sh (then follow the prompts)
          Drupal 7     ./d7-account-forcer.sh (then follow the prompts)
     
--------------------------------------------------

#[devel-exploit]
This script will harvest all user e-mails and password hashes from an application running the Drupal Devel module.

There are two versions, Drupal 6 and Drupal 7 as each has slight differences in the code. This script can be used to automate the task of extracting user account information from any site that has left the devel module enabled.

     To run...
          Drupal 6     ./d6-devel-exploit.sh (then follow the prompts)
          Drupal 7     ./d7-devel-exploit.sh (then follow the prompts)
     
--------------------------------------------------

#[drupal-security-checklist]
Basic checklist which helps developers and security teams alike avoid common security pitfalls when developing Drupal web applications.

--------------------------------------------------

#[presentation-&-movies]
The full OWASP presentation and movies are located in the /presentation/ directory.
Alternatively, you can view the presentation on slideshare:
  http://www.slideshare.net/heinzarelli/attacking-drupal

--------------------------------------------------

#[changelog]

	1/28/2014 - Updates
    Presentation
      -slides updated to include hardening
      -checklist updated to include hardening
      -drupal-account-forcer.mp4 - updated and shortened
    Scripts
      -adding User Agent strings
      -clear screen before run
      -minor tweaks...

  	1/15/2014 - Public Release

--------------------------------------------------
