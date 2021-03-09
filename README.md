# csl-fmipa-bio
CSL untuk PS Biologi

---
## Update

9 Mar 2021: Pembuatan csl dan penambahan sitasi untuk jurnal dan artikel

9 Mar 2021: Macro using

9 Mar 2021: Pembuatan csl khusus Fauna Kalimantan

---

## Code

```csl
<?xml version="1.0" encoding="utf-8"?>
<style class="in-text" version="1.0" name-form="count" and="symbol" et-al-min="2" initialize-with="." name-as-sort-order="first" initialize-with-hyphen="false" demote-non-dropping-particle="never" xmlns="http://purl.org/net/xbiblio/csl">
  <info>
    <title>PS Bio, FMIPA</title>
    <id>http://www.zotero.org/styles/ps-bio-fmipa</id>
    <link rel="self" href="http://www.zotero.org/styles/ps-bio-fmipa"/>
    <updated>2021-03-09T02:41:12+00:00</updated>
  </info>
  <citation name-form="count" et-al-min="2" et-al-use-first="2">
    <sort>
      <key variable="author" names-min="1" names-use-first="1"/>
    </sort>
    <layout font-style="normal" font-weight="normal" text-decoration="none" prefix="(">
      <choose>
        <if match="none" variable="author">
          <text value="Anonim" suffix=", "/>
        </if>
      </choose>
      <names variable="author" delimiter=" " suffix=", "/>
      <date date-parts="year" form="text" variable="issued" suffix=")"/>
    </layout>
  </citation>
  <bibliography name-delimiter=", " name-form="count" and="symbol" initialize-with="." name-as-sort-order="first" names-delimiter="" subsequent-author-substitute-rule="partial-first" line-spacing="2" hanging-indent="true">
    <sort>
      <key variable="author"/>
    </sort>
    <layout font-weight="normal">
      <choose>
        <if match="none" variable="author">
          <text value="Anonim" suffix=". "/>
        </if>
      </choose>
      <names variable="author" suffix=". "/>
      <date date-parts="year" form="text" variable="issued" suffix=". "/>
      <choose>
        <if type="article-journal" match="any">
          <text variable="title" font-style="normal" suffix=". "/>
        </if>
        <else>
          <text variable="title" text-case="capitalize-all" font-style="italic" suffix=". "/>
        </else>
      </choose>
      <choose>
        <if type="article-journal" match="any">
          <group>
            <text variable="container-title" font-style="italic" suffix=" "/>
            <number font-style="italic" font-weight="bold" suffix=" " variable="volume"/>
            <number prefix="(" suffix=") " variable="issue"/>
            <label text-case="capitalize-first" suffix=": " variable="page" form="symbol"/>
            <text variable="page" suffix="."/>
          </group>
        </if>
        <else-if type="book" match="any">
          <choose>
            <if match="all" variable="collection-title collection-editor">
              <text variable="collection-title" prefix=" dalam " suffix="."/>
            </if>
          </choose>
          <text variable="publisher" suffix=": "/>
          <text variable="publisher-place"/>
        </else-if>
      </choose>
    </layout>
  </bibliography>
</style>
```
