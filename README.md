PagerIndicator
==============

Page Indicator Library Like IOS in Android


in Layout.xml
<RelativeLayout
            android:layout_width="fill_parent"
            android:layout_height="fill_parent" >

            <!-- ViewPager  -->

           <android.support.v4.view.ViewPager
                android:id="@+id/vpDots"
                android:layout_width="fill_parent"
                android:layout_height="fill_parent" />

            <com.viewpagerindicator.CirclePageIndicator
                android:id="@+id/indicator"
                android:layout_width="fill_parent"
                android:layout_height="wrap_content"
                android:layout_alignParentBottom="true"
                android:layout_alignBottom="@+id/vpDots"
                android:background="@android:color/transparent"
                app:fillColor="@android:color/darker_gray"
                app:pageColor="@android:color/white"
                app:radius="6dp"
                android:paddingBottom="5dp" />
        </RelativeLayout>
        
In .Java

ViewPager _mViewPager = (ViewPager) findViewById(R.id.vpDots);
		_mViewPager.setAdapter(mAdapter);

PageIndicator mIndicator = (CirclePageIndicator)findViewById(R.id.indicator);
		mIndicator.setViewPager(_mViewPager);
