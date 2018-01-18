# Patch Bootstrap CSS to 24 columns grid

Add more column CSS classes (like `.col-xs-11_5`, `.col-sm-pull-1_5`, `.col-md-push-9_5`, `.col-lg-offset-0_5`,...) to Bootstrap 3 to support 24 columns grid.

## Getting Started

Use this CSS file beside with Bootstrap CSS file like:
```html
<!-- Bootstrap -->
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css"/>
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap24@3.3/bootstrap24.min.css"/>
```
**See** the [Usage Examples](https://nthachus.github.io/bootstrap24/examples.html) for more details.

## Components

### 24 columns grid

Width of `.col-sm-1_5` equals to `.col-sm-1` and a half; and so on...
```html
<div class="row">
  <div class="col-sm-3_5 col-md-3 col-lg-2_5 col-sm-push-8_5 col-md-push-9 col-lg-push-9_5">.col-sm-3_5</div>
  <div class="col-sm-8_5 col-md-9 col-lg-9_5 col-sm-pull-3_5 col-md-pull-3 col-lg-pull-2_5">.col-sm-8_5</div>
</div>
<div class="row">
  <div class="col-xs-5_5 col-sm-7 col-md-6_5 col-lg-6 col-xs-offset-6_5 col-sm-offset-5 col-md-offset-5_5 col-lg-offset-6">.col-xs-5_5</div>
</div>
```
**Note** that the new classes are not inheritance (e.g. `.col-md-3_5` class only affect to `md` devices, not `sm` nor `lg` devices). **So**, you need to use next-size column classes beside the custom classes like `col-sm-3_5 col-md-3`, or `col-md-7_5 col-lg-7`, or `col-md-3_5 col-lg-2_5`,...

### Colored tooltips

Colored Bootstrap tooltips with new CSS classes: `.tooltip-success`, `.tooltip-info`, `.tooltip-warning` and `.tooltip-danger`.
```html
<a href="#" data-toggle="tooltip" title="Hooray!" class="tooltip-warning">Hover over me</a>
```

### Colored modals

Now you can colored Bootstrap modals with CSS classes `.panel-*` such as `.panel-info`, `.panel-warning`.
```html
<div class="modal fade" tabindex="-1" role="dialog">
  <div class="modal-dialog" role="document">
    <div class="modal-content panel-info">
      <div class="modal-header panel-heading">
        <button type="button" class="close" data-dismiss="modal" aria-label="Close"><span aria-hidden="true">&times;</span></button>
        <h4 class="modal-title">Modal Header</h4>
      </div>
      <div class="modal-body">
        <p>Some text in the modal.</p>
      </div>
    </div>
    <!-- /.modal-content -->
  </div>
</div>
```

### No rounded corners

There are new 3 CSS classes to allow to prevent Bootstrap CSS rounded corners: `.no-rounded` and `.no-rounded-tip`.
```html
<pre class="no-rounded"><code>pre.no-rounded and .img-thumbnail</code></pre>
<img src="https://via.placeholder.com/100" alt="100x100" class="img-thumbnail no-rounded"/>

<!-- Tooltips -->
<a href="#" data-toggle="tooltip" title="Info!" class="btn btn-info no-rounded-tip">.no-rounded-tip</a>

<!-- Popovers -->
<a href="#" class="btn btn-danger no-rounded-tip" role="button" data-toggle="popover" data-trigger="focus"
   title="Dismissible popover" data-content="And here's some amazing content. It's very engaging. Right?">.no-rounded-tip</a>
```
Add `.no-rounded` class to any elements that you want to prevent rounded corners like: `.form-control`, `.btn`, `.dropdown-menu`, `.input-group-addon`, `.nav-tabs`, `.nav-pills`, `.navbar`, `.navbar-toggle`, `.breadcrumb`, `.pagination`, `.alert`, `.progress`, `.list-group`, `.panel`, `.well`, `.modal-content`,...

### Extras

Labels in `.form-horizontal` can be aligned left with existing `.text-left` class.
```html
<form class="form-horizontal">
  <div class="form-group">
    <label for="email" class="col-sm-3_5 col-md-3 control-label text-left">Email <b class="text-danger">*</b></label>
    <div class="col-sm-8_5 col-md-9">
      <input type="email" class="form-control" id="email" placeholder="Enter email"/>
    </div>
  </div>
  ...
</form>
```

Use `.row-condensed` to make Bootstrap grids more compact by cutting column padding in half.
```html
<div class="row row-condensed">
  <div class="col-md-7_5 col-lg-7">.col-md-7_5</div>
  <div class="col-md-4_5 col-lg-4">.col-md-4_5</div>
</div>
```

Support horizontal collapsing.
```html
<button type="button" class="btn btn-primary" data-toggle="collapse" data-target="#collapseX">collapse X</button>
<div class="collapse width" id="collapseX">
  <div style="width:250px; height:250px; background:blue;"></div>
</div>
```

Add new helper classes: `.no-underline`, `.bg-transparent`, `.full-width`, `.full-height`
```css
.no-underline { text-decoration: none; }
.bg-transparent { background-color: transparent; }

.full-width { width: 100%; }
.full-height { height: 100%; }
```

## Development

Prerequisites
* [Node.js](https://nodejs.org/) >=4.0

Installing
```bash
npm install
```

Built With
```bash
npm run build
```

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details
