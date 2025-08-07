
<img src="https://raw.githubusercontent.com/muhsinciftci/pyclimaterisk/main/pyclimaterisk/data/logo.png" align="right" height="175" alt=""/>

This mini package provides access to latin american climate risk indices
at different categories. Those indices are derived from a large corpus
of newspapers archives and available at monthly and daily frequency. It
further provides certain climate related events (laws, legislation,
presidential decrees).

The package provides three different functions. Python library `Polars`
must be installed. The package can be found on PyPI under the link:
<https://pypi.org/project/pyclimaterisk/>

``` python
import pyclimaterisk as cr
```

``` python
cr.get_monthly_data().head()
```

<div><style>
.dataframe > thead > tr,
.dataframe > tbody > tr {
  text-align: right;
  white-space: pre-wrap;
}
</style>
<small>shape: (5, 9)</small><table border="1" class="dataframe"><thead><tr><th>country</th><th>date</th><th>year</th><th>month</th><th>newspapers_agg</th><th>newspapers_reg</th><th>newspapers_opp</th><th>newspapers_phy</th><th>newspapers_risk</th></tr><tr><td>str</td><td>date</td><td>i32</td><td>i32</td><td>f64</td><td>f64</td><td>f64</td><td>f64</td><td>f64</td></tr></thead><tbody><tr><td>&quot;Brazil&quot;</td><td>2000-01-01</td><td>2000</td><td>1</td><td>2.614197</td><td>1.406846</td><td>0.460916</td><td>2.024123</td><td>0.338765</td></tr><tr><td>&quot;Brazil&quot;</td><td>2000-02-01</td><td>2000</td><td>2</td><td>2.010683</td><td>1.502156</td><td>0.709737</td><td>1.314579</td><td>0.21611</td></tr><tr><td>&quot;Brazil&quot;</td><td>2000-03-01</td><td>2000</td><td>3</td><td>1.467206</td><td>1.376422</td><td>0.286903</td><td>1.207837</td><td>0.0</td></tr><tr><td>&quot;Brazil&quot;</td><td>2000-04-01</td><td>2000</td><td>4</td><td>1.752851</td><td>1.289066</td><td>0.392993</td><td>1.407381</td><td>0.349019</td></tr><tr><td>&quot;Brazil&quot;</td><td>2000-05-01</td><td>2000</td><td>5</td><td>1.618396</td><td>1.39724</td><td>0.381636</td><td>0.885867</td><td>0.065075</td></tr></tbody></table></div>

``` python
cr.get_daily_data().head()
```

<div><style>
.dataframe > thead > tr,
.dataframe > tbody > tr {
  text-align: right;
  white-space: pre-wrap;
}
</style>
<small>shape: (5, 7)</small><table border="1" class="dataframe"><thead><tr><th>country</th><th>date</th><th>newspapers_agg</th><th>newspapers_reg</th><th>newspapers_opp</th><th>newspapers_phy</th><th>newspapers_risk</th></tr><tr><td>str</td><td>date</td><td>f64</td><td>f64</td><td>f64</td><td>f64</td><td>f64</td></tr></thead><tbody><tr><td>&quot;Costa Rica&quot;</td><td>2002-10-29</td><td>0.0</td><td>0.0</td><td>0.0</td><td>0.0</td><td>0.0</td></tr><tr><td>&quot;Costa Rica&quot;</td><td>2002-10-30</td><td>9.746684</td><td>0.0</td><td>0.0</td><td>0.0</td><td>0.0</td></tr><tr><td>&quot;Costa Rica&quot;</td><td>2002-10-31</td><td>0.0</td><td>0.0</td><td>0.0</td><td>0.0</td><td>0.0</td></tr><tr><td>&quot;Costa Rica&quot;</td><td>2002-11-01</td><td>2.206796</td><td>0.0</td><td>0.0</td><td>0.0</td><td>0.0</td></tr><tr><td>&quot;Costa Rica&quot;</td><td>2002-11-02</td><td>0.0</td><td>0.0</td><td>0.0</td><td>0.0</td><td>0.0</td></tr></tbody></table></div>

``` python
cr.get_events().head()
```

<div><style>
.dataframe > thead > tr,
.dataframe > tbody > tr {
  text-align: right;
  white-space: pre-wrap;
}
</style>
<small>shape: (5, 3)</small><table border="1" class="dataframe"><thead><tr><th>Country</th><th>date</th><th>Title</th></tr><tr><td>str</td><td>date</td><td>str</td></tr></thead><tbody><tr><td>&quot;Brazil&quot;</td><td>2017-06-27</td><td>&quot;Establishing the Brazilian For…</td></tr><tr><td>&quot;Brazil&quot;</td><td>2018-03-16</td><td>&quot;RenovaBio&quot;</td></tr><tr><td>&quot;Brazil&quot;</td><td>2018-07-05</td><td>&quot;Procedures and conditions for …</td></tr><tr><td>&quot;Brazil&quot;</td><td>2018-08-02</td><td>&quot;Efficiency Standards for Refri…</td></tr><tr><td>&quot;Brazil&quot;</td><td>2018-08-02</td><td>&quot;Reduction of losses of distrib…</td></tr></tbody></table></div>

If you use this data set, please kindly cite our work as: - Muhsin
Ciftci, and Christina Kolerus. “Climate News and Asset Valuations:
Insights from Latin America”, IMF Working Papers 2025, 037 (2025),
<https://doi.org/10.5089/9798229000932.001>
