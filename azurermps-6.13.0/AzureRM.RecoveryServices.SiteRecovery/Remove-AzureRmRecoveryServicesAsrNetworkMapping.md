---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: 56c188b6b6e902fffa9cd777d6a5acf3b38cb2fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588399"
---
# <span data-ttu-id="407f2-101">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="407f2-101">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="407f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="407f2-102">SYNOPSIS</span></span>
<span data-ttu-id="407f2-103">Belirtilen ASR Ağ eşlemesini kurtarma hizmetleri kasasından siler.</span><span class="sxs-lookup"><span data-stu-id="407f2-103">Deletes the specified ASR network mapping from the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="407f2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="407f2-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="407f2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="407f2-105">DESCRIPTION</span></span>
<span data-ttu-id="407f2-106">**Remove-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet 'ı belirtilen ASR Ağ eşlemesini siler.</span><span class="sxs-lookup"><span data-stu-id="407f2-106">The **Remove-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet deletes the specified ASR network mapping.</span></span>

## <span data-ttu-id="407f2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="407f2-107">EXAMPLES</span></span>

### <span data-ttu-id="407f2-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="407f2-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrNetworkMapping -NetworkMapping $networkmapping
```

<span data-ttu-id="407f2-109">Belirtilen ASR ağ eşlemesinin silinmesini başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="407f2-109">Starts the deletion of specified ASR network mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="407f2-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="407f2-110">PARAMETERS</span></span>

### <span data-ttu-id="407f2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="407f2-111">-DefaultProfile</span></span>
<span data-ttu-id="407f2-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="407f2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="407f2-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="407f2-113">-InputObject</span></span>
<span data-ttu-id="407f2-114">Cmdlet 'e giriş nesnesi: ASR ağ eşlemesine yönelik ASR ağ eşleme nesnesi silinecek.</span><span class="sxs-lookup"><span data-stu-id="407f2-114">The input object to the cmdlet: The ASR network mapping object corresponding to the ASR network mapping to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping
Parameter Sets: (All)
Aliases: NetworkMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="407f2-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="407f2-115">-Confirm</span></span>
<span data-ttu-id="407f2-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="407f2-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="407f2-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="407f2-117">-WhatIf</span></span>
<span data-ttu-id="407f2-118">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="407f2-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="407f2-119">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="407f2-119">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="407f2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="407f2-120">CommonParameters</span></span>
<span data-ttu-id="407f2-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="407f2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="407f2-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="407f2-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="407f2-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="407f2-123">INPUTS</span></span>

### <span data-ttu-id="407f2-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="407f2-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="407f2-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="407f2-125">OUTPUTS</span></span>

### <span data-ttu-id="407f2-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="407f2-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="407f2-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="407f2-127">NOTES</span></span>

## <span data-ttu-id="407f2-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="407f2-128">RELATED LINKS</span></span>

[<span data-ttu-id="407f2-129">Get-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="407f2-129">Get-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./Get-AzureRmRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="407f2-130">New-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="407f2-130">New-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./New-AzureRmRecoveryServicesAsrNetworkMapping.md)
