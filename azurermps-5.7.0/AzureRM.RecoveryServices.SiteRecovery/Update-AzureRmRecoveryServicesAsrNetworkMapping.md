---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/update-azurermrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: be521545111667493c5b0e268013ffa4464ed3a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573341"
---
# <span data-ttu-id="08ae6-101">Update-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="08ae6-101">Update-AzureRmRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="08ae6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08ae6-102">SYNOPSIS</span></span>
<span data-ttu-id="08ae6-103">Belirtilen Azure Site Recovery Ağ eşlemesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="08ae6-103">Updates the specified azure site recovery network mapping.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="08ae6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="08ae6-104">SYNTAX</span></span>

### <span data-ttu-id="08ae6-105">ByNetworkObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="08ae6-105">ByNetworkObject (Default)</span></span>
```
Update-AzureRmRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping> -RecoveryNetwork <ASRNetwork>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08ae6-106">Byıd</span><span class="sxs-lookup"><span data-stu-id="08ae6-106">ById</span></span>
```
Update-AzureRmRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping>
 -RecoveryAzureNetworkId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="08ae6-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="08ae6-107">DESCRIPTION</span></span>
<span data-ttu-id="08ae6-108">**Update-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet 'ı belirtilen Azure Site Recovery Ağ eşlemesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="08ae6-108">The **Update-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet updates the specified Azure Site Recovery network mapping.</span></span>

## <span data-ttu-id="08ae6-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="08ae6-109">EXAMPLES</span></span>

### <span data-ttu-id="08ae6-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="08ae6-110">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrNetworkMapping -Mapping $NetworkMapping -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="08ae6-111">Belirtilen parametreleri kullanarak Ağ eşlemesini Güncelleştir işlemini başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="08ae6-111">Starts the update network mapping operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="08ae6-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="08ae6-112">PARAMETERS</span></span>

### <span data-ttu-id="08ae6-113">-Onay</span><span class="sxs-lookup"><span data-stu-id="08ae6-113">-Confirm</span></span>
<span data-ttu-id="08ae6-114">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="08ae6-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08ae6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08ae6-115">-DefaultProfile</span></span>
<span data-ttu-id="08ae6-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="08ae6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08ae6-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="08ae6-117">-InputObject</span></span>
<span data-ttu-id="08ae6-118">Giriş nesnesi: güncelleştirilecek ASR ağ eşleme nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="08ae6-118">Input Object: Specifies the ASR network mapping object corresponding to the ASR network mapping to be updated.</span></span>

```yaml
Type: ASRNetworkMapping
Parameter Sets: (All)
Aliases: NetworkMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="08ae6-119">-Recoveryazurenetworkıd</span><span class="sxs-lookup"><span data-stu-id="08ae6-119">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="08ae6-120">Ağ eşlemesi için kurtarma Azure ağ KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="08ae6-120">Specifies the recovery azure network ID for the network mapping.</span></span>

```yaml
Type: String
Parameter Sets: ById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08ae6-121">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="08ae6-121">-RecoveryNetwork</span></span>
<span data-ttu-id="08ae6-122">Ağ eşlemesi için kurtarma ağı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="08ae6-122">Specifies the recovery network object for the network mapping.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: ByNetworkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08ae6-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08ae6-123">-WhatIf</span></span>
<span data-ttu-id="08ae6-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="08ae6-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="08ae6-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="08ae6-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08ae6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08ae6-126">CommonParameters</span></span>
<span data-ttu-id="08ae6-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="08ae6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08ae6-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08ae6-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08ae6-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="08ae6-129">INPUTS</span></span>

### <span data-ttu-id="08ae6-130">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="08ae6-130">None</span></span>

## <span data-ttu-id="08ae6-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="08ae6-131">OUTPUTS</span></span>

### <span data-ttu-id="08ae6-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="08ae6-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="08ae6-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="08ae6-133">NOTES</span></span>

## <span data-ttu-id="08ae6-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="08ae6-134">RELATED LINKS</span></span>
