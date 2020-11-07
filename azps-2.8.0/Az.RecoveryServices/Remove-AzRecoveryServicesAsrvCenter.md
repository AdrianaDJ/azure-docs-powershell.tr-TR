---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrvCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrvCenter.md
ms.openlocfilehash: c1ac3ae34e92feb2b356d5946a7b9f0a30a0a2aa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932968"
---
# <span data-ttu-id="a3dea-101">Remove-AzRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="a3dea-101">Remove-AzRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="a3dea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3dea-102">SYNOPSIS</span></span>
<span data-ttu-id="a3dea-103">VCenter Server 'dan vCenter Server 'ı kaldırır ve vCenter sunucusundan sanal makinelerin bulunmasını durdurur.</span><span class="sxs-lookup"><span data-stu-id="a3dea-103">Removes the vCenter server from the ASR fabric and stops discovery of virtual machines from the vCenter server.</span></span>

## <span data-ttu-id="a3dea-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a3dea-104">SYNTAX</span></span>

### <span data-ttu-id="a3dea-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a3dea-105">Default (Default)</span></span>
```
Remove-AzRecoveryServicesAsrvCenter -InputObject <ASRvCenter> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3dea-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="a3dea-106">ByResourceId</span></span>
```
Remove-AzRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3dea-107">ByName</span><span class="sxs-lookup"><span data-stu-id="a3dea-107">ByName</span></span>
```
Remove-AzRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3dea-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="a3dea-108">DESCRIPTION</span></span>
<span data-ttu-id="a3dea-109">**Remove-AzRecoveryServicesAsrvCenter** cmdlet 'ı, vCenter sunucusunu ASR yapıdan kaldırır ve vCenter sunucusundan sanal makinelerin bulunmasını durdurur.</span><span class="sxs-lookup"><span data-stu-id="a3dea-109">The **Remove-AzRecoveryServicesAsrvCenter** cmdlet removes the vCenter server from the ASR fabric and stops discovery of virtual machines from the vCenter server.</span></span>

## <span data-ttu-id="a3dea-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a3dea-110">EXAMPLES</span></span>

### <span data-ttu-id="a3dea-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a3dea-111">Example 1</span></span>
```
PS C:\> Remove-AzRecoveryServicesAsrvCenterServer -InputObject $vCenter
```

<span data-ttu-id="a3dea-112">ASR sunucusunu ASR yapıdan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a3dea-112">Removes the vCenter server from the ASR fabric.</span></span>

## <span data-ttu-id="a3dea-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a3dea-113">PARAMETERS</span></span>

### <span data-ttu-id="a3dea-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3dea-114">-DefaultProfile</span></span>
<span data-ttu-id="a3dea-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a3dea-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3dea-116">-Kumaş</span><span class="sxs-lookup"><span data-stu-id="a3dea-116">-Fabric</span></span>
<span data-ttu-id="a3dea-117">Yapılandırma sunucusunu temsil eden ASR Fabric nesnesi.</span><span class="sxs-lookup"><span data-stu-id="a3dea-117">ASR fabric object representing the Configuration Server.</span></span>

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

### <span data-ttu-id="a3dea-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a3dea-118">-InputObject</span></span>
<span data-ttu-id="a3dea-119">Kaldırılacak vCenter sunucusunu temsil eden ASR vCenter nesnesi.</span><span class="sxs-lookup"><span data-stu-id="a3dea-119">ASR vCenter object representing the vCenter server to be removed.</span></span>

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

### <span data-ttu-id="a3dea-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="a3dea-120">-Name</span></span>
<span data-ttu-id="a3dea-121">VCenter sunucusunun adı.</span><span class="sxs-lookup"><span data-stu-id="a3dea-121">Name of the vCenter Server.</span></span>

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

### <span data-ttu-id="a3dea-122">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="a3dea-122">-ResourceId</span></span>
<span data-ttu-id="a3dea-123">Kaldırılacak vCenter 'ın RESOURCEID 'yi belirtir.</span><span class="sxs-lookup"><span data-stu-id="a3dea-123">Specifies the resourceId of vCenter to remove.</span></span>

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

### <span data-ttu-id="a3dea-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="a3dea-124">-Confirm</span></span>
<span data-ttu-id="a3dea-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a3dea-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3dea-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3dea-126">-WhatIf</span></span>
<span data-ttu-id="a3dea-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a3dea-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3dea-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a3dea-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3dea-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3dea-129">CommonParameters</span></span>
<span data-ttu-id="a3dea-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a3dea-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3dea-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3dea-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3dea-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a3dea-132">INPUTS</span></span>

### <span data-ttu-id="a3dea-133">System. String</span><span class="sxs-lookup"><span data-stu-id="a3dea-133">System.String</span></span>

### <span data-ttu-id="a3dea-134">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRvCenter</span><span class="sxs-lookup"><span data-stu-id="a3dea-134">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

### <span data-ttu-id="a3dea-135">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="a3dea-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="a3dea-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a3dea-136">OUTPUTS</span></span>

### <span data-ttu-id="a3dea-137">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="a3dea-137">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="a3dea-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a3dea-138">NOTES</span></span>

## <span data-ttu-id="a3dea-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a3dea-139">RELATED LINKS</span></span>
