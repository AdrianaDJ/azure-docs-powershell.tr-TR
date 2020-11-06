---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 4CC5E6A8-B51A-49ED-BB93-FE63F1500780
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryNetwork.md
ms.openlocfilehash: 83410371d517bbd90a0b302d258ff25325e06cf9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589078"
---
# <span data-ttu-id="d680e-101">Get-AzureRmSiteRecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="d680e-101">Get-AzureRmSiteRecoveryNetwork</span></span>

## <span data-ttu-id="d680e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d680e-102">SYNOPSIS</span></span>
<span data-ttu-id="d680e-103">Geçerli kasa için site kurtarma tarafından yönetilen ağlar hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="d680e-103">Gets information about the networks managed by Site Recovery for the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d680e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d680e-104">SYNTAX</span></span>

### <span data-ttu-id="d680e-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d680e-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryNetwork [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d680e-106">ByServerObject</span><span class="sxs-lookup"><span data-stu-id="d680e-106">ByServerObject</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Server <ASRServer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d680e-107">Binamelegacy</span><span class="sxs-lookup"><span data-stu-id="d680e-107">ByNameLegacy</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Server <ASRServer> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d680e-108">Byetlynamelegacy</span><span class="sxs-lookup"><span data-stu-id="d680e-108">ByFriendlyNameLegacy</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Server <ASRServer> -FriendlyName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d680e-109">ByFabricObject</span><span class="sxs-lookup"><span data-stu-id="d680e-109">ByFabricObject</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d680e-110">ByName</span><span class="sxs-lookup"><span data-stu-id="d680e-110">ByName</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Fabric <ASRFabric> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d680e-111">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="d680e-111">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Fabric <ASRFabric> -FriendlyName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d680e-112">Tanım</span><span class="sxs-lookup"><span data-stu-id="d680e-112">DESCRIPTION</span></span>
<span data-ttu-id="d680e-113">**Get-AzureRmSiteRecoveryNetwork** cmdlet 'i, geçerli Azure Site Recovery Kasası Için Azure Site Recovery ağları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="d680e-113">The **Get-AzureRmSiteRecoveryNetwork** cmdlet gets information about Azure Site Recovery networks for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="d680e-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d680e-114">EXAMPLES</span></span>

## <span data-ttu-id="d680e-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d680e-115">PARAMETERS</span></span>

### <span data-ttu-id="d680e-116">-Kumaş</span><span class="sxs-lookup"><span data-stu-id="d680e-116">-Fabric</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRFabric
Parameter Sets: ByFabricObject, ByName, ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d680e-117">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="d680e-117">-FriendlyName</span></span>
<span data-ttu-id="d680e-118">Sanal makine ağının kolay adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d680e-118">Specifies the friendly name of the virtual machine network.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyNameLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d680e-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="d680e-119">-Name</span></span>
<span data-ttu-id="d680e-120">Sanal makine ağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d680e-120">Specifies the name of the virtual machine network.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d680e-121">-Sunucu</span><span class="sxs-lookup"><span data-stu-id="d680e-121">-Server</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRServer
Parameter Sets: ByServerObject, ByNameLegacy, ByFriendlyNameLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d680e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d680e-122">-DefaultProfile</span></span>
<span data-ttu-id="d680e-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d680e-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d680e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d680e-124">CommonParameters</span></span>
<span data-ttu-id="d680e-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d680e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d680e-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d680e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d680e-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d680e-127">INPUTS</span></span>

### <span data-ttu-id="d680e-128">ASRFabric</span><span class="sxs-lookup"><span data-stu-id="d680e-128">ASRFabric</span></span>
<span data-ttu-id="d680e-129">Parametre ' Fabric ', ardışık düzenin ' ASRFabric ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="d680e-129">Parameter 'Fabric' accepts value of type 'ASRFabric' from the pipeline</span></span>

### <span data-ttu-id="d680e-130">Dizisi</span><span class="sxs-lookup"><span data-stu-id="d680e-130">String</span></span>
<span data-ttu-id="d680e-131">' FriendlyName ' parametresi ardışık düzenin ' String ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="d680e-131">Parameter 'FriendlyName' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="d680e-132">Dizisi</span><span class="sxs-lookup"><span data-stu-id="d680e-132">String</span></span>
<span data-ttu-id="d680e-133">' FriendlyName ' parametresi ardışık düzenin ' String ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="d680e-133">Parameter 'FriendlyName' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="d680e-134">Dizisi</span><span class="sxs-lookup"><span data-stu-id="d680e-134">String</span></span>
<span data-ttu-id="d680e-135">' Name ' parametresi ardışık düzenin ' String ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="d680e-135">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="d680e-136">Dizisi</span><span class="sxs-lookup"><span data-stu-id="d680e-136">String</span></span>
<span data-ttu-id="d680e-137">' Name ' parametresi ardışık düzenin ' String ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="d680e-137">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="d680e-138">ASRServer</span><span class="sxs-lookup"><span data-stu-id="d680e-138">ASRServer</span></span>
<span data-ttu-id="d680e-139">' Server ' parametresi ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="d680e-139">Parameter 'Server' accepts value of type 'ASRServer' from the pipeline</span></span>

## <span data-ttu-id="d680e-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d680e-140">OUTPUTS</span></span>

### <span data-ttu-id="d680e-141">System. Koleksiyonlar. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRNetwork]</span><span class="sxs-lookup"><span data-stu-id="d680e-141">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRNetwork]</span></span>

## <span data-ttu-id="d680e-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d680e-142">NOTES</span></span>

## <span data-ttu-id="d680e-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d680e-143">RELATED LINKS</span></span>

