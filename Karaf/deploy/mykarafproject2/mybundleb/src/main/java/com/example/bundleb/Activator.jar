package com.example.bundleb;

import org.osgi.framework.BundleActivator;
import org.osgi.framework.BundleContext;
import org.osgi.framework.ServiceReference;
import com.example.bundlea.MyService;

public class Activator implements BundleActivator {

    private ServiceReference<MyService> myServiceRef;

    @Override
    public void start(BundleContext context) throws Exception {
        System.out.println("MyBundleB started.");
        myServiceRef = context.getServiceReference(MyService.class);
        MyService myService = context.getService(myServiceRef);
        System.out.println(myService.greet());
    }

    @Override
    public void stop(BundleContext context) throws Exception {
        System.out.println("MyBundleB stopped.");
        context.ungetService(myServiceRef);
    }
}