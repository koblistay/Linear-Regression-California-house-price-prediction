# Linear-Regression-California-house-price-prediction

Датасет: https://www.kaggle.com/datasets/harrywang/housing

EDA: https://colab.research.google.com/drive/1dt3nvtQzf4Uuiac61Jk2sVkTwPzcBnG3?usp=sharing

Были обучены следующие модели:

https://colab.research.google.com/drive/1dt3nvtQzf4Uuiac61Jk2sVkTwPzcBnG3?usp=sharing

https://colab.research.google.com/drive/1usqDBF2vN_M9iHAPpzrvT-VxOAL1PtxZ?usp=sharing

RidgeCV:
MSE train: 4.239941085227615e-06
MSE train: 1.0248983184078621e-05

MAE train: 3.276503595015895e-05
MAE train: 8.573539617790463e-05

GridSearchCV(ElasticNet):
MSE train: 2.4060699498281486e-05
MSE test: 4.940204430855466e-05

MAE train: 0.00010957484947126241
MAE train: 0.00011463985706270938

RandomForestRegressor(max_depth=15, n_estimators=300, n_jobs=-1, random_state=42):
rfr RMSE train: 0.0023347210192416314
rfr RMSE test: 0.0028100938915835484
rfr MAE train: 4.1574865887366845e-05
rfr MAE test: 5.948656966608713e-05
rfr r2 score train: 0.9403838304299004
rfr r2 score test: 0.945578863873837

XGBRegressor(n_estimators=500, learning_rate = 0.05, max_depth=6, subsample=0.8, colsample_bytree=0.8,random_state=42): ###ИЗ-ЗА Масштабирования произошла утечка данных!!!!!!!!
xgb RMSE train: 1.5728448422488014e-05
xgb RMSE test: 0.0006667729849386428
xgb MAE train: 3.280608417616052e-07
xgb MAE test: 8.093906489627345e-06
xgb r2 score train: 0.9999972943859402
xgb r2 score test: 0.9969360481684586

st = StackingRegressor(estimators = base_models, final_estimator=Ridge()) #base models (Ridge, RandomForestRegressor, XGBRegressor)
st RMSE train: 0.004404966157115788
st RMSE test: 0.005567176598671021
st MAE train: 6.991293903980904e-05
st MAE test: 0.00010332038607906674
st r2 score train: 0.7877834576495605
st r2 score test: 0.7864026116830181
