add_subdirectory(kcm)

kcoreaddons_add_plugin(hidecursor INSTALL_NAMESPACE "kwin/effects/plugins/")
target_sources(hidecursor PRIVATE
    hidecursor.cpp
    main.cpp
)
kconfig_add_kcfg_files(hidecursor hidecursorconfig.kcfgc)

target_link_libraries(hidecursor
    KF5::ConfigCore
    KF5::ConfigGui
    KF5::CoreAddons
    KF5::I18n
    kwineffects::kwineffects
    kwineffects::kwinglutils
    epoxy::epoxy
)
