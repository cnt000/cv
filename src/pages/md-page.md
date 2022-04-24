---
setup: |
  import Layout from "../layouts/Layout.astro"
  import Cover from "../components/Cover.astro";
  import Skills from "../components/Skills.astro";
  import SectionTitle from "../components/SectionTitle.astro";
  import Experience from "../components/Experience.astro";
  import { data as contents } from "../data/data.js";
title: Edoardo Gargano
description: Senior front-end developer, full-stack developer, tech lead, JavaScript lover and Bologna JS Community Organizer with more than 10 years of experience in multinational companies
---

<Cover />
<SectionTitle title="Skills">
  <Skills />
</SectionTitle>
{contents.map(c => <SectionTitle title={c.title}>
  <Experience title={c.content.title} duration={c.content.duration} link={c.content.link} company={c.content.company} content={c.content.text} />
</SectionTitle>
)}
