---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrVCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrVCenter.md
ms.openlocfilehash: 1d298a543071c879e2279734247febba00b8da21
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573361"
---
# <span data-ttu-id="55367-101">New-AzureRmRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="55367-101">New-AzureRmRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="55367-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55367-102">SYNOPSIS</span></span>
<span data-ttu-id="55367-103">Korunabilir öğeleri bulmak için bir vCenter sunucusu ekler.</span><span class="sxs-lookup"><span data-stu-id="55367-103">Adds a vCenter server to discover protectable items from.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55367-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="55367-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String> -Account <ASRRunAsAccount>
 -Port <Int32> -IpOrHostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="55367-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="55367-105">DESCRIPTION</span></span>
<span data-ttu-id="55367-106">**Yeni-AzureRmRecoveryServicesAsrvCenter** cmdlet 'i, korunabilir öğeleri bulmak Için bir vCenter sunucusu ekler.</span><span class="sxs-lookup"><span data-stu-id="55367-106">The **New-AzureRmRecoveryServicesAsrvCenter** cmdlet adds a vCenter server to discover protectable items from.</span></span> <span data-ttu-id="55367-107">Bu cmdlet, vCenter Server 'ı yapılandırma sunucusuyla bulmaya kaydeder.</span><span class="sxs-lookup"><span data-stu-id="55367-107">This cmdlet registers the vCenter server for discovery with the Configuration server.</span></span>

## <span data-ttu-id="55367-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="55367-108">EXAMPLES</span></span>

### <span data-ttu-id="55367-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="55367-109">Example 1</span></span>
```
PS C:\> New-AzureRmRecoveryServicesAsrvCenterServer -Account $ConfigServer.FabricSpecificDetails.RunAsAccounts[1] -Fabric $ConfigServer -Name InmTest59 -Port 443 -Server 10.150.209.6

Asr Job for vCenter creation.
```

<span data-ttu-id="55367-110">Korunabilir öğeleri bulmak için bir vCenter sunucusu ekler.</span><span class="sxs-lookup"><span data-stu-id="55367-110">Adds a vCenter server to discover protectable items from.</span></span>

## <span data-ttu-id="55367-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="55367-111">PARAMETERS</span></span>

### <span data-ttu-id="55367-112">-Hesap</span><span class="sxs-lookup"><span data-stu-id="55367-112">-Account</span></span>
<span data-ttu-id="55367-113">Kullanıcı oturum açma kimliği.</span><span class="sxs-lookup"><span data-stu-id="55367-113">User login creadential Account.</span></span>

```yaml
Type: ASRRunAsAccount
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55367-114">-Onay</span><span class="sxs-lookup"><span data-stu-id="55367-114">-Confirm</span></span>
<span data-ttu-id="55367-115">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="55367-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55367-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55367-116">-DefaultProfile</span></span>
<span data-ttu-id="55367-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="55367-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55367-118">-Kumaş</span><span class="sxs-lookup"><span data-stu-id="55367-118">-Fabric</span></span>
<span data-ttu-id="55367-119">Yapılandırma sunucusuna karşılık gelen ASR yapısı.</span><span class="sxs-lookup"><span data-stu-id="55367-119">ASR fabric corresponding to the Configuration server.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="55367-120">-Iporanabilgisayaradı</span><span class="sxs-lookup"><span data-stu-id="55367-120">-IpOrHostName</span></span>
<span data-ttu-id="55367-121">VCenter sunucusunun IPv4 adresi veya FQDN 'SI.</span><span class="sxs-lookup"><span data-stu-id="55367-121">IPv4 address or FQDN of the vCenter server.</span></span>

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

### <span data-ttu-id="55367-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="55367-122">-Name</span></span>
<span data-ttu-id="55367-123">VCenter sunucusunun kolay adı.</span><span class="sxs-lookup"><span data-stu-id="55367-123">A friendly name for the vCenter server.</span></span>

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

### <span data-ttu-id="55367-124">-Bağlantı noktası</span><span class="sxs-lookup"><span data-stu-id="55367-124">-Port</span></span>
<span data-ttu-id="55367-125">Bulma için kullanılacak vCenter sunucusundaki TCP bağlantı noktası.</span><span class="sxs-lookup"><span data-stu-id="55367-125">The TCP port on the vCenter server to use for discovery.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55367-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55367-126">-WhatIf</span></span>
<span data-ttu-id="55367-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="55367-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55367-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="55367-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55367-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55367-129">CommonParameters</span></span>
<span data-ttu-id="55367-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="55367-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55367-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55367-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55367-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="55367-132">INPUTS</span></span>

### <span data-ttu-id="55367-133">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="55367-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="55367-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="55367-134">OUTPUTS</span></span>

### <span data-ttu-id="55367-135">System. Koleksiyonlar. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. Sıterecovery. ASRJob, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 0.1.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="55367-135">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="55367-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="55367-136">NOTES</span></span>

## <span data-ttu-id="55367-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="55367-137">RELATED LINKS</span></span>
