---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectableItem.md
ms.openlocfilehash: 57f9009ead66eb87685aaf0142c6dbd8b125f307
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759661"
---
# <span data-ttu-id="0ecb6-101">New-AzRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="0ecb6-101">New-AzRecoveryServicesAsrProtectableItem</span></span>

## <span data-ttu-id="0ecb6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ecb6-102">SYNOPSIS</span></span>
<span data-ttu-id="0ecb6-103">Korunabilir öğeler listesine fiziksel bir sunucu ekleyin (keşfedin).</span><span class="sxs-lookup"><span data-stu-id="0ecb6-103">Add(Discover) a physical server to the list of protectable items.</span></span>

## <span data-ttu-id="0ecb6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0ecb6-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrProtectableItem -ProtectionContainer <ASRProtectionContainer> -FriendlyName <String>
 -IPAddress <String> -OSType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0ecb6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0ecb6-105">DESCRIPTION</span></span>
<span data-ttu-id="0ecb6-106">**Yeni-Azrecoveryservicesasrkorumatabloöğesi** , ASR yapısı içindeki bir koruma kapsayıcısındaki bulunan korunabilir öğeler listesine yeni bir korunabilir öğe ekler (yalnızca VMware Fabric türü için geçerlidir).</span><span class="sxs-lookup"><span data-stu-id="0ecb6-106">The **New-AzRecoveryServicesAsrProtectableItem** adds a new protectable item to the list of discovered protectable items in a protection container within an ASR fabric (applicable only for the VMware fabric type).</span></span>

## <span data-ttu-id="0ecb6-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0ecb6-107">EXAMPLES</span></span>

### <span data-ttu-id="0ecb6-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0ecb6-108">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesAsrProtectableItem -ProtectionContainer $pc -Name $name -IPAddress $ipaddresss -OSType $OsType
```

<span data-ttu-id="0ecb6-109">Yeni Azure kurtarma hizmeti korunabilir öğesi ekleyin veya keşfedin.</span><span class="sxs-lookup"><span data-stu-id="0ecb6-109">Add or Discover new Azure Recovery Service ProtectableItem.</span></span>

## <span data-ttu-id="0ecb6-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0ecb6-110">PARAMETERS</span></span>

### <span data-ttu-id="0ecb6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ecb6-111">-DefaultProfile</span></span>
<span data-ttu-id="0ecb6-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0ecb6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ecb6-113">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="0ecb6-113">-FriendlyName</span></span>
<span data-ttu-id="0ecb6-114">Korunabilir öğe için kolay ad.</span><span class="sxs-lookup"><span data-stu-id="0ecb6-114">Friendly name for the protectable item.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ecb6-115">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="0ecb6-115">-IPAddress</span></span>
<span data-ttu-id="0ecb6-116">Korunabilir öğenin IP adresi.</span><span class="sxs-lookup"><span data-stu-id="0ecb6-116">IP address of the protectable item.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ecb6-117">-OSType</span><span class="sxs-lookup"><span data-stu-id="0ecb6-117">-OSType</span></span>
<span data-ttu-id="0ecb6-118">Korunabilir öğesinin işletim sistemi türü (Windows/Linux).</span><span class="sxs-lookup"><span data-stu-id="0ecb6-118">Operating System type (Windows/Linux) of the protectable item.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ecb6-119">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="0ecb6-119">-ProtectionContainer</span></span>
<span data-ttu-id="0ecb6-120">Korunabilir öğenin eklenmesi gereken ASR koruma kapsayıcısı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="0ecb6-120">ASR Protection container object to which the protectable item should be added.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0ecb6-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="0ecb6-121">-Confirm</span></span>
<span data-ttu-id="0ecb6-122">Cmdlet 'i çalıştırmadan önce onay için istemde bulun.</span><span class="sxs-lookup"><span data-stu-id="0ecb6-122">Prompt for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ecb6-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ecb6-123">-WhatIf</span></span>
<span data-ttu-id="0ecb6-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0ecb6-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0ecb6-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0ecb6-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ecb6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ecb6-126">CommonParameters</span></span>
<span data-ttu-id="0ecb6-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0ecb6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ecb6-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ecb6-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ecb6-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0ecb6-129">INPUTS</span></span>

### <span data-ttu-id="0ecb6-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="0ecb6-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="0ecb6-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0ecb6-131">OUTPUTS</span></span>

### <span data-ttu-id="0ecb6-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="0ecb6-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="0ecb6-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0ecb6-133">NOTES</span></span>

## <span data-ttu-id="0ecb6-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0ecb6-134">RELATED LINKS</span></span>
