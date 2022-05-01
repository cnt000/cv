---
setup: |
  import Layout from "../layouts/Layout.astro"
  import Cover from "../components/Cover.astro";
  import Skills from "../components/Skills.astro";
  import SectionTitle from "../components/SectionTitle.astro";
  import Experience from "../components/Experience.astro"
  import Skill from "../components/Skill.astro"
  import { contents as data } from "../data/contents.js";
title: Edoardo Gargano
description: Senior front-end developer, full-stack developer, tech lead, JavaScript lover and Bologna JS Community Organizer with more than 10 years of experience in multinational companies
---

<Cover />
<SectionTitle title="Skills">
  <Skills />
</SectionTitle>
{data.map(c => <SectionTitle title={c.title}>
  {c.content.map(section => <Experience title={section.title} duration={section.duration} link={section.link} company={section.company} content={section.text} />)}
</SectionTitle>
)}
<SectionTitle title="Languages">
  <ul class="grid grid-cols-3 md:grid-cols-3 gap-4">
    <Skill name="Italian" level="100" />
    <Skill name="English" level="90" />
    <Skill name="Deutsch" level="60" />
  </ul>
</SectionTitle>
