unit_files = [
    ['adc', 'xyz.openbmc_project.adcsensor.service'],
    ['cpu', 'xyz.openbmc_project.cpusensor.service'],
    ['exit-air', 'xyz.openbmc_project.exitairsensor.service'],
    ['fan', 'xyz.openbmc_project.fansensor.service'],
    ['hwmon-temp', 'xyz.openbmc_project.hwmontempsensor.service'],
    ['ipmb', 'xyz.openbmc_project.ipmbsensor.service'],
    ['intrusion', 'xyz.openbmc_project.intrusionsensor.service'],
    ['mcu-temp', 'xyz.openbmc_project.mcutempsensor.service'],
    ['nvme', 'xyz.openbmc_project.nvmesensor.service'],
    ['psu-temp', 'xyz.openbmc_project.psusensor.service'],
]

foreach tuple : unit_files
    if get_option(tuple[0]).enabled()
        configure_file(
            copy: true,
            input: tuple[1],
            install: true,
            install_dir: systemd_system_unit_dir,
            output: tuple[1],
        )
    endif


endforeach
