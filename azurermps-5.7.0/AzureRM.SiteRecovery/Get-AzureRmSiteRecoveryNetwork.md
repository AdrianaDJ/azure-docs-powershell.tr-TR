---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 4CC5E6A8-B51A-49ED-BB93-FE63F1500780
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoverynetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryNetwork.md
ms.openlocfilehash: 6ffd3a295ecc228ec395a00ba597f2d7b0967a2e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762511"
---
# <span data-ttu-id="6aa9c-101">Get-AzureRmSiteRecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="6aa9c-101">Get-AzureRmSiteRecoveryNetwork</span></span>

## <span data-ttu-id="6aa9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6aa9c-102">SYNOPSIS</span></span>
<span data-ttu-id="6aa9c-103">Geçerli kasa için site kurtarma tarafından yönetilen ağlar hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="6aa9c-103">Gets information about the networks managed by Site Recovery for the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6aa9c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6aa9c-104">SYNTAX</span></span>

### <span data-ttu-id="6aa9c-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6aa9c-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryNetwork [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6aa9c-106">ByServerObject</span><span class="sxs-lookup"><span data-stu-id="6aa9c-106">ByServerObject</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Server <ASRServer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6aa9c-107">Binamelegacy</span><span class="sxs-lookup"><span data-stu-id="6aa9c-107">ByNameLegacy</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Server <ASRServer> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6aa9c-108">Byetlynamelegacy</span><span class="sxs-lookup"><span data-stu-id="6aa9c-108">ByFriendlyNameLegacy</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Server <ASRServer> -FriendlyName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6aa9c-109">ByFabricObject</span><span class="sxs-lookup"><span data-stu-id="6aa9c-109">ByFabricObject</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6aa9c-110">ByName</span><span class="sxs-lookup"><span data-stu-id="6aa9c-110">ByName</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Fabric <ASRFabric> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6aa9c-111">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="6aa9c-111">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Fabric <ASRFabric> -FriendlyName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6aa9c-112">Tanım</span><span class="sxs-lookup"><span data-stu-id="6aa9c-112">DESCRIPTION</span></span>
<span data-ttu-id="6aa9c-113">**Get-AzureRmSiteRecoveryNetwork** cmdlet 'i, geçerli Azure Site Recovery Kasası Için Azure Site Recovery ağları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="6aa9c-113">The **Get-AzureRmSiteRecoveryNetwork** cmdlet gets information about Azure Site Recovery networks for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="6aa9c-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6aa9c-114">EXAMPLES</span></span>

## <span data-ttu-id="6aa9c-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6aa9c-115">PARAMETERS</span></span>

### <span data-ttu-id="6aa9c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6aa9c-116">-DefaultProfile</span></span>
<span data-ttu-id="6aa9c-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6aa9c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6aa9c-118">-Kumaş</span><span class="sxs-lookup"><span data-stu-id="6aa9c-118">-Fabric</span></span>
```yaml
Type: ASRFabric
Parameter Sets: ByFabricObject, ByName, ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6aa9c-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="6aa9c-119">-FriendlyName</span></span>
<span data-ttu-id="6aa9c-120">Sanal makine ağının kolay adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6aa9c-120">Specifies the friendly name of the virtual machine network.</span></span>

```yaml
Type: String
Parameter Sets: ByFriendlyNameLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6aa9c-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="6aa9c-121">-Name</span></span>
<span data-ttu-id="6aa9c-122">Sanal makine ağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6aa9c-122">Specifies the name of the virtual machine network.</span></span>

```yaml
Type: String
Parameter Sets: ByNameLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6aa9c-123">-Sunucu</span><span class="sxs-lookup"><span data-stu-id="6aa9c-123">-Server</span></span>
```yaml
Type: ASRServer
Parameter Sets: ByServerObject, ByNameLegacy, ByFriendlyNameLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6aa9c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6aa9c-124">CommonParameters</span></span>
<span data-ttu-id="6aa9c-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6aa9c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6aa9c-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6aa9c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6aa9c-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6aa9c-127">INPUTS</span></span>

### <span data-ttu-id="6aa9c-128">ASRFabric</span><span class="sxs-lookup"><span data-stu-id="6aa9c-128">ASRFabric</span></span>
<span data-ttu-id="6aa9c-129">Parametre ' Fabric ', ardışık düzenin ' ASRFabric ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="6aa9c-129">Parameter 'Fabric' accepts value of type 'ASRFabric' from the pipeline</span></span>

### <span data-ttu-id="6aa9c-130">Dizisi</span><span class="sxs-lookup"><span data-stu-id="6aa9c-130">String</span></span>
<span data-ttu-id="6aa9c-131">' FriendlyName ' parametresi ardışık düzenin ' String ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="6aa9c-131">Parameter 'FriendlyName' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="6aa9c-132">Dizisi</span><span class="sxs-lookup"><span data-stu-id="6aa9c-132">String</span></span>
<span data-ttu-id="6aa9c-133">' FriendlyName ' parametresi ardışık düzenin ' String ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="6aa9c-133">Parameter 'FriendlyName' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="6aa9c-134">Dizisi</span><span class="sxs-lookup"><span data-stu-id="6aa9c-134">String</span></span>
<span data-ttu-id="6aa9c-135">' Name ' parametresi ardışık düzenin ' String ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="6aa9c-135">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="6aa9c-136">Dizisi</span><span class="sxs-lookup"><span data-stu-id="6aa9c-136">String</span></span>
<span data-ttu-id="6aa9c-137">' Name ' parametresi ardışık düzenin ' String ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="6aa9c-137">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="6aa9c-138">ASRServer</span><span class="sxs-lookup"><span data-stu-id="6aa9c-138">ASRServer</span></span>
<span data-ttu-id="6aa9c-139">' Server ' parametresi ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="6aa9c-139">Parameter 'Server' accepts value of type 'ASRServer' from the pipeline</span></span>

## <span data-ttu-id="6aa9c-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6aa9c-140">OUTPUTS</span></span>

### <span data-ttu-id="6aa9c-141">System. Koleksiyonlar. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRNetwork]</span><span class="sxs-lookup"><span data-stu-id="6aa9c-141">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRNetwork]</span></span>

## <span data-ttu-id="6aa9c-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6aa9c-142">NOTES</span></span>

## <span data-ttu-id="6aa9c-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6aa9c-143">RELATED LINKS</span></span>

