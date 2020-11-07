---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrvCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrvCenter.md
ms.openlocfilehash: 8039da508110b47024be75967932719e5436f73b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933483"
---
# <span data-ttu-id="73633-101">New-AzRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="73633-101">New-AzRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="73633-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73633-102">SYNOPSIS</span></span>
<span data-ttu-id="73633-103">Korunabilir öğeleri bulmak için bir vCenter sunucusu ekler.</span><span class="sxs-lookup"><span data-stu-id="73633-103">Adds a vCenter server to discover protectable items from.</span></span>

## <span data-ttu-id="73633-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="73633-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String> -Account <ASRRunAsAccount> -Port <Int32>
 -IpOrHostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73633-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="73633-105">DESCRIPTION</span></span>
<span data-ttu-id="73633-106">**Yeni-AzRecoveryServicesAsrvCenter** cmdlet 'i, korunabilir öğeleri bulmak Için bir vCenter sunucusu ekler.</span><span class="sxs-lookup"><span data-stu-id="73633-106">The **New-AzRecoveryServicesAsrvCenter** cmdlet adds a vCenter server to discover protectable items from.</span></span> <span data-ttu-id="73633-107">Bu cmdlet, vCenter Server 'ı yapılandırma sunucusuyla bulmaya kaydeder.</span><span class="sxs-lookup"><span data-stu-id="73633-107">This cmdlet registers the vCenter server for discovery with the Configuration server.</span></span>

## <span data-ttu-id="73633-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="73633-108">EXAMPLES</span></span>

### <span data-ttu-id="73633-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="73633-109">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesAsrvCenterServer -Account $ConfigServer.FabricSpecificDetails.RunAsAccounts[1] -Fabric $ConfigServer -Name InmTest59 -Port 443 -Server 10.150.209.6

Asr Job for vCenter creation.
```

<span data-ttu-id="73633-110">Korunabilir öğeleri bulmak için bir vCenter sunucusu ekler.</span><span class="sxs-lookup"><span data-stu-id="73633-110">Adds a vCenter server to discover protectable items from.</span></span>

## <span data-ttu-id="73633-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="73633-111">PARAMETERS</span></span>

### <span data-ttu-id="73633-112">-Hesap</span><span class="sxs-lookup"><span data-stu-id="73633-112">-Account</span></span>
<span data-ttu-id="73633-113">Kullanıcı oturum açma kimlik bilgileri hesabı.</span><span class="sxs-lookup"><span data-stu-id="73633-113">User login credential Account.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRunAsAccount
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73633-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73633-114">-DefaultProfile</span></span>
<span data-ttu-id="73633-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="73633-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73633-116">-Kumaş</span><span class="sxs-lookup"><span data-stu-id="73633-116">-Fabric</span></span>
<span data-ttu-id="73633-117">Yapılandırma sunucusuna karşılık gelen ASR yapısı.</span><span class="sxs-lookup"><span data-stu-id="73633-117">ASR fabric corresponding to the Configuration server.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73633-118">-Iporanabilgisayaradı</span><span class="sxs-lookup"><span data-stu-id="73633-118">-IpOrHostName</span></span>
<span data-ttu-id="73633-119">VCenter sunucusunun IPv4 adresi veya FQDN 'SI.</span><span class="sxs-lookup"><span data-stu-id="73633-119">IPv4 address or FQDN of the vCenter server.</span></span>

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

### <span data-ttu-id="73633-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="73633-120">-Name</span></span>
<span data-ttu-id="73633-121">VCenter sunucusunun kolay adı.</span><span class="sxs-lookup"><span data-stu-id="73633-121">A friendly name for the vCenter server.</span></span>

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

### <span data-ttu-id="73633-122">-Bağlantı noktası</span><span class="sxs-lookup"><span data-stu-id="73633-122">-Port</span></span>
<span data-ttu-id="73633-123">Bulma için kullanılacak vCenter sunucusundaki TCP bağlantı noktası.</span><span class="sxs-lookup"><span data-stu-id="73633-123">The TCP port on the vCenter server to use for discovery.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73633-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="73633-124">-Confirm</span></span>
<span data-ttu-id="73633-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="73633-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73633-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73633-126">-WhatIf</span></span>
<span data-ttu-id="73633-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="73633-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73633-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="73633-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73633-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73633-129">CommonParameters</span></span>
<span data-ttu-id="73633-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="73633-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73633-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73633-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73633-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="73633-132">INPUTS</span></span>

### <span data-ttu-id="73633-133">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="73633-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="73633-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="73633-134">OUTPUTS</span></span>

### <span data-ttu-id="73633-135">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="73633-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="73633-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="73633-136">NOTES</span></span>

## <span data-ttu-id="73633-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="73633-137">RELATED LINKS</span></span>
