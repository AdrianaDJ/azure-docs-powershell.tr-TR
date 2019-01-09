---
title: Azure PowerShell’e Genel Bakış
description: Azure PowerShell Az modülünü yükleme ve kullanmaya başlama hakkında bilgiler içeren genel bir bakış.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.manager: carmonm
ms.date: 10/29/2018
ms.openlocfilehash: 7982e122d49db4d558648231d1ab8bfeed80be2d
ms.sourcegitcommit: 4acddc7026522c4fe39de2c4424917d88ee01b7e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/21/2018
ms.locfileid: "53736469"
---
# <a name="overview-of-azure-powershell"></a>Azure PowerShell’e Genel Bakış

Azure PowerShell, Azure kaynaklarınızı yönetmek için [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) modelini kullanan bir dizi cmdlet sunar. Azure PowerShell .NET Standard’ı kullandığından, Windows, macOS ve Linux’ta kullanılabilir.
Azure PowerShell, Azure Cloud Shell’den de kullanılabilir.

[Azure Cloud Shell](/azure/cloud-shell/overview)’i kullanarak Azure PowerShell’i tarayıcınızda çalıştırın veya [yerel olarak yükleyin](install-az-ps.md). Azure PowerShell ile ilgili temel kavramları öğrenmek ve Azure’ı kullanmaya başlamak için [Kullanmaya Başlama](get-started-azureps.md) makalesine göz atın.

En son Azure PowerShell sürümü hakkında bilgi edinmek için [sürüm notlarına](release-notes-azureps.md) bakın.

## <a name="about-the-new-az-module"></a>Yeni Az modülü hakkında

Bu belgede, Azure PowerShell’e yönelik yeni Az modülü açıklanır. Bu yeni modül, en baştan itibaren .NET Standard platformunda yazılmıştır. .NET Standard’ın kullanılması, Azure PowerShell’in Windows’da PowerShell 5.x veya diğer tüm platformlarda PowerShell 6 altında çalışmasına olanak tanır. Artık PowerShell üzerinden Azure ile etkileşim kurmak için kullanılması hedeflenen yöntem Az modülüdür.
AzureRM için hata düzeltmeleri sağlanmaya devam edilecek olsa da artık yeni özellikler sağlanmayacaktır.

[Azure PowerShell Az modülüne giriş](new-azureps-module-az.md) makalesini okuyarak komutların nasıl yeniden adlandırıldığı ve AzureRM’ye yönelik bakım planları dahil olmak üzere yeni modülle ilgili tüm ayrıntıları öğrenin. Yeni modülü hemen kullanmaya başlamak istiyorsanız bkz. [AzureRM’den Az’ye geçiş](migrate-from-azurerm-to-az.md).

[AzureRM belgeleri](/powershell/azure/azurerm) de sağlanır.

> [!IMPORTANT]
>
> Azure belgelerini yeni modüldeki cmdlet adlarını yansıtacak şekilde güncelleştirme çalışmaları sırasında makalelerde AzureRM komutları kullanılmaya devam edilebilir. Az modülünü yükledikten sonra `Enable-AzureRmAlias` ile AzureRM cmdlet'i diğer adlarını etkinleştirmeniz önerilir. Daha ayrıntılı bilgi edinmek için [AzureRM’den Az’ye geçiş](migrate-from-azurerm-to-az.md) makalesine bakın.

## <a name="common-scenarios"></a>Genel senaryolar

Aşağıdaki örnekler, yaygın senaryoları Azure PowerShell ile nasıl gerçekleştireceğinizi öğrenmenize yardımcı olabilir:

* [Linux Sanal Makineleri](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=/powershell/azure/toc.json)
* [Windows Sanal Makineleri](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=/powershell/azure/toc.json)
* [Web Apps](/azure/app-service-web/app-service-powershell-samples?toc=/powershell/azure/toc.json)
* [SQL Veritabanları](/azure/sql-database/sql-database-powershell-samples?toc=/powershell/azure/toc.json)

## <a name="learn-powershell-basics"></a>PowerShell temel bilgilerini öğrenme

PowerShell'i tanımıyorsanız bir tanıtımı incelemeniz yararlı olabilir.

* [PowerShell’i yükleme](/powershell/scripting/setup/installing-windows-powershell)
* [PowerShell ile betik oluşturma](/powershell/scripting/powershell-scripting)

Ayrıca şu videoyu izleyebilirsiniz: [PowerShell Temel Bilgileri: (Bölüm 1) PowerShell'i Kullanmaya Başlama](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1).

Dilerseniz Microsoft Sanal Akademi’nin [PowerShell Jumpstart’ı Kullanmaya Başlama](https://mva.microsoft.com/liveevents/powershell-jumpstart) etkinliğine de katılabilirsiniz.

## <a name="build-your-skills-with-microsoft-learn"></a>Microsoft Learn ile becerilerinizi geliştirin

- [PowerShell betiklerini kullanarak Azure görevlerini otomatikleştirme](/learn/modules/automate-azure-tasks-with-powershell/)
- [Daha fazla etkileşimli öğrenme içeriği...](/learn/browse/?term=powershell)

## <a name="other-azure-powershell-modules"></a>Diğer Azure PowerShell modülleri

* [Azure Active Directory](/powershell/azure/active-directory/)
* [Azure Information Protection](/powershell/azure/aip/)
* [Azure Service Fabric](/powershell/azure/service-fabric/)
* [Azure Elastik DB](/powershell/azure/elasticdbjobs/)
