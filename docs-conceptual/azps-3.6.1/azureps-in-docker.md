---
title: Docker’da Azure PowerShell kullanma
description: Bir Docker görüntüsündeki önceden yüklenmiş Azure PowerShell’i kullanma.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.openlocfilehash: a5746b71cfc41f7c6283b0e95b0940ca4b594ec7
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2020
ms.locfileid: "79402689"
---
# <a name="using-azure-powershell-in-docker"></a>Docker’da Azure PowerShell kullanma

Azure PowerShell’in önceden yüklenmiş olduğu Docker görüntülerini yayımlıyoruz. Bu makale, Docker kapsayıcısında Azure PowerShell’i kullanmaya başlamayı gösterir.

## <a name="finding-available-images"></a>Kullanılabilir görüntüleri bulma

Yayınlanan görüntüler Docker 17.05 veya üstünü gerektirir. Docker’ı `sudo` veya yerel yönetici hakları olmadan çalıştırabilecek durumda olmanız beklenir. `docker` yüklemesini doğru bir şekilde gerçekleştirmek için Docker’ın resmi [yönergelerini][install] izleyin.

Yayınlanan kapsayıcılar resmi PowerShell kapsayıcılarından oluşturulur ve Az modülü bunlara katman olarak eklenir.

En son kararlı görüntü şunları içerir:

- Ubuntu 18.04
- PowerShell 6.2.4 sürümü
- Azure PowerShell en güncel Az modülü

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