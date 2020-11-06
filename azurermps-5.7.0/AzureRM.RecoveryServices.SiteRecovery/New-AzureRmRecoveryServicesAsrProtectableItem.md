---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrProtectableItem.md
ms.openlocfilehash: 8973c3606c7c29c254650b3412275c1dfd7bf761
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593452"
---
# <span data-ttu-id="7ae7c-101">New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="7ae7c-101">New-AzureRmRecoveryServicesAsrProtectableItem</span></span>

## <span data-ttu-id="7ae7c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ae7c-102">SYNOPSIS</span></span>
<span data-ttu-id="7ae7c-103">Korunabilir öğeler listesine fiziksel bir sunucu ekleyin (keşfedin).</span><span class="sxs-lookup"><span data-stu-id="7ae7c-103">Add(Discover) a physical server to the list of protectable items.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7ae7c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7ae7c-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesAsrProtectableItem -ProtectionContainer <ASRProtectionContainer>
 -FriendlyName <String> -IPAddress <String> -OSType <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ae7c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7ae7c-105">DESCRIPTION</span></span>
<span data-ttu-id="7ae7c-106">**New-Azurermrecoveryservicesasrkorunabilir TableItem** , bir ASR yapısı içindeki bir koruma kapsayıcısındaki bulunan korunabilir öğeler listesine yeni bir korunabilir öğe ekler (yalnızca VMware Fabric türü için geçerlidir).</span><span class="sxs-lookup"><span data-stu-id="7ae7c-106">The **New-AzureRmRecoveryServicesAsrProtectableItem** adds a new protectable item to the list of discovered protectable items in a protection container within an ASR fabric (applicable only for the VMware fabric type).</span></span>

## <span data-ttu-id="7ae7c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7ae7c-107">EXAMPLES</span></span>

### <span data-ttu-id="7ae7c-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7ae7c-108">Example 1</span></span>
```
PS C:\> New-AzureRmRecoveryServicesAsrProtectableItem ProtectionContainer $pc -Name $name -IPAddress $ipaddresss -OSType $OsType
```

<span data-ttu-id="7ae7c-109">Yeni Azure kurtarma hizmeti korunabilir öğesi ekleyin veya keşfedin.</span><span class="sxs-lookup"><span data-stu-id="7ae7c-109">Add or Discover new Azure Recovery Service ProtectableItem.</span></span>

## <span data-ttu-id="7ae7c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7ae7c-110">PARAMETERS</span></span>

### <span data-ttu-id="7ae7c-111">-Onay</span><span class="sxs-lookup"><span data-stu-id="7ae7c-111">-Confirm</span></span>
<span data-ttu-id="7ae7c-112">Cmdlet 'i çalıştırmadan önce onay için istemde bulun.</span><span class="sxs-lookup"><span data-stu-id="7ae7c-112">Prompt for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ae7c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ae7c-113">-DefaultProfile</span></span>
<span data-ttu-id="7ae7c-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7ae7c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ae7c-115">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="7ae7c-115">-FriendlyName</span></span>
<span data-ttu-id="7ae7c-116">Korunabilir öğe için kolay ad.</span><span class="sxs-lookup"><span data-stu-id="7ae7c-116">Friendly name for the protectable item.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ae7c-117">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="7ae7c-117">-IPAddress</span></span>
<span data-ttu-id="7ae7c-118">Korunabilir öğenin IP adresi.</span><span class="sxs-lookup"><span data-stu-id="7ae7c-118">IP address of the protectable item.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ae7c-119">-OSType</span><span class="sxs-lookup"><span data-stu-id="7ae7c-119">-OSType</span></span>
<span data-ttu-id="7ae7c-120">Korunabilir öğesinin işletim sistemi türü (Windows/Linux).</span><span class="sxs-lookup"><span data-stu-id="7ae7c-120">Operating System type (Windows/Linux) of the protectable item.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ae7c-121">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="7ae7c-121">-ProtectionContainer</span></span>
<span data-ttu-id="7ae7c-122">Korunabilir öğenin eklenmesi gereken ASR koruma kapsayıcısı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="7ae7c-122">ASR Protection container object to which the protectable item should be added.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7ae7c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ae7c-123">-WhatIf</span></span>
<span data-ttu-id="7ae7c-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7ae7c-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7ae7c-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7ae7c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ae7c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ae7c-126">CommonParameters</span></span>
<span data-ttu-id="7ae7c-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7ae7c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ae7c-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ae7c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ae7c-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7ae7c-129">INPUTS</span></span>

### <span data-ttu-id="7ae7c-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="7ae7c-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="7ae7c-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7ae7c-131">OUTPUTS</span></span>

### <span data-ttu-id="7ae7c-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="7ae7c-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="7ae7c-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7ae7c-133">NOTES</span></span>

## <span data-ttu-id="7ae7c-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7ae7c-134">RELATED LINKS</span></span>
