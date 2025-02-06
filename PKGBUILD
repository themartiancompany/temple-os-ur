# SPDX-License-Identifier: AGPL-3.0

#    ----------------------------------------------------------------------
#    Copyright © 2025  Pellegrino Prevete
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

# Maintainer: Truocolo <truocolo@aol.com>
# Maintainer: Pellegrino Prevete (tallero) <pellegrinoprevete@gmail.com>

# shellcheck disable=SC2034
_archive="true"
evmfs="false"
_pkg="windows-xp"
_variant="starter-edition"
_pkgbase="${_pkg}-${_variant}"
pkgname=(
  "${_pkgbase}"
)
pkgver="5.1.2600.7208"
pkgrel=1
pkgdesc="Operating system by Microsoft Corporation."
arch=(
  'any'
)
license=(
  'EULA'
)
url="https://web.archive.org/web/20030621141136/http://www.microsoft.com:80/italy/windowsxp/default.asp"
provides=(
  "${_pkg}"
)
makedepends=(
)
checkdepends=(
)
_archive_http="https://archive.org/download"
_ns="windowsxpstarter_limboqemu"
_zip_filename="Windows%20XP%20Starter.zip"
_zip_sum="3bf68530f8473b961410ca8fc0a1649487362f6bf4c9c972821af852f8551f39"
if [[ "${_archive}" == "true" ]]; then
  _src="${pkgname}-${pkgver}.zip::${_archive_http}/${_ns}/${_zip_filename}"
elif [[ "${_evmfs}" == "true" ]]; then
  echo \
    "S O O N"
fi
source=(
  "${_src}"
)
sha256sums=(
  "${_zip_sum}"
)

# shellcheck disable=SC2154
package() {
  install \
    -vdm755 \
    "${pkgdir}/var/lib/libvirt/images"
  mv \
    "${srcdir}/Windows XP Starter Edition.qcow2" \
    "${pkgdir}/var/lib/libvirt/images"
}
