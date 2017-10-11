# TestOkHttp3.9.0
Bug with Cookie and ProGuard

Original issue: https://github.com/square/okhttp/issues/3582


# Solution

Add this to `proguard-rules.pro`:

    -keepnames class okhttp3.internal.publicsuffix.PublicSuffixDatabase
    
Via https://github.com/square/okhttp/pull/3647
