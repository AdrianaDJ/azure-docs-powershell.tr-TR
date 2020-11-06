---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrFabric.md
ms.openlocfilehash: 92631a1a6c5d27953777efe2b6ea158f59da8fdb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587471"
---
# <span data-ttu-id="387de-101">Get-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="387de-101">Get-AzureRmRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="387de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="387de-102">SYNOPSIS</span></span>
<span data-ttu-id="387de-103">Azure Site kurtarma yapısı ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="387de-103">Get the details of an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="387de-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="387de-104">SYNTAX</span></span>

### <span data-ttu-id="387de-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="387de-105">Default (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrFabric [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="387de-106">ByName</span><span class="sxs-lookup"><span data-stu-id="387de-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrFabric -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="387de-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="387de-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrFabric -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="387de-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="387de-108">DESCRIPTION</span></span>
<span data-ttu-id="387de-109">**Get-AzureRmRecoveryServicesAsrFabric** cmdlet 'i, belirli bir Azure Site Recovery yapısı veya kurtarma hizmeti kasasındaki tüm Azure Site kurtarma yapılarını alır.</span><span class="sxs-lookup"><span data-stu-id="387de-109">The **Get-AzureRmRecoveryServicesAsrFabric** cmdlet gets the properties of a specified Azure Site Recovery Fabric or all Azure Site Recovery Fabrics in a Recovery Service vault.</span></span>

## <span data-ttu-id="387de-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="387de-110">EXAMPLES</span></span>

### <span data-ttu-id="387de-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="387de-111">Example 1</span></span>
```
PS C:\> $fabrics = Get-AzureRmRecoveryServicesAsrFabric
```

<span data-ttu-id="387de-112">Kasadaki tüm Azure Site kurtarma yapılarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="387de-112">Returns all the Azure Site Recovery fabrics in the vault.</span></span>

### <span data-ttu-id="387de-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="387de-113">Example 2</span></span>
```
PS C:\> $fabric = Get-AzureRmRecoveryServicesAsrFabric -Name xxxx

Name                  : xxxx
FriendlyName          : XXXXXXXXXX
ID                    : /Subscriptions/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/XXXXXXXXXXXXX/replicationFabrics/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
FabricType            : VMware
SiteIdentifier        : XXXXXXXXxxxxxxxxxxx
FabricSpecificDetails : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificDetails
```

<span data-ttu-id="387de-114">Adı xxxx olan Azure Site kurtarma yapısı.</span><span class="sxs-lookup"><span data-stu-id="387de-114">Return azure site recovery fabric with name xxxx.</span></span>

### <span data-ttu-id="387de-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="387de-115">Example 3</span></span>
```
PS C:\> $fabric = Get-AzureRmRecoveryServicesAsrFabric -FriendlyName XXXXXXXXXX

Name                  : xxxx
FriendlyName          : XXXXXXXXXX
ID                    : /Subscriptions/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/XXXXXXXXXXXXX/replicationFabrics/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
FabricType            : VMware
SiteIdentifier        : XXXXXXXXxxxxxxxxxxx
FabricSpecificDetails : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificDetails
```

<span data-ttu-id="387de-116">Ad ve ad</span><span class="sxs-lookup"><span data-stu-id="387de-116">Return azure site recovery fabric with friendly name xxxx.</span></span>

## <span data-ttu-id="387de-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="387de-117">PARAMETERS</span></span>

### <span data-ttu-id="387de-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="387de-118">-DefaultProfile</span></span>
<span data-ttu-id="387de-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="387de-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="387de-120">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="387de-120">-FriendlyName</span></span>
<span data-ttu-id="387de-121">, Dokunun kolay adıyla ASR dokusunda arama yapın.</span><span class="sxs-lookup"><span data-stu-id="387de-121">Search for the ASR fabric by the friendly name of the fabric.</span></span>

```yaml
Type: String
Parameter Sets: ByFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="387de-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="387de-122">-Name</span></span>
<span data-ttu-id="387de-123">, Dokunun adına göre ASR yapınızı arayın.</span><span class="sxs-lookup"><span data-stu-id="387de-123">Search for the ASR fabric by the name of the fabric.</span></span>

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

### <span data-ttu-id="387de-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="387de-124">CommonParameters</span></span>
<span data-ttu-id="387de-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="387de-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="387de-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="387de-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="387de-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="387de-127">INPUTS</span></span>

### <span data-ttu-id="387de-128">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="387de-128">None</span></span>

## <span data-ttu-id="387de-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="387de-129">OUTPUTS</span></span>

### <span data-ttu-id="387de-130">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="387de-130">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="387de-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="387de-131">NOTES</span></span>

## <span data-ttu-id="387de-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="387de-132">RELATED LINKS</span></span>

[<span data-ttu-id="387de-133">Yeni-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="387de-133">New-AzureRmRecoveryServicesAsrFabric</span></span>](./New-AzureRmRecoveryServicesAsrFabric.md)

[<span data-ttu-id="387de-134">Remove-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="387de-134">Remove-AzureRmRecoveryServicesAsrFabric</span></span>](./Remove-AzureRmRecoveryServicesAsrFabric.md)
