---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/update-azurermrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: fb92ec38bcbe7addb23f274616cde0fd84ebbafc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587195"
---
# <span data-ttu-id="7bb69-101">Update-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="7bb69-101">Update-AzureRmRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="7bb69-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7bb69-102">SYNOPSIS</span></span>
<span data-ttu-id="7bb69-103">Belirtilen Azure Site Recovery Ağ eşlemesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="7bb69-103">Updates the specified azure site recovery network mapping.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7bb69-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7bb69-104">SYNTAX</span></span>

### <span data-ttu-id="7bb69-105">ByNetworkObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7bb69-105">ByNetworkObject (Default)</span></span>
```
Update-AzureRmRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping> -RecoveryNetwork <ASRNetwork>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7bb69-106">Byıd</span><span class="sxs-lookup"><span data-stu-id="7bb69-106">ById</span></span>
```
Update-AzureRmRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping>
 -RecoveryAzureNetworkId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7bb69-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="7bb69-107">DESCRIPTION</span></span>
<span data-ttu-id="7bb69-108">**Update-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet 'ı belirtilen Azure Site Recovery Ağ eşlemesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="7bb69-108">The **Update-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet updates the specified Azure Site Recovery network mapping.</span></span>

## <span data-ttu-id="7bb69-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7bb69-109">EXAMPLES</span></span>

### <span data-ttu-id="7bb69-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7bb69-110">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrNetworkMapping -Mapping $NetworkMapping -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="7bb69-111">Belirtilen parametreleri kullanarak Ağ eşlemesini Güncelleştir işlemini başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="7bb69-111">Starts the update network mapping operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="7bb69-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7bb69-112">PARAMETERS</span></span>

### <span data-ttu-id="7bb69-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bb69-113">-DefaultProfile</span></span>
<span data-ttu-id="7bb69-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7bb69-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="7bb69-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7bb69-115">-InputObject</span></span>
<span data-ttu-id="7bb69-116">Giriş nesnesi: güncelleştirilecek ASR ağ eşleme nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7bb69-116">Input Object: Specifies the ASR network mapping object corresponding to the ASR network mapping to be updated.</span></span>

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

### <span data-ttu-id="7bb69-117">-Recoveryazurenetworkıd</span><span class="sxs-lookup"><span data-stu-id="7bb69-117">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="7bb69-118">Ağ eşlemesi için kurtarma Azure ağ KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="7bb69-118">Specifies the recovery azure network ID for the network mapping.</span></span>

```yaml
Type: System.String
Parameter Sets: ById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bb69-119">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="7bb69-119">-RecoveryNetwork</span></span>
<span data-ttu-id="7bb69-120">Ağ eşlemesi için kurtarma ağı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7bb69-120">Specifies the recovery network object for the network mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork
Parameter Sets: ByNetworkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bb69-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="7bb69-121">-Confirm</span></span>
<span data-ttu-id="7bb69-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7bb69-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7bb69-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bb69-123">-WhatIf</span></span>
<span data-ttu-id="7bb69-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7bb69-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7bb69-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7bb69-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7bb69-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bb69-126">CommonParameters</span></span>
<span data-ttu-id="7bb69-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7bb69-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bb69-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7bb69-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bb69-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7bb69-129">INPUTS</span></span>

### <span data-ttu-id="7bb69-130">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="7bb69-130">None</span></span>

## <span data-ttu-id="7bb69-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7bb69-131">OUTPUTS</span></span>

### <span data-ttu-id="7bb69-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="7bb69-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="7bb69-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7bb69-133">NOTES</span></span>

## <span data-ttu-id="7bb69-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7bb69-134">RELATED LINKS</span></span>
