![NeoRixium](logos/Images/NeoLogo/NeoLogoLong.png)

**NeoRixium** is a lightweight, bloat-free Linux distro based on Arch, made for everyday use. The operating system's original name is **RixiumOS**. It is developed by **The NeoRixium Project**, often shortened to **Neo**.

## Built on Arch Linux™

NeoRixium runs on Arch Linux™ under the hood. Rolling release means your system stays up to date — no big version jumps and no reinstalls.

## What is nrx?

Arch Linux gives you pacman — a powerful tool for Arch packages. **nrx** is NeoRixium's own package manager front-end: a small command-line tool that sits on top of pacman and gives you a short, predictable set of commands.

nrx does not replace pacman, and it does not skip any of pacman's safety checks. It passes your request to pacman and returns pacman's result.

```
You type:  nrx install firefox
nrx runs:  sudo pacman -S --needed -- firefox
```

You can still use pacman directly at any time. nrx is a convenient option, not something you have to use.

### Available now (nrx v1, version 0.1.0)

```
nrx update               Upgrade the whole system
nrx upgrade              Same as update
nrx install <package>    Install a package
nrx remove <package>     Remove a package
nrx search <query>       Search for packages
nrx info <package>       Show package information
nrx help                 Show the command list
nrx version              Show the nrx version
```

- **Pacman does the work.** In v1, nrx works with pacman only. Package signature checks, dependency resolution, and pacman's confirmation prompts all stay on. nrx never adds options such as `--noconfirm` for you.
- **Administrator rights only when needed.** Run nrx as a normal user. It asks for administrator rights (through `sudo`) only for commands that change the system. `search`, `info`, `help`, and `version` never need them.
- **`update` and `upgrade` are the same.** Both run `pacman -Syu`: they refresh the package databases and upgrade the whole system in one step. Arch Linux does not support partial upgrades, so nrx never refreshes the databases without also upgrading.
- **`install` does not reinstall.** Packages that are already up to date are skipped.
- **`remove` is careful.** It removes only the packages you name. Pacman refuses if other packages still depend on them. nrx does not remove leftover dependencies automatically, and pacman keeps backup copies of configuration files you have changed.
- **Predictable input.** nrx v1 accepts plain package names only. Options and flags (for example `--noconfirm` or `--overwrite`) are rejected instead of being passed on to pacman. Version constraints such as `package>=1.0` are not supported yet.
- **Script-friendly.** nrx returns pacman's exit code. Wrong or missing arguments return exit code 2.

### Planned

The following ideas are development goals. They are **not** available yet.

- **More package systems.** Optional backends for other package formats, such as Debian/Ubuntu `.deb` packages, chosen with an option like `--apt`. Pacman will always remain the native backend.
- **Inspecting foreign packages.** Before installing a package from another system, nrx would show what it contains — its files, dependencies, and install scripts — and keep it separate from your native Arch system.
- **System updates through nrx.** Checking for new NeoRixium releases and showing what has changed. Checking, downloading, and installing would be separate steps, and nothing would be installed without your approval.

### Why it exists

The goal is not to hide Linux's complexity. It is to give everyday package tasks one simple, safe set of commands — today for pacman, and in the future for more package systems.

---

**NeoRixium** currently offers two desktop environment editions:

- ![Neodymium](logos/Images/NeoLogo/Neodymium.png) **Neodymium (XFCE)** – Fast and light, with essential apps and Firefox. It also works well on older hardware.
- ![Neosilicium](logos/Images/NeoLogo/Neosilicium.png) **Neosilicium (KDE Plasma)** – A customizable desktop with KDE's own app suite. It is not bloat-free by nature, but it has been trimmed down as much as possible.

Both editions run on the same Arch-based core. Different desktop, same system.

## These system builds are currently in development and not yet available.

---

# NeoRixium Terms and Conditions

Welcome to NeoRixium! By using, downloading, or sharing NeoRixium, you agree to these terms:

## 1. License

The NeoRixium **software** is licensed under the **GNU General Public License v3 (GPLv3)**. You may use, change, and share the software under the terms of this license.

The NeoRixium **name, logos, and images are not part of that license**. They are covered by Section 3 below and by the Trademark Policy.

## 2. Usage

- NeoRixium is provided **as is**. The developers are not responsible for damage, data loss, or other problems caused by using the software.
- You may make changes to NeoRixium or build your own distribution based on it.

## 3. Logos and Images

- NeoRixium logos and images are **not** licensed under the GPLv3. The rules in this section apply to them instead.
- You may use NeoRixium logos and images for **personal use**, such as wallpapers or decoration.
- You may not use NeoRixium logos, images, or branding for **commercial purposes** without permission.
- You may change the logos for personal, non-commercial projects.

## 4. No Warranty

NeoRixium comes without any warranty. The developer makes no promises about how well it works, its stability, or whether it will work with your hardware. Use it at your own risk.

## 5. Intellectual Property

- The NeoRixium name and logos belong to **The NeoRixium Project**.
- You may mention NeoRixium in non-commercial projects.

## 6. Updates and Support

- NeoRixium may provide updates and new ISO releases.
- Support comes from the community. Official technical support is not guaranteed.

## 7. Changes to These Terms

The NeoRixium Project may update these terms. If you continue to use NeoRixium, you accept the changes.

---

# NeoRixium Privacy Policy

Your privacy is important to The NeoRixium Project. This policy explains what information is collected and how it is used.

## 1. Information Collection

- The NeoRixium Project **does not directly collect personal data** through the NeoRixium operating system or its ISO downloads.
- You do not need to register or provide personal information to use NeoRixium or download ISOs.

## 2. Third-Party Services and Software

- NeoRixium may link to other services, such as GitHub, for downloads or contributions. These services may process data when you use them, and their privacy policies apply.
- NeoRixium includes software made by others, such as Firefox and the Arch Linux package servers it downloads from. Those services have their own privacy policies, which The NeoRixium Project does not control.

## 3. Your Rights

The NeoRixium Project does not directly collect personal data through the operating system or ISO downloads. Third-party services may process data under their own privacy policies. Please contact those services about data they process.

## 4. Changes to This Policy

This Privacy Policy may change over time. If you continue to use NeoRixium, you accept any updates.

---

# Trademark Policy

Last updated: 2026

## NeoRixium Name and Logo

- The NeoRixium name and logos belong to **The NeoRixium Project**. You may freely mention the NeoRixium name in non-commercial contexts. You may not use the name or logo to suggest official approval or support without permission.

## Arch Linux™

- NeoRixium is based on Arch Linux™. The Arch Linux name and logo are trademarks owned by Levente Polyák and Judd Vinet, on behalf of Arch Linux. NeoRixium is an independent project. It is not affiliated with, approved by, or sponsored by the Arch Linux project.
- The Arch Linux™ name is used here only to say that NeoRixium is based on Arch Linux, as described in the [Arch Linux Trademark Policy](https://terms.archlinux.org/docs/trademark-policy/). NeoRixium is not Arch Linux and is not called Arch Linux.

## Firefox

Firefox is a trademark of the Mozilla Foundation. NeoRixium includes Firefox as the default browser in its editions. This does not mean Mozilla is connected with or supports NeoRixium.

## KDE Plasma

KDE and the KDE logo are registered trademarks of KDE e.V. The NeoRixium Neosilicium edition is built on KDE Plasma. This does not mean KDE e.V. is connected with or supports NeoRixium.

## XFCE

XFCE is a trademark of its project. NeoRixium uses XFCE in its Neodymium edition, but this does not mean there is an official connection with the XFCE project.

## Other Trademarks

All other trademarks, product names, and company names mentioned here belong to their respective owners.
