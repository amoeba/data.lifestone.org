<script type="ts">
export default {
  data() {
    return {
      sectionComponentCode:
        `
<Section>
  <template #head>
    My Section
  </template>

  My Section's Content

  <template #foot>
    My Section's Footer
  </template>
</Section>`,
      tabbedSectionComponentCode: `
<TabbedSection initialTab="hello">
  <template #tabs>
    <Tab id="hello">Hello</Tab>
    <Tab id="world">World</Tab>
  </template>
  <template #content>
    <TabContent id="hello">Hello Content</TabContent>
    <TabContent id="world">World Content</TabContent>
  </template>
</TabbedSection>`,
      twoColComponentCode: `
<TwoCol>
  <template #left>
    Left Side
  </template>
  <template #right>
    Right Side
  </template>
</TwoCol>`,
      calloutComponentCode: `
<Callout>
  <template #content>
    Ulysses, Ulysses — Soaring through all the galaxies. In search of Earth, flying in to the night.
  </template>
</Callout>`,
    }
  }
}
</script>

<template>
  <h2>Components</h2>

  <!-- Tables -->
  <!-- Cards -->
  <!-- Two/Three Col -->
  <!-- Tree -->
  <!-- Sectional -->
  <h3>Section Component</h3>
  <Section>
    <template #head>
      My Section
    </template>

    My Section's Content

    <template #foot>
      My Section's Footer
    </template>
  </Section>
  <details>
    <summary>Source code</summary>
    <Code>
      {{ sectionComponentCode }}
    </Code>
  </details>

  <h3>Tabbed Section Component</h3>
  <TabbedSection initialTab="hello">
    <template #tabs>
      <Tab id="hello">Hello</Tab>
      <Tab id="world">World</Tab>
    </template>
    <template #content>
      <TabContent id="hello">Hello Content</TabContent>
      <TabContent id="world">World Content</TabContent>
    </template>
  </TabbedSection>

  <details>
    <summary>Source code</summary>
    <Code>
      {{ tabbedSectionComponentCode }}
    </Code>
  </details>

  <h3>Tables</h3>
  <table>
    <thead>
      <tr>
        <td>A</td>
        <td>B</td>
        <td>C</td>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>A</td>
        <td>B</td>
        <td>C</td>
      </tr>
      <tr>
        <td>A</td>
        <td>B</td>
        <td>C</td>
      </tr>
      <tr>
        <td>A</td>
        <td>B</td>
        <td>C</td>
      </tr>
      <tr>
        <td>A</td>
        <td>B</td>
        <td>C</td>
      </tr>
      <tr>
        <td>A</td>
        <td>B</td>
        <td>C</td>
      </tr>
    </tbody>
  </table>

  <h3>Columnar Layouts</h3>
  <h4>Two-Column Layout</h4>
  <TwoCol>
    <template #left>
      Left Side
    </template>
    <template #right>
      Right Side
    </template>
  </TwoCol>

  <details>
    <summary>Source code</summary>
    <Code>
      {{ twoColComponentCode }}
    </Code>
  </details>

  <h4>Callout</h4>
  <Callout>
    <template #content>
      Ulysses, Ulysses — Soaring through all the galaxies. In search of Earth, flying in to the night.
    </template>
  </Callout>

  <details>
    <summary>Source code</summary>
    <Code>
      {{ calloutComponentCode }}
    </Code>
  </details>
</template>
