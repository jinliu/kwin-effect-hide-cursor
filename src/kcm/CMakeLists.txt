set(kwin_hidecursor_config_SOURCES hidecursor_config.cpp)
ki18n_wrap_ui(kwin_hidecursor_config_SOURCES hidecursor_config.ui)
qt_add_dbus_interface(kwin_hidecursor_config_SOURCES ${KWIN_EFFECTS_INTERFACE} kwineffects_interface)

kcoreaddons_add_plugin(kwin_hidecursor_config INSTALL_NAMESPACE "kwin/effects/configs" SOURCES ${kwin_hidecursor_config_SOURCES})
kconfig_add_kcfg_files(kwin_hidecursor_config ../hidecursorconfig.kcfgc)
target_link_libraries(kwin_hidecursor_config
    KF6::ConfigCore
    KF6::ConfigGui
    KF6::ConfigWidgets
    KF6::CoreAddons
    KF6::I18n
    KF6::KCMUtils
    KF6::XmlGui

    KWin::kwin
)