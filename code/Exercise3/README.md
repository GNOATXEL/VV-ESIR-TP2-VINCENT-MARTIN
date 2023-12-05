# Code of your exercise

Voilà le .xml obtenu en exportant :

```
<rule name="ifpuissance3"
      language="java"
      message="euh ya plus de 3 ifs imbriqués bozo c pas bien :nerd:"
      class="net.sourceforge.pmd.lang.rule.XPathRule">
  <description>
    Euh bah quand y&apos;a 3 ifs emboîtés ça couine
  </description>
  <priority>1</priority>
  <properties>
    <property name="version" value="3.1"/>
    <property name="xpath">
      <value>
        <![CDATA[
//IfStatement[count(ancestor::IfStatement) + 1 >= 2]

]]>
      </value>
    </property>
  </properties>
</rule>
```
