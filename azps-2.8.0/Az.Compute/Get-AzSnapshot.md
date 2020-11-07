---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzSnapshot.md
ms.openlocfilehash: 534af1de5513520eeef02161916de6dce1655df4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752938"
---
# <span data-ttu-id="79bab-101">Get-AzSnapshot</span><span class="sxs-lookup"><span data-stu-id="79bab-101">Get-AzSnapshot</span></span>

## <span data-ttu-id="79bab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79bab-102">SYNOPSIS</span></span>
<span data-ttu-id="79bab-103">Anlık görüntünün özelliklerini alır</span><span class="sxs-lookup"><span data-stu-id="79bab-103">Gets the properties of a snapshot</span></span>

## <span data-ttu-id="79bab-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="79bab-104">SYNTAX</span></span>

```
Get-AzSnapshot [[-ResourceGroupName] <String>] [[-SnapshotName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79bab-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="79bab-105">DESCRIPTION</span></span>
<span data-ttu-id="79bab-106">**Get-azsnapshot** cmdlet 'inin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="79bab-106">The **Get-AzSnapshot** cmdlet gets the properties of a snapshot.</span></span>

## <span data-ttu-id="79bab-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="79bab-107">EXAMPLES</span></span>

### <span data-ttu-id="79bab-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="79bab-108">Example 1</span></span>
```
PS C:\> Get-AzSnapshot

ResourceGroupName  : ResourceGroupName1
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.SnapshotSku
TimeCreated        : 4/10/2018 7:05:42 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroupName1/providers/Microsoft.Compu
                     te/snapshots/SnapshotName1
Name               : SnapshotName1
Type               : Microsoft.Compute/snapshots
Location           : westus2
Tags               : {}

ResourceGroupName  : ResourceGroupName1
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.SnapshotSku
TimeCreated        : 4/10/2018 7:05:42 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroupName1/providers/Microsoft.Compu
                     te/snapshots/SnapshotName2
Name               : SnapshotName2
Type               : Microsoft.Compute/snapshots
Location           : westus2
Tags               : {}

ResourceGroupName  : ResourceGroupName2
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.SnapshotSku
TimeCreated        : 4/10/2018 7:05:42 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroupName2/providers/Microsoft.Compu
                     te/snapshots/SnapshotName3
Name               : SnapshotName3
Type               : Microsoft.Compute/snapshots
Location           : westus2
Tags               : {}
```

<span data-ttu-id="79bab-109">Bu komut, aboneliğin tüm anlık görüntülerinin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="79bab-109">This command gets the properties of all snapshots of the subscription.</span></span>

### <span data-ttu-id="79bab-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="79bab-110">Example 2</span></span>
```
PS C:\> Get-AzSnapshot -ResourceGroupName "ResourceGroupName1"

ResourceGroupName  : ResourceGroupName1
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.SnapshotSku
TimeCreated        : 4/10/2018 7:05:42 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroupName1/providers/Microsoft.Compu
                     te/snapshots/SnapshotName1
Name               : SnapshotName1
Type               : Microsoft.Compute/snapshots
Location           : westus2
Tags               : {}

ResourceGroupName  : ResourceGroupName1
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.SnapshotSku
TimeCreated        : 4/10/2018 7:05:42 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroupName1/providers/Microsoft.Compu
                     te/snapshots/SnapshotName2
Name               : SnapshotName2
Type               : Microsoft.Compute/snapshots
Location           : westus2
Tags               : {}
```

<span data-ttu-id="79bab-111">Bu komut, "ResourceGroupName1" adlı kaynak grubundaki tüm anlık görüntülerin özelliklerini alır</span><span class="sxs-lookup"><span data-stu-id="79bab-111">This command gets the properties of all snapshots in the resource group named "ResourceGroupName1"</span></span>

### <span data-ttu-id="79bab-112">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="79bab-112">Example 3</span></span>
```
PS C:\> Get-AzSnapshot -ResourceGroupName "ResourceGroupName1" -SnapshotName "SnapshotName1"

ResourceGroupName  : ResourceGroupName1
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.SnapshotSku
TimeCreated        : 4/10/2018 7:05:42 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroupName1/providers/Microsoft.Compu
                     te/snapshots/SnapshotName1
Name               : SnapshotName1
Type               : Microsoft.Compute/snapshots
Location           : westus2
Tags               : {}
```

<span data-ttu-id="79bab-113">Bu komut, "ResourceGroupName1" adlı kaynak grubundaki "SnapshotName1" adlı anlık görüntünün özelliklerini alır</span><span class="sxs-lookup"><span data-stu-id="79bab-113">This command gets the properties of the snapshot named "SnapshotName1" in the resource group named "ResourceGroupName1"</span></span>

### <span data-ttu-id="79bab-114">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="79bab-114">Example 4</span></span>
```
PS C:\> Get-AzSnapshot -SnapshotName "SnapshotName*"

ResourceGroupName  : ResourceGroupName1
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.SnapshotSku
TimeCreated        : 4/10/2018 7:05:42 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroupName1/providers/Microsoft.Compu
                     te/snapshots/SnapshotName1
Name               : SnapshotName1
Type               : Microsoft.Compute/snapshots
Location           : westus2
Tags               : {}

ResourceGroupName  : ResourceGroupName1
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.SnapshotSku
TimeCreated        : 4/10/2018 7:05:42 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroupName1/providers/Microsoft.Compu
                     te/snapshots/SnapshotName2
Name               : SnapshotName2
Type               : Microsoft.Compute/snapshots
Location           : westus2
Tags               : {}

ResourceGroupName  : ResourceGroupName2
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.SnapshotSku
TimeCreated        : 4/10/2018 7:05:42 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroupName2/providers/Microsoft.Compu
                     te/snapshots/SnapshotName3
Name               : SnapshotName3
Type               : Microsoft.Compute/snapshots
Location           : westus2
Tags               : {}
```

<span data-ttu-id="79bab-115">Bu komut, "SnapshotName" ile başlayan tüm anlık görüntüleri alır</span><span class="sxs-lookup"><span data-stu-id="79bab-115">This command gets all snapshots that start with "SnapshotName"</span></span>

## <span data-ttu-id="79bab-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="79bab-116">PARAMETERS</span></span>

### <span data-ttu-id="79bab-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79bab-117">-DefaultProfile</span></span>
<span data-ttu-id="79bab-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="79bab-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79bab-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79bab-119">-ResourceGroupName</span></span>
<span data-ttu-id="79bab-120">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="79bab-120">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="79bab-121">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="79bab-121">-SnapshotName</span></span>
<span data-ttu-id="79bab-122">Anlık görüntünün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="79bab-122">Specifies the name of a snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="79bab-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79bab-123">CommonParameters</span></span>
<span data-ttu-id="79bab-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="79bab-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79bab-125">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="79bab-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79bab-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="79bab-126">INPUTS</span></span>

### <span data-ttu-id="79bab-127">System. String</span><span class="sxs-lookup"><span data-stu-id="79bab-127">System.String</span></span>

## <span data-ttu-id="79bab-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="79bab-128">OUTPUTS</span></span>

### <span data-ttu-id="79bab-129">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="79bab-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="79bab-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="79bab-130">NOTES</span></span>

## <span data-ttu-id="79bab-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="79bab-131">RELATED LINKS</span></span>
