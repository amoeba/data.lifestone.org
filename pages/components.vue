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
</template>
