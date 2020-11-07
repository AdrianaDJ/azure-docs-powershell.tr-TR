---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Import-AzureRmRecoveryServicesAsrVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Import-AzureRmRecoveryServicesAsrVaultSettingsFile.md
ms.openlocfilehash: ad22cbe1cb17e69358ef386b478fe929abe415b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762425"
---
# <span data-ttu-id="5ce4b-101">Import-AzureRmRecoveryServicesAsrVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="5ce4b-101">Import-AzureRmRecoveryServicesAsrVaultSettingsFile</span></span>

## <span data-ttu-id="5ce4b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ce4b-102">SYNOPSIS</span></span>
<span data-ttu-id="5ce4b-103">PowerShell oturumunda sonraki ASR işlemleri için kasa bağlamını (PowerShell oturum bağlamı) ayarlamak üzere belirtilen ASR kasa ayarları dosyasını içeri aktarır.</span><span class="sxs-lookup"><span data-stu-id="5ce4b-103">Imports the specified ASR vault settings file to set the vault context(PowerShell session context) for subsequent ASR operations in the PowerShell session.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ce4b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5ce4b-104">SYNTAX</span></span>

```
Import-AzureRmRecoveryServicesAsrVaultSettingsFile [-Path] <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ce4b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5ce4b-105">DESCRIPTION</span></span>
<span data-ttu-id="5ce4b-106">**Import-Azurermrecoveryservicesasrvaultsettingsfıle** cmdlet 'ı, Azure Site Recovery kasa ayarları dosyasını içeri aktarır.</span><span class="sxs-lookup"><span data-stu-id="5ce4b-106">The **Import-AzureRmRecoveryServicesAsrVaultSettingsFile** cmdlet imports the Azure Site Recovery vault settings file.</span></span> <span data-ttu-id="5ce4b-107">Kasa ayarları dosyası, geçerli oturumdaki sonraki Azure Site kurtarma işlemleri için kasa bağlamını ayarlamak üzere kullanılır.</span><span class="sxs-lookup"><span data-stu-id="5ce4b-107">The vault settings file is used to set the vault context for subsequent Azure Site Recovery operations in the current session.</span></span>

## <span data-ttu-id="5ce4b-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5ce4b-108">EXAMPLES</span></span>

### <span data-ttu-id="5ce4b-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5ce4b-109">Example 1</span></span>
```
PS C:\> $VaultSettings = Import-AzureRmRecoveryServicesAsrVaultSettingsFile -Path $FilePath
```

<span data-ttu-id="5ce4b-110">Belirtilen kurtarma hizmetleri Kasası ayarları dosyasını içeri aktarır ve içeri aktarılan kasanın ayarlarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="5ce4b-110">Imports the specified Recovery Services vault settings file and returns settings of the imported vault.</span></span>

## <span data-ttu-id="5ce4b-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5ce4b-111">PARAMETERS</span></span>

### <span data-ttu-id="5ce4b-112">-Yol</span><span class="sxs-lookup"><span data-stu-id="5ce4b-112">-Path</span></span>
<span data-ttu-id="5ce4b-113">ASR kasa ayarları dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="5ce4b-113">Specifies the path of the ASR vault settings file.</span></span>
<span data-ttu-id="5ce4b-114">Bu dosya, Kurtarma Hizmetleri kasa portalından indirilebilir ve yerel olarak depolanabilir.</span><span class="sxs-lookup"><span data-stu-id="5ce4b-114">This file can be downloaded from the Recovery Services vault portal and stored locally.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ce4b-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="5ce4b-115">-Confirm</span></span>
<span data-ttu-id="5ce4b-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5ce4b-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ce4b-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ce4b-117">-WhatIf</span></span>
<span data-ttu-id="5ce4b-118">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5ce4b-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5ce4b-119">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5ce4b-119">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ce4b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ce4b-120">CommonParameters</span></span>
<span data-ttu-id="5ce4b-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5ce4b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ce4b-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ce4b-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ce4b-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5ce4b-123">INPUTS</span></span>

### <span data-ttu-id="5ce4b-124">System. String</span><span class="sxs-lookup"><span data-stu-id="5ce4b-124">System.String</span></span>

## <span data-ttu-id="5ce4b-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5ce4b-125">OUTPUTS</span></span>

### <span data-ttu-id="5ce4b-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="5ce4b-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="5ce4b-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5ce4b-127">NOTES</span></span>

## <span data-ttu-id="5ce4b-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5ce4b-128">RELATED LINKS</span></span>

[<span data-ttu-id="5ce4b-129">Get-AzureRmRecoveryServicesAsrVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="5ce4b-129">Get-AzureRmRecoveryServicesAsrVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesAsrVaultSettingsFile.md)
