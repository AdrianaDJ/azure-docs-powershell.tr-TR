---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrFabric.md
ms.openlocfilehash: c3bd5ecf7e3561be5f9e6b8d990c40281135982c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938211"
---
# <span data-ttu-id="1528e-101">Get-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="1528e-101">Get-AzRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="1528e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1528e-102">SYNOPSIS</span></span>
<span data-ttu-id="1528e-103">Azure Site kurtarma yapısı ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="1528e-103">Get the details of an Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="1528e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1528e-104">SYNTAX</span></span>

### <span data-ttu-id="1528e-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1528e-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrFabric [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1528e-106">ByName</span><span class="sxs-lookup"><span data-stu-id="1528e-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrFabric -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1528e-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="1528e-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrFabric -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1528e-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="1528e-108">DESCRIPTION</span></span>
<span data-ttu-id="1528e-109">**Get-AzRecoveryServicesAsrFabric** cmdlet 'i, belirli bir Azure Site Recovery yapısı veya kurtarma hizmeti kasasındaki tüm Azure Site kurtarma yapılarını alır.</span><span class="sxs-lookup"><span data-stu-id="1528e-109">The **Get-AzRecoveryServicesAsrFabric** cmdlet gets the properties of a specified Azure Site Recovery Fabric or all Azure Site Recovery Fabrics in a Recovery Service vault.</span></span>

## <span data-ttu-id="1528e-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1528e-110">EXAMPLES</span></span>

### <span data-ttu-id="1528e-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1528e-111">Example 1</span></span>
```
PS C:\> $fabrics = Get-AzRecoveryServicesAsrFabric
```

<span data-ttu-id="1528e-112">Kasadaki tüm Azure Site kurtarma yapılarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="1528e-112">Returns all the Azure Site Recovery fabrics in the vault.</span></span>

### <span data-ttu-id="1528e-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="1528e-113">Example 2</span></span>
```
PS C:\> $fabric = Get-AzRecoveryServicesAsrFabric -Name xxxx

Name                  : xxxx
FriendlyName          : XXXXXXXXXX
ID                    : /Subscriptions/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/XXXXXXXXXXXXX/replicationFabrics/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
FabricType            : VMware
SiteIdentifier        : XXXXXXXXxxxxxxxxxxx
FabricSpecificDetails : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificDetails
```

<span data-ttu-id="1528e-114">Adı xxxx olan Azure Site kurtarma yapısı.</span><span class="sxs-lookup"><span data-stu-id="1528e-114">Return azure site recovery fabric with name xxxx.</span></span>

### <span data-ttu-id="1528e-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="1528e-115">Example 3</span></span>
```
PS C:\> $fabric = Get-AzRecoveryServicesAsrFabric -FriendlyName XXXXXXXXXX

Name                  : xxxx
FriendlyName          : XXXXXXXXXX
ID                    : /Subscriptions/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/XXXXXXXXXXXXX/replicationFabrics/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
FabricType            : VMware
SiteIdentifier        : XXXXXXXXxxxxxxxxxxx
FabricSpecificDetails : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificDetails
```

<span data-ttu-id="1528e-116">Ad ve ad</span><span class="sxs-lookup"><span data-stu-id="1528e-116">Return azure site recovery fabric with friendly name xxxx.</span></span>

## <span data-ttu-id="1528e-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1528e-117">PARAMETERS</span></span>

### <span data-ttu-id="1528e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1528e-118">-DefaultProfile</span></span>
<span data-ttu-id="1528e-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1528e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1528e-120">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="1528e-120">-FriendlyName</span></span>
<span data-ttu-id="1528e-121">, Dokunun kolay adıyla ASR dokusunda arama yapın.</span><span class="sxs-lookup"><span data-stu-id="1528e-121">Search for the ASR fabric by the friendly name of the fabric.</span></span>

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

### <span data-ttu-id="1528e-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="1528e-122">-Name</span></span>
<span data-ttu-id="1528e-123">, Dokunun adına göre ASR yapınızı arayın.</span><span class="sxs-lookup"><span data-stu-id="1528e-123">Search for the ASR fabric by the name of the fabric.</span></span>

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

### <span data-ttu-id="1528e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1528e-124">CommonParameters</span></span>
<span data-ttu-id="1528e-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1528e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1528e-126">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1528e-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1528e-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1528e-127">INPUTS</span></span>

### <span data-ttu-id="1528e-128">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="1528e-128">None</span></span>

## <span data-ttu-id="1528e-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1528e-129">OUTPUTS</span></span>

### <span data-ttu-id="1528e-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="1528e-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="1528e-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1528e-131">NOTES</span></span>

## <span data-ttu-id="1528e-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1528e-132">RELATED LINKS</span></span>

[<span data-ttu-id="1528e-133">Yeni-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="1528e-133">New-AzRecoveryServicesAsrFabric</span></span>](./New-AzRecoveryServicesAsrFabric.md)

[<span data-ttu-id="1528e-134">Remove-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="1528e-134">Remove-AzRecoveryServicesAsrFabric</span></span>](./Remove-AzRecoveryServicesAsrFabric.md)
