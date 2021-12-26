# Mein Shell-Skript Aufgabe 4
# Ursula Münich 2021-12-26

sed -Ee 's/[ ]//g' 2021-11-29-Article_list_dirty.tsv > ohneblank.tsv
sed '75,77d' ohneblank.tsv > ohnezeilen1.tsv
sed '19,2d' ohnezeilen1.tsv > ohnezeilen2.tsv
sed '7,10d' ohnezeilen2.tsv > ohnezeilen3.tsv
cut -f 2,15 ohnezeilen3.tsv > ohnezeilen4.tsv
sed '24,32d' ohnezeilen4.tsv > ohnezeilen5.tsv
sed '1d' ohnezeilen5.tsv > ohnezeilen6.tsv
sed -Ee 's/[ISSN:]//g' ohnezeilen6.tsv > ohnezeilen7.tsv
sed -Ee 's/[issn]//g' ohnezeilen7.tsv > ohnezeilen8.tsv
sort ohnezeilen8.tsv > ohnezeilen9.tsv
cat ohnezeilen9.tsv
uniq ohnezeilen9.tsv > ohnezeilen10.tsv
