The rate data file used as input is historico_txref.csv. If needed, I also uploaded parser_curva_b3.ipynb, which contains the scraping logic to extract the curve data directly from B3.

In terms of the notebook flow:

00_build_data.ipynb prepares the core DI curve dataset and builds the forward-based spread used in the analysis.

01_build_di_curve_and_forwards.ipynb generates the main curve and spread figures

02_build_macro_inflation_dataset.ipynb downloads and aligns the macro data, then merges it with the curve dataset.

03_statistical_validation.ipynb runs the main statistical tests and exports the tables/figures used in the analysis

04_walk_forward_backtest_fair_value_zscore.ipynb implements the walk-forward fair value model and backtest, and exports the performance outputs.

05_analyse_fair_value_trend_stationarity.ipynb adds the final diagnostic analysis, including stationarity/relationship checks and complementary figures

So each notebook is responsible for exporting the processed data, figures, and tables that are later used in the analysis and in the final report.
