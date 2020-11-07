---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 3F62A993-18BF-4189-A7C0-BB877F550AA5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryStorageClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryStorageClassification.md
ms.openlocfilehash: 8e2b563563ca50e0fdf6913a9e9999e1a642ff9e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764219"
---
# <span data-ttu-id="64ca2-101">Get-AzureRmSiteRecoveryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="64ca2-101">Get-AzureRmSiteRecoveryStorageClassification</span></span>

## <span data-ttu-id="64ca2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64ca2-102">SYNOPSIS</span></span>
<span data-ttu-id="64ca2-103">Site kurtarmada depolama sınıflandırmaları alır.</span><span class="sxs-lookup"><span data-stu-id="64ca2-103">Gets storage classifications in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64ca2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="64ca2-104">SYNTAX</span></span>

### <span data-ttu-id="64ca2-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="64ca2-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryStorageClassification [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64ca2-106">ByName</span><span class="sxs-lookup"><span data-stu-id="64ca2-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryStorageClassification -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="64ca2-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="64ca2-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryStorageClassification -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="64ca2-108">ByFabricObject</span><span class="sxs-lookup"><span data-stu-id="64ca2-108">ByFabricObject</span></span>
```
Get-AzureRmSiteRecoveryStorageClassification -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="64ca2-109">ByServerObject</span><span class="sxs-lookup"><span data-stu-id="64ca2-109">ByServerObject</span></span>
```
Get-AzureRmSiteRecoveryStorageClassification -Server <ASRServer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="64ca2-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="64ca2-110">DESCRIPTION</span></span>
<span data-ttu-id="64ca2-111">**Get-AzureRmSiteRecoveryStorageClassification** cmdlet 'ı Azure Site Recovery 'de depolama sınıflandırmaları alır.</span><span class="sxs-lookup"><span data-stu-id="64ca2-111">The **Get-AzureRmSiteRecoveryStorageClassification** cmdlet gets storage classifications in Azure Site Recovery.</span></span>

## <span data-ttu-id="64ca2-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="64ca2-112">EXAMPLES</span></span>

## <span data-ttu-id="64ca2-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="64ca2-113">PARAMETERS</span></span>

### <span data-ttu-id="64ca2-114">-Kumaş</span><span class="sxs-lookup"><span data-stu-id="64ca2-114">-Fabric</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRFabric
Parameter Sets: ByFabricObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64ca2-115">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="64ca2-115">-FriendlyName</span></span>
<span data-ttu-id="64ca2-116">Bu cmdlet 'in aldığı depolama sınıflandırmasının kolay adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="64ca2-116">Specifies the friendly name of the storage classification that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64ca2-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="64ca2-117">-Name</span></span>
<span data-ttu-id="64ca2-118">Bu cmdlet 'in aldığı depolama sınıflandırması 'nın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="64ca2-118">Specifies the name of the storage classification that this cmdlet gets.</span></span>

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

### <span data-ttu-id="64ca2-119">-Sunucu</span><span class="sxs-lookup"><span data-stu-id="64ca2-119">-Server</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRServer
Parameter Sets: ByServerObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64ca2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64ca2-120">-DefaultProfile</span></span>
<span data-ttu-id="64ca2-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="64ca2-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64ca2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64ca2-122">CommonParameters</span></span>
<span data-ttu-id="64ca2-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="64ca2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64ca2-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64ca2-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64ca2-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="64ca2-125">INPUTS</span></span>

### <span data-ttu-id="64ca2-126">ASRFabric</span><span class="sxs-lookup"><span data-stu-id="64ca2-126">ASRFabric</span></span>
<span data-ttu-id="64ca2-127">Parametre ' Fabric ', ardışık düzenin ' ASRFabric ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="64ca2-127">Parameter 'Fabric' accepts value of type 'ASRFabric' from the pipeline</span></span>

### <span data-ttu-id="64ca2-128">ASRServer</span><span class="sxs-lookup"><span data-stu-id="64ca2-128">ASRServer</span></span>
<span data-ttu-id="64ca2-129">' Server ' parametresi ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="64ca2-129">Parameter 'Server' accepts value of type 'ASRServer' from the pipeline</span></span>

## <span data-ttu-id="64ca2-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="64ca2-130">OUTPUTS</span></span>

### <span data-ttu-id="64ca2-131">System. Koleksiyonlar. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. Asrstoragec,</span><span class="sxs-lookup"><span data-stu-id="64ca2-131">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRStorageClassification]</span></span>

## <span data-ttu-id="64ca2-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="64ca2-132">NOTES</span></span>

## <span data-ttu-id="64ca2-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="64ca2-133">RELATED LINKS</span></span>

