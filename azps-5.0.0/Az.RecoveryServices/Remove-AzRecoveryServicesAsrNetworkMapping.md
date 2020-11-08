---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: ef251bb9d1060e511658f9174cde2c04ab288ed7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278044"
---
# <span data-ttu-id="1b72f-101">Remove-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="1b72f-101">Remove-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="1b72f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b72f-102">SYNOPSIS</span></span>
<span data-ttu-id="1b72f-103">Belirtilen ASR Ağ eşlemesini kurtarma hizmetleri kasasından siler.</span><span class="sxs-lookup"><span data-stu-id="1b72f-103">Deletes the specified ASR network mapping from the Recovery Services vault.</span></span>

## <span data-ttu-id="1b72f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1b72f-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b72f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1b72f-105">DESCRIPTION</span></span>
<span data-ttu-id="1b72f-106">**Remove-AzRecoveryServicesAsrNetworkMapping** cmdlet 'ı belirtilen ASR Ağ eşlemesini siler.</span><span class="sxs-lookup"><span data-stu-id="1b72f-106">The **Remove-AzRecoveryServicesAsrNetworkMapping** cmdlet deletes the specified ASR network mapping.</span></span>

## <span data-ttu-id="1b72f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1b72f-107">EXAMPLES</span></span>

### <span data-ttu-id="1b72f-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1b72f-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrNetworkMapping -NetworkMapping $networkmapping
```

<span data-ttu-id="1b72f-109">Belirtilen ASR ağ eşlemesinin silinmesini başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="1b72f-109">Starts the deletion of specified ASR network mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="1b72f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1b72f-110">PARAMETERS</span></span>

### <span data-ttu-id="1b72f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b72f-111">-DefaultProfile</span></span>
<span data-ttu-id="1b72f-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1b72f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="1b72f-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1b72f-113">-InputObject</span></span>
<span data-ttu-id="1b72f-114">Cmdlet 'e giriş nesnesi: ASR ağ eşlemesine yönelik ASR ağ eşleme nesnesi silinecek.</span><span class="sxs-lookup"><span data-stu-id="1b72f-114">The input object to the cmdlet: The ASR network mapping object corresponding to the ASR network mapping to be deleted.</span></span>

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

### <span data-ttu-id="1b72f-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="1b72f-115">-Confirm</span></span>
<span data-ttu-id="1b72f-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1b72f-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b72f-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b72f-117">-WhatIf</span></span>
<span data-ttu-id="1b72f-118">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1b72f-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1b72f-119">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1b72f-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b72f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b72f-120">CommonParameters</span></span>
<span data-ttu-id="1b72f-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1b72f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b72f-122">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1b72f-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b72f-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1b72f-123">INPUTS</span></span>

### <span data-ttu-id="1b72f-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="1b72f-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="1b72f-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1b72f-125">OUTPUTS</span></span>

### <span data-ttu-id="1b72f-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="1b72f-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="1b72f-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1b72f-127">NOTES</span></span>

## <span data-ttu-id="1b72f-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1b72f-128">RELATED LINKS</span></span>

[<span data-ttu-id="1b72f-129">Get-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="1b72f-129">Get-AzRecoveryServicesAsrNetworkMapping</span></span>](./Get-AzRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="1b72f-130">Yeni-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="1b72f-130">New-AzRecoveryServicesAsrNetworkMapping</span></span>](./New-AzRecoveryServicesAsrNetworkMapping.md)
