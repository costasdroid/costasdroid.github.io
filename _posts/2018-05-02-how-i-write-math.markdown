---
layout: post
title:  "Πώς γράφω Μαθηματικά 1"
date:   2018-05-02 23:59:28 +0300
categories: tech
description: Αν θέλεις να μάθεις να γράφεις μαθηματικά ή σε βασανίζει το πρόγραμμα που χρησιμοποιείς.
---

# Τι χρειάζεσαι
Τίποτα που δεν έχεις ήδη εγκατεστημένο
- Browser (Firefox, Chrome, Safari, Edge...)
- Notepad
- Internet

# Γιατί κείμενο
Έχω αναφέρει ότι είμαι υπέρμαχος του απλού κειμένου. Εξηγώ. Σκέψου να έχεις αγοράσει ή ως γνωστός πειρατής κατεβάσει το τέλειο πρόγραμμα που γράφει μαθηματικά. Το ιδανικό πρόγραμμα το φαντάζομαι ως να γράφεις και να βλέπεις το αποτέλεσμα (το γνωστό WYSIWYG). Θέλεις πλήρη στοίχιση, μερικά bold, το κλάσμα με το ολοκλήρωμα και να καμαρώνεις το έργο σου. Δεν το κρύβω, ζηλεύω. Υπάρχουν τόσα και τόσα προγράμματα εκεί έξω που να το κάνουν αυτό. Microsoft Word με MathType, Scientific Workplace, LyX... άλλα με πληρωμή, άλλα ελεύθερα. Τώρα σκέψου να χρειαστεί να τα αλλάξεις αυτά που έγραψες. Στην ανάγκη. Σε άλλον υπολογιστή. Μετά από καιρό. Αληθινή κόλαση? Όλα τα προηγούμενα προγράμματα αφού είναι WYSIWYG έχουν τον δικό τους κώδικα (μορφοποίηση) εσωτερικά του αρχείου, το οποίο το κάνει να είναι αδύνατο να διαβαστεί. Δοκιμάστε να ανοίξετε ένα word με επεξεργαστή κειμένου.

Αν γνωρίζετε τι σημαίνει git μπορείτε να προσπεράσετε αυτή τη παράγραφο. Οι υπόλοιποι προσπαθήστε να κρατήσετε ένα έγγραφο, όταν έχει περάσει από διορθώσεις (από εσένα, από άλλα άτομα, ξανά από εσένα...). Δεν λέω, τα ίδια τα λογισμικά έχουν από μόνα τους αυτή τη λειτουργία, αλλά λειτουργεί μόνο μέσα στο πρόγραμμα και δεν μπορεί να ανέβει κάπου να το έχεις πρόχειρο π.χ. στο github.

Αν όλα ήταν απλό κείμενο με σημάδια μορφοποίησης, θα μπορούσε να επεξεργαστεί με οποιοδήποτε επεξεργαστή κειμένου. Ακόμα και με nano ή notepad. Φαντάσου τώρα ακόμα και τα μαθηματικά να ήταν απλό κείμενο, π.χ. για να εμφανιστεί κλάσμα σε ολοκλήρωμα θα έγραφες κάτι σαν `\int_a^b{\frac{2}{x^2+1}}dx` και θα εμφανιζόταν \$\$\int_a^b{\frac{2}{x^2+1}}dx\$\$

Μαγικό?

# Απο Μηχανής Θεός
Σίγουρα υπάρχουν πολλοί τρόποι να γράψεις μαθηματικά με κείμενο. Ο τίτλος είναι "Γράφω Μαθηματικά 1" γιατί είναι ο πιο απλός. Η πιο κομψή λύση είναι το [MathJax](https://www.mathjax.org/). Σε προκαλώ... Δημιούργησε ένα αρχείο με κατάληξη `html`. Τοποθέτησε τα απολύτως απαραίτητα για ιστοσελίδα, δηλαδή

```html
<!DOCTYPE html>
<head>
</head>
<body>
</body>
</html>
```

Και βάλε στο `head` τον κώδικα όπως τον βλέπεις

```html
<script type="text/x-mathjax-config">
  MathJax.Hub.Config({
    extensions: ["tex2jax.js"],
    jax: ["input/TeX", "output/HTML-CSS"],
    tex2jax: {
      inlineMath: [ ['$','$'], ["\\(","\\)"] ],
      displayMath: [ ['$$','$$'], ["\\[","\\]"] ],
      processEscapes: true
    },
    "HTML-CSS": { availableFonts: ["TeX"] }
  });
</script>
<script src='https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.4/MathJax.js?config=TeX-MML-AM_CHTML' async></script>
```

Αν ανοίξεις την σελίδα στο browser, δεν θα δεις τίποτα. Απολύτως τίποτα. Βάλε ανάμεσα στο `body` ότι θέλεις. Αν θέλεις μαθηματικά άνοιξε και κλείσε την παράσταση σε `$`. Ανανέωσε τη σελίδα. Φοβερό? Μαθηματικά χωρίς τρίτο πρόγραμμα? Μόνο με κείμενο? Και το ανεβάζεις όπου θέλεις να το ανοίξει όποιος θέλει, όποτε θέλει και όπου θέλει? Όρισε το τέλειο.

Αν βάλεις και σωστά τη μορφοποίηση, τύπωσέ το, κάνε το pdf... Τύφλα να έχει το Word.

# Σύνδεσμοι για στήσιμο

1. [MathJax](https://www.mathjax.org/)

# Σύνδεσμοι για γράψιμο

1. [Html](https://www.w3schools.com/html/html_intro.asp)
2. [$\LaTeX$](https://en.wikibooks.org/wiki/LaTeX/Mathematics)
