---
title: Azure PowerShell’e Genel Bakış
description: Azure PowerShell Az modülünü yükleme ve kullanmaya başlama hakkında bilgiler içeren genel bir bakış.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.manager: carmonm
ms.date: 01/10/2019
ms.openlocfilehash: 45ab083dd133c8c7b8dbe902484c92564bc216b9
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63068821"
---
# <a name="overview-of-azure-powershell"></a>Azure PowerShell’e Genel Bakış

Azure PowerShell, Azure kaynaklarınızı yönetmek için [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) modelini kullanan bir dizi cmdlet sunar. Azure PowerShell'in .NET Standard’ı kullanması Windows, macOS ve Linux’ta kullanılabilmesini sağlar.
Azure PowerShell, Azure Cloud Shell üzerinde de kullanılabilir.

## <a name="about-the-new-az-module"></a>Yeni Az modülü hakkında

Bu belgede, Azure PowerShell’e yönelik yeni Az modülü açıklanır. Bu yeni modül, en baştan itibaren .NET Standard platformunda yazılmıştır. .NET Standard’ın kullanılması, Azure PowerShell’in Windows’da PowerShell 5 veya diğer tüm platformlarda PowerShell 6 altında çalışmasına olanak tanır. Artık PowerShell üzerinden Azure ile etkileşim kurmak için kullanılması hedeflenen yöntem Az modülüdür.
AzureRM için hata düzeltmeleri sağlanmaya devam edilecek olsa da artık yeni özellikler sağlanmayacaktır.

[Azure PowerShell Az modülüne giriş](new-azureps-module-az.md) makalesini okuyarak komutların nasıl yeniden adlandırıldığı ve AzureRM’ye yönelik bakım planları dahil olmak üzere yeni modülle ilgili tüm ayrıntıları öğrenin. Yeni modülü hemen kullanmaya başlamak istiyorsanız bkz. [AzureRM’den Az’ye geçiş](migrate-from-azurerm-to-az.md).

[AzureRM belgeleri](/powershell/azure/azurerm) de sağlanır.

> [!IMPORTANT]
>
> Azure belgelerinin yeni modüldeki cmdlet adlarını yansıtacak şekilde güncelleştirilmesi sürerken makalelerde AzureRM komutları kullanılmaya devam edilebilir. Az modülünü yükledikten sonra `Enable-AzureRmAlias` ile AzureRM cmdlet'i diğer adlarını etkinleştirmeniz önerilir. Daha ayrıntılı bilgi edinmek için [AzureRM’den Az’ye geçiş](migrate-from-azurerm-to-az.md) makalesine bakın.

## <a name="run-or-install"></a>Çalıştırma veya yükleme

Azure PowerShell’i, Windows’da PowerShell 5.1 veya sonraki sürümlerine, diğer platformlarda PowerShell 6’ya yükleyebilir veya Azure Cloud Shell’de çalıştırabilirsiniz.

* Tarayıcınızda Azure Cloud Shell ile çalıştırmak için bkz. [Azure Cloud Shell'de PowerShell için Hızlı Başlangıç](/azure/cloud-shell/quickstart-powershell).
* Azure PowerShell'i sisteminize yüklemek için bkz. [Azure PowerShell'i yükleme](install-az-ps.md).

En son Azure PowerShell sürümü hakkında bilgi edinmek için [sürüm notlarına](release-notes-azureps.md) bakın.

## <a name="get-started"></a>Başlarken

Azure PowerShell ile ilgili temel kavramları öğrenmek için [Azure PowerShell'i Kullanmaya Başlama](get-started-azureps.md) makalesini gözden geçirin. PowerShell'i tanımıyorsanız, bir tanıtımı incelemeniz yararlı olabilir:

* [PowerShell yükleme](/powershell/scripting/install/installing-powershell)
* [PowerShell ile betik oluşturma](/powershell/scripting/powershell-scripting)
* [PowerShell Temel Bilgileri: (Bölüm 1) PowerShell'i Kullanmaya Başlama](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1)
* Microsoft Virtual Academy'de [PowerShell Jumpstart’ı Kullanmaya Başlama](https://mva.microsoft.com/liveevents/powershell-jumpstart)

Aşağıdaki örnekler Azure'ın bazı yaygın kullanımları konusunda yardımcı olabilir:

* [Linux Sanal Makineleri](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=/powershell/azure/toc.json)
* [Windows Sanal Makineleri](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=/powershell/azure/toc.json)
* [Web Apps](/azure/app-service-web/app-service-powershell-samples?toc=/powershell/azure/toc.json)
* [SQL Veritabanları](/azure/sql-database/sql-database-powershell-samples?toc=/powershell/azure/toc.json)

## <a name="build-your-skills-with-microsoft-learn"></a>Microsoft Learn ile becerilerinizi geliştirin

- [PowerShell betiklerini kullanarak Azure görevlerini otomatikleştirme](/learn/modules/automate-azure-tasks-with-powershell/)
- [Daha fazla etkileşimli öğrenme içeriği...](/learn/browse/?term=powershell)

## <a name="other-azure-powershell-modules"></a>Diğer Azure PowerShell modülleri

* [Azure Active Directory](/powershell/azure/active-directory/)
* [Azure Service Fabric](/powershell/azure/service-fabric/)
* [Azure Elastik DB](/powershell/azure/elasticdbjobs/)
