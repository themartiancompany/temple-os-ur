# SPDX-License-Identifier: AGPL-3.0

#    ----------------------------------------------------------------------
#    Copyright © 2022, 2023, 2024, 2025, 2026  Pellegrino Prevete
#
#    All rights reserved
#    ----------------------------------------------------------------------
#
#    This program is free software: you can redistribute it and/or modify
#    it under the terms of the GNU Affero General Public License as published by
#    the Free Software Foundation, either version 3 of the License, or
#    (at your option) any later version.
#
#    This program is distributed in the hope that it will be useful,
#    but WITHOUT ANY WARRANTY; without even the implied warranty of
#    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
#    GNU Affero General Public License for more details.
#
#    You should have received a copy of the GNU Affero General Public License
#    along with this program.  If not, see <https://www.gnu.org/licenses/>.

# Maintainers:
#   Truocolo
#     <truocolo@aol.com>
#     <truocolo@0x6E5163fC4BFc1511Dbe06bB605cc14a3e462332b>
#   Pellegrino Prevete (dvorak)
#     <pellegrinoprevete@gmail.com>
#     <dvorak@0x87003Bd6C074C713783df04f36517451fF34CBEf>

# shellcheck disable=SC2034
_archive="true"
evmfs="false"
_pkg=temple-os
_pkgbase="${_pkg}"
pkgname=(
  "${_pkgbase}"
)
pkgver="1.0-terry"
pkgrel=1
_pkgdesc=(
  "Operating system written Terry A. Davis."
)
arch=(
  'any'
)
license=(
  'CC0'
)
url="https://templeos.org"
provides=(
  "j-operating-system"
  "j-os"
  "lose-thos"
  "sparrow-os"
)
makedepends=(
)
checkdepends=(
)
_tarname="${_pkg}-${pkgver}"
_tarfile="${_tarname}.tar.xz"
_sum="aff80f250eeb19cbc191a3434caab268d0e660c43a2989c3bf9544eb25fe5ba8"
_sig_sum="258ce911bb8f69386a8f59318b92be30f86d00f3663387764e196d6f82bf3050"
_namespace="0x5179A7Ff1E17688489152689a01640c42550A9F2"
_net="100"
_fs="0x69470b18f8b8b5f92b48f6199dcb147b4be96571"
_dir="evmfs://${_net}/${_fs}/${_namespace}"
_uri="${_dir}/${_sum}"
_sig_uri="${_dir}/${_sig_sum}"
source=(
  "${_tarfile}::${_uri}"
  "${_tarfile}.sig::${_sig_uri}"
)
sha256sums=(
  "${_sum}"
  "${_sig_sum}"
)

# shellcheck disable=SC2154
package() {
  install \
    -vdm755 \
    "${pkgdir}/usr/share/images"
  mv \
    "${srcdir}/TempleOS.ISO" \
    "${pkgdir}/usr/share/images/${_tarname}.iso"
}
