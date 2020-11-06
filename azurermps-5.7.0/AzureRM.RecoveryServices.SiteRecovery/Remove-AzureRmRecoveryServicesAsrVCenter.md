---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrVCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrVCenter.md
ms.openlocfilehash: eaa357e6dd216b62a2c8e8f1cd78ff15387be57a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589731"
---
# <span data-ttu-id="2ca34-101">Remove-AzureRmRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="2ca34-101">Remove-AzureRmRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="2ca34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ca34-102">SYNOPSIS</span></span>
<span data-ttu-id="2ca34-103">VCenter Server 'dan vCenter Server 'ı kaldırır ve vCenter sunucusundan sanal makinelerin bulunmasını durdurur.</span><span class="sxs-lookup"><span data-stu-id="2ca34-103">Removes the vCenter server from the ASR fabric and stops discovery of virtual machines from the vCenter server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ca34-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2ca34-104">SYNTAX</span></span>

### <span data-ttu-id="2ca34-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2ca34-105">Default (Default)</span></span>
```
Remove-AzureRmRecoveryServicesAsrvCenter -InputObject <ASRvCenter> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ca34-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="2ca34-106">ByResourceId</span></span>
```
Remove-AzureRmRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ca34-107">ByName</span><span class="sxs-lookup"><span data-stu-id="2ca34-107">ByName</span></span>
```
Remove-AzureRmRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ca34-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="2ca34-108">DESCRIPTION</span></span>
<span data-ttu-id="2ca34-109">**Remove-AzureRmRecoveryServicesAsrvCenter** cmdlet 'ı, vCenter sunucusunu ASR yapıdan kaldırır ve vCenter sunucusundan sanal makinelerin bulunmasını durdurur.</span><span class="sxs-lookup"><span data-stu-id="2ca34-109">The **Remove-AzureRmRecoveryServicesAsrvCenter** cmdlet removes the vCenter server from the ASR fabric and stops discovery of virtual machines from the vCenter server.</span></span>

## <span data-ttu-id="2ca34-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2ca34-110">EXAMPLES</span></span>

### <span data-ttu-id="2ca34-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2ca34-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmRecoveryServicesAsrvCenterServer -InputObject $vCenter
```

<span data-ttu-id="2ca34-112">ASR sunucusunu ASR yapıdan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2ca34-112">Removes the vCenter server from the ASR fabric.</span></span>

## <span data-ttu-id="2ca34-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2ca34-113">PARAMETERS</span></span>

### <span data-ttu-id="2ca34-114">-Onay</span><span class="sxs-lookup"><span data-stu-id="2ca34-114">-Confirm</span></span>
<span data-ttu-id="2ca34-115">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2ca34-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ca34-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ca34-116">-DefaultProfile</span></span>
<span data-ttu-id="2ca34-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2ca34-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ca34-118">-Kumaş</span><span class="sxs-lookup"><span data-stu-id="2ca34-118">-Fabric</span></span>
<span data-ttu-id="2ca34-119">Yapılandırma sunucusunu temsil eden ASR Fabric nesnesi.</span><span class="sxs-lookup"><span data-stu-id="2ca34-119">ASR fabric object representing the Configuration Server.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2ca34-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2ca34-120">-InputObject</span></span>
<span data-ttu-id="2ca34-121">Kaldırılacak vCenter sunucusunu temsil eden ASR vCenter nesnesi.</span><span class="sxs-lookup"><span data-stu-id="2ca34-121">ASR vCenter object representing the vCenter server to be removed.</span></span>

```yaml
Type: ASRvCenter
Parameter Sets: Default
Aliases: vCenter

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2ca34-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="2ca34-122">-Name</span></span>
<span data-ttu-id="2ca34-123">VCenter sunucusunun adı.</span><span class="sxs-lookup"><span data-stu-id="2ca34-123">Name of the vCenter Server.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ca34-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="2ca34-124">-ResourceId</span></span>
<span data-ttu-id="2ca34-125">Kaldırılacak vCenter 'ın RESOURCEID 'yi belirtir.</span><span class="sxs-lookup"><span data-stu-id="2ca34-125">Specifies the resourceId of vCenter to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ca34-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ca34-126">-WhatIf</span></span>
<span data-ttu-id="2ca34-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2ca34-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ca34-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2ca34-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ca34-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ca34-129">CommonParameters</span></span>
<span data-ttu-id="2ca34-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2ca34-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ca34-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ca34-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ca34-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2ca34-132">INPUTS</span></span>

### <span data-ttu-id="2ca34-133">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRvCenter</span><span class="sxs-lookup"><span data-stu-id="2ca34-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

## <span data-ttu-id="2ca34-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2ca34-134">OUTPUTS</span></span>

### <span data-ttu-id="2ca34-135">System. Koleksiyonlar. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. Sıterecovery. ASRJob, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 0.1.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="2ca34-135">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="2ca34-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2ca34-136">NOTES</span></span>

## <span data-ttu-id="2ca34-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2ca34-137">RELATED LINKS</span></span>
