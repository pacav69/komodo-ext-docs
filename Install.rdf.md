## Install.rdf
* Located in root
* user data
* target application

<code>

<?xml version="1.0"?>
<RDF xmlns="http://www.w3.org/1999/02/22-rdf-syntax-ns#"
     xmlns:em="http://www.mozilla.org/2004/em-rdf#">
    <Description about="urn:mozilla:install-manifest">
        <em:id>jphpextgen@silverpcgroup.com</em:id>
        <em:name>jphpextgen</em:name>
        <em:version>0.1b</em:version>
        <em:description></em:description>
        <em:creator>Me</em:creator>
        <em:homepageURL>http://silverpcgroup.com/jphpextgen</em:homepageURL>
        <em:type>2</em:type> <!-- type=extension -->

        <em:targetApplication>
            <Description>
                <!-- Komodo IDE's uuid -->
                <em:id>{36E66FA0-F259-11D9-850E-000D935D3368}</em:id>
                <em:minVersion>6.0</em:minVersion>
                <em:maxVersion>9.*</em:maxVersion>
            </Description>
        </em:targetApplication>
        <em:targetApplication>
            <Description>
                <!-- Komodo Edit's uuid -->
                <em:id>{b1042fb5-9e9c-11db-b107-000d935d3368}</em:id>
                <em:minVersion>6.0</em:minVersion>
                <em:maxVersion>9.*</em:maxVersion>
            </Description>
        </em:targetApplication>
    </Description>
</RDF>

</code>
