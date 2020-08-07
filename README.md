# OPdf

基于SurfaceView的单页PDF查看，可自由缩放和平移。
使用方便，尤其适合展示复杂的PDF页面。

        //创建renderer 
        //create renderer object
        mRenderer = new OPdfSurfaceRenderer(surfaceView, pdfFile, 0);
        
        //在缩放和拖动时提高清晰度
        //improve drawing result when transforming, it will cause some performance lost
        mRenderer.setOptimizeTransformDrawing(true);
        
        //绑定surfaceView 和 renderer， 初始化完成
        //setup and it will initialize. every thing is ready.
        ViewGestureHelper.bindView(surfaceView, mRenderer);
        
        //可选，添加回调
        //optionally set callback
        mRenderer.setOPdfCallback(new OPdfCallbackImpl());
        
It is an single PDF page viewer implementation base on SurfaceView.
Free scale and translate is supported.
Easy to use and show complicated PDF very well.