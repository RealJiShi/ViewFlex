# plugins

----------

Plugins root folder, implements Qt-plugin under this folder.

- viewer plugins


###Design format

One plugin should open only once by GUI, but one plugin is able to maintain many instances. Plugin is implemented as interface here, such as:

    class ViewerInterface : public QObject,
            public infra::mainframe::PluginInterface,
            public gui::api::Viewer {}

`infra::mainframe::PluginInterface` is a base class of interface and `gui::api::Viewer` is a base class of api interface.

