add_subdirectory(kcm)

kcoreaddons_add_plugin(hidecursor INSTALL_NAMESPACE "kwin/effects/plugins/")
target_sources(hidecursor PRIVATE
    hidecursor.cpp
    main.cpp
)
kconfig_add_kcfg_files(hidecursor hidecursorconfig.kcfgc)

target_link_libraries(hidecursor
    KF6::ConfigCore
    KF6::ConfigGui
    KF6::CoreAddons
    KF6::I18n
    
    KWin::kwin
)
