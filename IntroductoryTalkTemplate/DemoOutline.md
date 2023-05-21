# Orchard Core demo outline

Use the snippets in the Snippets file to quickly copy text instead of having to type it all in.

This assumes you already have an Orchard Core solution ready but as a first step you can also demo creating it. The corresponding snippet uses [Lombiq Utility Scripts
](https://github.com/Lombiq/Utility-Scripts).

1. Setup with the Blog recipe (as it’s simple yet a quite complete overview of Orchard features; you may use Agency too, but the rest of these notes assume you’ve used Blog), briefly explain every option and field on the setup screen. "Password1!" is a simple demo password that you can use.
2. Access the admin, show that it’s responsive.
3. The Orchard content model: Show the basics of Orchard’s concepts around content, since that’s in the core of the CMS.
	1. Show and explain the default Blog Post and Article content items. Show and compare their content types (like telling that their titles are handled by the same Title Part).
	2. As a more complex demo create a Page with an Html Widget, explain Preview, draft and versioning.
	3. Explain content definition: Content types/parts/fields. Modify the Html Widget type to use a WYSIWIG editor.
	4. Create a new widget content type, Markdown Widget with MarkdownBody, and demo it with the same Page.
4. Batteries included: Show what other features are built into Orchard that cover most of what a usual website should do.
	1. Media Library: Upload images and show them on a page.
	2. User management basics.
	3. Recipes again, import/export
	4. Modules and themes: Basic concepts of Orchard extensibility, how to configure them. Enable another theme (like Agency) to show how themes work.
	5. Enable Audit Trail, configure all content types to record events for. Show how creating, then editing a Blog Post is recorded, with diffs. Use the occasion to explain versioning.
	6. Enable Workflows and create a Workflow Type to show a notification when content is published (notification Liquid: `Thank you {{User.Identity.Name}}!`).
	7. Layers and widgets: Show how the same widget concept used with Pages can be utilized again.
	8. Queries and Search with Lucene: Explain the concept of queries, what Lucene is, how listing content items works. You can also explain SQL Queries.
	9. Templates: Create a template to override some small shape template.
	10. Localization: Configure site cultures, set up a language selector, create localized content items, mention how UI labels are localized.
5. Introduction to extending Orchard
	1. Create a theme with the command line template if you haven't created it together with the solution: `dotnet new octheme -n "OrchardCore.Theme"`
	2. Modify *Layout.liquid* (e.g. you can write something in front of the site name) and explain the concept of shapes and shape template overrides.
	3. Show some simple examples from the [Training Demo module](https://github.com/Lombiq/Orchard-Training-Demo-Module). `YourFirstOrchardCoreController` is a good example. Alternatively or additionally, you can show the code of something simpler, like `TitlePart`, in the Orchard Core source. You can correlate what people have seen on the admin with the code. Explain that a module/theme is just an ASP.NET Core area and for a quick start, you can turn a C# project into an Orchard Core extension by not much more than adding a Manifest file.
