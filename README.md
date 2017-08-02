# SwitchLanguageDemo
Android应用内实现语言切换的demo


```
  /**
     * 
     * <切换语言>
     * 
     * @param language
     * @see [类、类#方法、类#成员]
     */
    protected void switchLanguage(String language)
    {
        // 设置应用语言类型
        Resources resources = getResources();
        Configuration config = resources.getConfiguration();
        DisplayMetrics dm = resources.getDisplayMetrics();
        if (language.equals("en"))
        {
            config.locale = Locale.ENGLISH;
        }
        else
        {
            // 简体中文
            config.locale = Locale.SIMPLIFIED_CHINESE;
        }
        resources.updateConfiguration(config, dm);

        // 保存设置语言的类型
        PreferenceUtil.commitString("language", language);
    }
```
