Upgrading to 1.8 could be done by replacing the rapla.war in your existing installation.
You need rapla 1.7.5 at least for this. If your version is lower see [UpgradingTo1\_7](UpgradingTo1_7.md)

In 1.8 all ids are replaced with unique UUIDS that are 64 bit random generated
numbers to ensure uniqueness of a rapla resource.


If you use the xml file rapla will convert to the new ids on the first save.


If you use a database, all data will be exported to the data.xml and the
database will be droped and recreated and the data.xml will be imported
again. This automatically happens if you start 1.8beta, so backup your
database first.

If you got problems with the database upgrade try an
alternative aproach. This is a repeatable process, so you should allwayw be alble to recover.

  1. Create a new database in MySql, postgres, etc.  ex. RaplaDB18
> 2. Run Rapla to create the new empty database
> 3. Run 1.7.8 raplaexport.cmd  to xml datafile. ( check 1.7 config
> file for output xml filename)
> 4. Run 1.8.1 raplaimport.cmd with the exported xml file.( set 1.8
> config file for input xml filename as per step 3)