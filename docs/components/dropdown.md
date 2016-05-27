---
layout: docs
title: Dropdown
group: components
---

## Contents

* toc
{:toc}

## Examples

<script src="{{ site.baseurl }}/demos/dropdown/dropdown-select.js"></script>


{% example html %}
<div ng-app="demos.dropdownSelect" ng-controller="DemoCtrl as ctrl">

<dropdown-select
    model="ctrl.selectedItem" options="ctrl.options"></dropdown-select>

<div ng-bind-template="[\{\{ctrl.selectedItem.value\}\}] \{\{ctrl.selectedItem.title\}\}">

</div>
{% endexample %}

{% highlight js %}
angular
  .module('demos.dropdownSelect', ['ccms.components'])
  .controller('DemoCtrl', function($scope) {
    this.options = {
      placeholderText: '请选择',

      valueField: 'value',
      displayField: 'title',

      searchable: true,

      datalist: [
        {title: '北京', value: 'bj'},
        {title: '上海', value: 'sh'},
        {title: '深圳', value: 'sz'},
        {title: '广州', value: 'gz'}
      ]

    };
  });
{% endhighlight %}
