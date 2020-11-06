---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrVCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrVCenter.md
ms.openlocfilehash: 505d2d81eefed3132cd693ea6cd989fde173b8b3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593658"
---
# <span data-ttu-id="7331a-101">Remove-AzureRmRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="7331a-101">Remove-AzureRmRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="7331a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7331a-102">SYNOPSIS</span></span>
<span data-ttu-id="7331a-103">VCenter Server 'dan vCenter Server 'ı kaldırır ve vCenter sunucusundan sanal makinelerin bulunmasını durdurur.</span><span class="sxs-lookup"><span data-stu-id="7331a-103">Removes the vCenter server from the ASR fabric and stops discovery of virtual machines from the vCenter server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7331a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7331a-104">SYNTAX</span></span>

### <span data-ttu-id="7331a-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7331a-105">Default (Default)</span></span>
```
Remove-AzureRmRecoveryServicesAsrvCenter -InputObject <ASRvCenter> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7331a-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="7331a-106">ByResourceId</span></span>
```
Remove-AzureRmRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7331a-107">ByName</span><span class="sxs-lookup"><span data-stu-id="7331a-107">ByName</span></span>
```
Remove-AzureRmRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7331a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="7331a-108">DESCRIPTION</span></span>
<span data-ttu-id="7331a-109">**Remove-AzureRmRecoveryServicesAsrvCenter** cmdlet 'ı, vCenter sunucusunu ASR yapıdan kaldırır ve vCenter sunucusundan sanal makinelerin bulunmasını durdurur.</span><span class="sxs-lookup"><span data-stu-id="7331a-109">The **Remove-AzureRmRecoveryServicesAsrvCenter** cmdlet removes the vCenter server from the ASR fabric and stops discovery of virtual machines from the vCenter server.</span></span>

## <span data-ttu-id="7331a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7331a-110">EXAMPLES</span></span>

### <span data-ttu-id="7331a-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7331a-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmRecoveryServicesAsrvCenterServer -InputObject $vCenter
```

<span data-ttu-id="7331a-112">ASR sunucusunu ASR yapıdan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7331a-112">Removes the vCenter server from the ASR fabric.</span></span>

## <span data-ttu-id="7331a-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7331a-113">PARAMETERS</span></span>

### <span data-ttu-id="7331a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7331a-114">-DefaultProfile</span></span>
<span data-ttu-id="7331a-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7331a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7331a-116">-Kumaş</span><span class="sxs-lookup"><span data-stu-id="7331a-116">-Fabric</span></span>
<span data-ttu-id="7331a-117">Yapılandırma sunucusunu temsil eden ASR Fabric nesnesi.</span><span class="sxs-lookup"><span data-stu-id="7331a-117">ASR fabric object representing the Configuration Server.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7331a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7331a-118">-InputObject</span></span>
<span data-ttu-id="7331a-119">Kaldırılacak vCenter sunucusunu temsil eden ASR vCenter nesnesi.</span><span class="sxs-lookup"><span data-stu-id="7331a-119">ASR vCenter object representing the vCenter server to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter
Parameter Sets: Default
Aliases: vCenter

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7331a-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="7331a-120">-Name</span></span>
<span data-ttu-id="7331a-121">VCenter sunucusunun adı.</span><span class="sxs-lookup"><span data-stu-id="7331a-121">Name of the vCenter Server.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7331a-122">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="7331a-122">-ResourceId</span></span>
<span data-ttu-id="7331a-123">Kaldırılacak vCenter 'ın RESOURCEID 'yi belirtir.</span><span class="sxs-lookup"><span data-stu-id="7331a-123">Specifies the resourceId of vCenter to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7331a-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="7331a-124">-Confirm</span></span>
<span data-ttu-id="7331a-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7331a-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7331a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7331a-126">-WhatIf</span></span>
<span data-ttu-id="7331a-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7331a-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7331a-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7331a-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7331a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7331a-129">CommonParameters</span></span>
<span data-ttu-id="7331a-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7331a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7331a-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7331a-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7331a-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7331a-132">INPUTS</span></span>

### <span data-ttu-id="7331a-133">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRvCenter</span><span class="sxs-lookup"><span data-stu-id="7331a-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

## <span data-ttu-id="7331a-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7331a-134">OUTPUTS</span></span>

### <span data-ttu-id="7331a-135">System. Koleksiyonlar. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. Sıterecovery. ASRJob, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 0.1.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="7331a-135">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="7331a-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7331a-136">NOTES</span></span>

## <span data-ttu-id="7331a-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7331a-137">RELATED LINKS</span></span>
