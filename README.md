# kaggle_houseprice_pred
It is a competition item of kaggle_house_price_pred, and the download address of the dataset is https://www.kaggle.com/c/house-prices-advanced-regression-techniques;训练数据集包括1460个样本，每个样本80个特征和1个标签，而测试数据包含1459个样本，每个样本80个特征。
DATA_HUB['kaggle_house_train']为脚本下载并缓存Kaggle房屋数据集。
train_data我们使用pandas分别加载包含训练数据和测试数据的两个CSV文件。
def get_net():定义网络
def log_rmse(net, features, labels):用价格预测的对数来衡量差异
def get_k_fold_data(k, i, X, y):k折交叉验证
submission.to_csv('submission.csv', index=False)提交你的Kaggle预测
小结：真实数据通常混合了不同的数据类型，需要进行预处理。将实值数据重新缩放为零均值和单位方差是一个很好的默认设置。用它们的平均值替换缺失的值也是一个很好的默认设置。将类别特征转化为指标特征，可以使我们把它们当作一个独热向量来对待。我们可以使用 K 折交叉验证来选择模型并调整超参数。对数对于相对误差很有用。
