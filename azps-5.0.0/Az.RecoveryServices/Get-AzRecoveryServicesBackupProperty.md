---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProperty.md
ms.openlocfilehash: efe463bab4195dfb09692f76d0e02e3aeaa59344
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323047"
---
# <span data-ttu-id="a762a-101">Get-AzRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="a762a-101">Get-AzRecoveryServicesBackupProperty</span></span>

## <span data-ttu-id="a762a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a762a-102">SYNOPSIS</span></span>
<span data-ttu-id="a762a-103">Yedekleme özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="a762a-103">Gets Backup properties.</span></span>

## <span data-ttu-id="a762a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a762a-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupProperty -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a762a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a762a-105">DESCRIPTION</span></span>
<span data-ttu-id="a762a-106">**Get-AzRecoveryServicesBackupProperty** cmdlet 'ı, kurtarma hizmetleri Kasası için yedekleme özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="a762a-106">The **Get-AzRecoveryServicesBackupProperty** cmdlet gets backup properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="a762a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a762a-107">EXAMPLES</span></span>

### <span data-ttu-id="a762a-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a762a-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesBackupProperty -Vault $vault
```

<span data-ttu-id="a762a-109">Kasa için yedek kasa özelliğini edinin.</span><span class="sxs-lookup"><span data-stu-id="a762a-109">Get the backup vault property for vault.</span></span>

## <span data-ttu-id="a762a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a762a-110">PARAMETERS</span></span>

### <span data-ttu-id="a762a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a762a-111">-DefaultProfile</span></span>
<span data-ttu-id="a762a-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a762a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a762a-113">-Kasa</span><span class="sxs-lookup"><span data-stu-id="a762a-113">-Vault</span></span>
<span data-ttu-id="a762a-114">Kasanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a762a-114">Specifies the name of the vault.</span></span>
<span data-ttu-id="a762a-115">Kasa bir **Azurermrecoveryserviceskasa** nesnesi olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="a762a-115">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="a762a-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a762a-116">CommonParameters</span></span>
<span data-ttu-id="a762a-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a762a-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a762a-118">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a762a-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a762a-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a762a-119">INPUTS</span></span>

### <span data-ttu-id="a762a-120">Microsoft. Azure. Commands. RecoveryServices. Arskasa</span><span class="sxs-lookup"><span data-stu-id="a762a-120">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="a762a-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a762a-121">OUTPUTS</span></span>

### <span data-ttu-id="a762a-122">Microsoft. Azure. Commands. RecoveryServices. ASRVaultBackupProperties</span><span class="sxs-lookup"><span data-stu-id="a762a-122">Microsoft.Azure.Commands.RecoveryServices.ASRVaultBackupProperties</span></span>

## <span data-ttu-id="a762a-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a762a-123">NOTES</span></span>

## <span data-ttu-id="a762a-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a762a-124">RELATED LINKS</span></span>
