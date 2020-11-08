---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProperty.md
ms.openlocfilehash: efe463bab4195dfb09692f76d0e02e3aeaa59344
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096362"
---
# <span data-ttu-id="2a197-101">Get-AzRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="2a197-101">Get-AzRecoveryServicesBackupProperty</span></span>

## <span data-ttu-id="2a197-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a197-102">SYNOPSIS</span></span>
<span data-ttu-id="2a197-103">Yedekleme özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="2a197-103">Gets Backup properties.</span></span>

## <span data-ttu-id="2a197-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2a197-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupProperty -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2a197-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2a197-105">DESCRIPTION</span></span>
<span data-ttu-id="2a197-106">**Get-AzRecoveryServicesBackupProperty** cmdlet 'ı, kurtarma hizmetleri Kasası için yedekleme özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="2a197-106">The **Get-AzRecoveryServicesBackupProperty** cmdlet gets backup properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="2a197-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2a197-107">EXAMPLES</span></span>

### <span data-ttu-id="2a197-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2a197-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesBackupProperty -Vault $vault
```

<span data-ttu-id="2a197-109">Kasa için yedek kasa özelliğini edinin.</span><span class="sxs-lookup"><span data-stu-id="2a197-109">Get the backup vault property for vault.</span></span>

## <span data-ttu-id="2a197-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2a197-110">PARAMETERS</span></span>

### <span data-ttu-id="2a197-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a197-111">-DefaultProfile</span></span>
<span data-ttu-id="2a197-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2a197-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a197-113">-Kasa</span><span class="sxs-lookup"><span data-stu-id="2a197-113">-Vault</span></span>
<span data-ttu-id="2a197-114">Kasanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a197-114">Specifies the name of the vault.</span></span>
<span data-ttu-id="2a197-115">Kasa bir **Azurermrecoveryserviceskasa** nesnesi olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="2a197-115">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2a197-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a197-116">CommonParameters</span></span>
<span data-ttu-id="2a197-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2a197-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a197-118">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2a197-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a197-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2a197-119">INPUTS</span></span>

### <span data-ttu-id="2a197-120">Microsoft. Azure. Commands. RecoveryServices. Arskasa</span><span class="sxs-lookup"><span data-stu-id="2a197-120">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="2a197-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2a197-121">OUTPUTS</span></span>

### <span data-ttu-id="2a197-122">Microsoft. Azure. Commands. RecoveryServices. ASRVaultBackupProperties</span><span class="sxs-lookup"><span data-stu-id="2a197-122">Microsoft.Azure.Commands.RecoveryServices.ASRVaultBackupProperties</span></span>

## <span data-ttu-id="2a197-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2a197-123">NOTES</span></span>

## <span data-ttu-id="2a197-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2a197-124">RELATED LINKS</span></span>
