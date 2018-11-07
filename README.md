# ADA Recommendations for TIND Forms
[Design Mock with suggesgted reorganization.](https://uchicago-library.github.io/tind/SubmitObject.html)

## Priority Items
- Restate what type of form it is as an h1 (Example: `<h1>Submit/Modify an Article</h1>`)
- Use h2s for all section headers
- Remove entire form from table. Only use tables for tabular data.
- Do not use `display:none;` or `visibility: hidden;`
- `<fieldset>` and `class="form-group"` are used
- Required elements use `<abbr title="required">*</abbr>`
- Show relationship between label and field (Example: `<label for="ISSN">ISSN/ISBN</label> <input type="text" id="ISSN" name="ISSN">`)
- Show relationship between input and help text (Example: `<input class="form-control" type="text" name="ISSN" aria-describedby="ISSNHelp" value=""><span id=”ISSNHelp” class="submitElemText">ISBN of the publication.</span>`)

## Resources
- Further documentation on [Accessible Web Forms](https://webaim.org/techniques/forms/controls) from WebAim
- [ADA code used by UChicago Library](https://github.com/uchicago-library/uchicago-library.github.io/blob/master/docs/code-resources.md) (and ADA more resources)

## Example code for one Section
```
<section>
    <h2>Submission Information</h2>
    <fieldset>
	<div class="form-group">
		<label><span class="submitElemHeader">Title <abbr title="required">*</abbr></span></label>
		<input type="text" class="form-control" name="TITLE" size="None" value="">
	</div>

	<div class="form-group">
		<label><span class="submitElemHeader">Abstract <abbr title="required">*</abbr></span></label>
		<textarea name="ABSTRACT" class="form-control" rows="4"></textarea>
	</div>

	<div class="form-group row">
		<label><span class="submitElemHeader">Date <abbr title="required">*</abbr></span></label>
		<input type="text" name="date_PUBLISHED" class="form-control" value="" id="dp1541018787105" aria-describedby="DateHelp" class="hasDatepicker">
		<span class="submitElemText" id="DateHelp">Date of publication. Format yyyy, yyyy-mm, or yyyy-mm-dd.</span>
	</div>
	</fieldset>
</section>
```
