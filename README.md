# SelectMemberActivity
重点关注
mScrollView：水平滚动条
mSelectedGridView：是个GridView
mTopSearchEditText：搜索框
mSearchIconView：放大镜图标

现在一个问题是图标大小不对，关注adjustSearchEditText方法：
marginRight=20;gridView=100;marginLeft=120;
对比二者是一样的。于是关注adjustGridView方法：相同。

怒刷FriendChooser:
mFriendDataManager：管理好友数据
mListPanel:是个包括titlebar的好友列表
mSearchPanelStub：搜索结果的stub
mFrameManager：不包括titlebar的ViewFlipper，好友列表
mScrollView：搜索框的水平滚动条
mBottomGridView:搜索后的gridview

。initTitleBar方法:初始化titlebar
。initBottomBar方法：初始化gridview，为gridview设置itemclick，当点击上面的图标时，相当于删除
。onBackEvent方法：当点击LeftBtn时，触发该方法。改方法主要触发quitSearchState方法。
。quitSearchState方法：将搜索框设置为空，设置退出动画animation。
。setupTitleBar方法：设置titlebar的名字、可见性等。
.onListViewItemClick方法：好友列表中某个item被点击触发的事件。
。onClickSearchBar方法：设置上升动画。
。inflateSearchPanelAndSetup方法：该方法在onAnimationEnd方法中被调用，也就是，动画结束后调用。该方法的目的是为searchtext添加监听
。adjustGridView：调整gridview
。refreshSearchResultList：主要是提供列表检索功能。被afterTextChanged方法调用
。GridViewAdapter：设置gridview
SearchResultAdapter：设置搜索列表listview
uiNotifyHandler：通知scrollview去scroll



DeviceDeleteFriendChooserActivity.java
DeviceAllShareFriendActivity.java
SmartHardwareActivity.java
DeviceAuthorityChooser.java
authority_chooser_item.xml
