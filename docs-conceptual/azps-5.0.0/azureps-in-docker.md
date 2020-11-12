---
title: Docker’da Azure PowerShell kullanma
description: Bir Docker görüntüsündeki önceden yüklenmiş Azure PowerShell’i kullanma.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/20/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 48935f15241ec965adf4c34d2c17aa670110585a
ms.sourcegitcommit: 2036538797dd088728aee5ac5021472454d82eb2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/06/2020
ms.locfileid: "93407740"
---
# <a name="using-azure-powershell-in-docker"></a>Docker’da Azure PowerShell kullanma

Azure PowerShell’in önceden yüklenmiş olduğu Docker görüntülerini yayımlıyoruz. Bu makale, Docker kapsayıcısında Azure PowerShell’i kullanmaya başlamayı gösterir.

## <a name="finding-available-images"></a>Kullanılabilir görüntüleri bulma

Yayınlanan görüntüler Docker 17.05 veya üstünü gerektirir. Docker’ı `sudo` veya yerel yönetici hakları olmadan çalıştırabilecek durumda olmanız beklenir. `docker` yüklemesini doğru bir şekilde gerçekleştirmek için Docker’ın resmi [yönergelerini][install] izleyin.

En son kapsayıcı görüntüsü, Az modülüyle desteklenen PowerShell ve Azure PowerShell modüllerinin en son sürümünü içerir.

Az modülünün her yeni sürümü için şu işletim sistemlerine yönelik bir görüntüyü kullanıma sunuyoruz:

- Ubuntu 18.04 (varsayılan)
- Debian 9
- CentOs 7

Sunulan görüntülerin tam listesine [Docker görüntüsü][az image] sayfamızdan erişebilirsiniz.

## <a name="using-azure-powershell-in-a-container"></a>Azure PowerShell’i bir kapsayıcıda kullanma

Aşağıdaki komutlar, görüntüyü indirip etkileşimli bir PowerShell oturumu başlatmak için gereken Docker komutlarını gösterir.

1. En güncel azure-powershell görüntüsünü indirin.

   ```console
   docker pull mcr.microsoft.com/azure-powershell
   ```

1. azure-powershell kapsayıcısını etkileşimli modda çalıştırın:

   ```console
   docker run -it mcr.microsoft.com/azure-powershell pwsh
   ```

Windows üzerindeki yerel sürücülerin Linux kapsayıcılarıyla paylaşılmasını sağlamak için Windows Docker konaklarında Docker File Sharing’i etkinleştirmeniz gerekir. Daha fazla bilgi için bkz. [Docker for Windows’u kullanmaya başlayın][file-sharing].

### <a name="run-the-azure-powershell-container-interactively-using-host-authentication"></a>Ana bilgisayar kimlik doğrulaması kullanarak azure-powershell kapsayıcısını etkileşimli olarak çalıştırın

Docker’ı barındıran sisteme Azure PowerShell’i önceden yüklediyseniz, Azure kimlik bilgileriniz önbelleğe alınmış olabilir. Bu kimlik bilgileri Docker kapsayıcısında çalışan PowerShell oturumunda kullanılabilir.

Varsayılan olarak önbelleğe alınan kimlik bilgileri, ana bilgisayarınızdaki `$HOME/.Azure` dizininde bulunur. Kimlik bilgilerine erişmek için Docker hizmetinin bu konuma erişebilmesi gerekir. Aşağıdaki komut, kapsayıcıyı kimlik bilgisi önbelleği bağlı şekilde çalıştırır ve etkileşimli bir PowerShell oturumu başlatır.

```console
docker run -it -v ~/.Azure/AzureRmContext.json:/root/.Azure/AzureRmContext.json -v ~/.Azure/TokenCache.dat:/root/.Azure/TokenCache.dat mcr.microsoft.com/azure-powershell pwsh
```

### <a name="remove-the-image-when-no-longer-needed"></a>Artık gerekmediğinde görüntüyü kaldırın

Aşağıdaki komut, Docker kapsayıcısına ihtiyacınız kalmadığında bunu silmek için kullanılır.

```console
docker rmi mcr.microsoft.com/azure-powershell
```

## <a name="next-steps"></a>Sonraki adımlar

Azure PowerShell modülleri ve bunların özellikleri hakkında daha fazla bilgi edinmek için bkz. [Azure PowerShell’i Kullanmaya Başlama](get-started-azureps.md).

<!-- link references -->
[install]: https://docs.docker.com/engine/installation/
[powershell image]: https://hub.docker.com/_/microsoft-powershell
[az image]: https://hub.docker.com/_/microsoft-azure-powershell
[file-sharing]: https://docs.docker.com/docker-for-windows/#file-sharing
