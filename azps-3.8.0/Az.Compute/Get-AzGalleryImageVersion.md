---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGalleryImageVersion.md
ms.openlocfilehash: 1385d4fe93157715ffdd521cfb62ed963b86e1ef
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94103688"
---
# <span data-ttu-id="bc7da-101">Get-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="bc7da-101">Get-AzGalleryImageVersion</span></span>

## <span data-ttu-id="bc7da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc7da-102">SYNOPSIS</span></span>
<span data-ttu-id="bc7da-103">Get veya LIST Galerisi görüntü sürümleri.</span><span class="sxs-lookup"><span data-stu-id="bc7da-103">Get or list gallery image versions.</span></span>

## <span data-ttu-id="bc7da-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bc7da-104">SYNTAX</span></span>

### <span data-ttu-id="bc7da-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bc7da-105">DefaultParameter (Default)</span></span>
```
Get-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [[-Name] <String>] [-ExpandReplicationStatus]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bc7da-106">Resourceıdparameter</span><span class="sxs-lookup"><span data-stu-id="bc7da-106">ResourceIdParameter</span></span>
```
Get-AzGalleryImageVersion [-ResourceId] <String> [-ExpandReplicationStatus]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc7da-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="bc7da-107">DESCRIPTION</span></span>
<span data-ttu-id="bc7da-108">Get veya LIST Galerisi görüntü sürümleri.</span><span class="sxs-lookup"><span data-stu-id="bc7da-108">Get or list gallery image versions.</span></span>

## <span data-ttu-id="bc7da-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bc7da-109">EXAMPLES</span></span>

### <span data-ttu-id="bc7da-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="bc7da-110">Example 1</span></span>
```powershell
PS C:\> Get-AzGalleryImageVersion -ResourceGroupName rg1 -GalleryName gallery1 -GalleryImageDefinitionName image1 -GalleryImageVersionName 1.0.0

ResourceGroupName        : rg1
PublishingProfile        :
  TargetRegions[0]       :
    Name                 : South Central US
    RegionalReplicaCount : 1
  TargetRegions[1]       :
    Name                 : East US 2
    RegionalReplicaCount : 2
  TargetRegions[2]       :
    Name                 : Central US
    RegionalReplicaCount : 1
  Source                 :
    ManagedImage         :
      Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/images/test1
  ReplicaCount           : 1
  ExcludeFromLatest      : False
  PublishedDate          : 11/14/2018 12:00:00 AM
  EndOfLifeDate          : 2/18/2025 12:07:00 PM
ProvisioningState        : Succeeded
StorageProfile           :
  OsDiskImage            :
    SizeInGB             : 127
    HostCaching          : ReadWrite
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/galleries/gallery1/images/image1/versions/1.0.0
Name                     : 1.0.0
Type                     : Microsoft.Compute/galleries/images/versions
Location                 : eastus2
Tags                     : {}
```

<span data-ttu-id="bc7da-111">Galeri görüntüsü sürümünü edinin.</span><span class="sxs-lookup"><span data-stu-id="bc7da-111">Get the gallery image version.</span></span>

### <span data-ttu-id="bc7da-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="bc7da-112">Example 2</span></span>
```powershell
PS C:\> Get-AzGalleryImageVersion -ResourceGroupName rg1 -GalleryName gallery1 -GalleryImageDefinitionName image1 -GalleryImageVersionName 1*

ResourceGroupName        : rg1
PublishingProfile        :
  TargetRegions[0]       :
    Name                 : South Central US
    RegionalReplicaCount : 1
  TargetRegions[1]       :
    Name                 : East US 2
    RegionalReplicaCount : 2
  TargetRegions[2]       :
    Name                 : Central US
    RegionalReplicaCount : 1
  Source                 :
    ManagedImage         :
      Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/images/test1
  ReplicaCount           : 1
  ExcludeFromLatest      : False
  PublishedDate          : 11/14/2018 12:00:00 AM
  EndOfLifeDate          : 2/18/2025 12:07:00 PM
ProvisioningState        : Succeeded
StorageProfile           :
  OsDiskImage            :
    SizeInGB             : 127
    HostCaching          : ReadWrite
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/galleries/gallery1/images/image1/versions/1.0.0
Name                     : 1.0.0
Type                     : Microsoft.Compute/galleries/images/versions
Location                 : eastus2
Tags                     : {}

ResourceGroupName        : rg1
PublishingProfile        :
  TargetRegions[0]       :
    Name                 : South Central US
    RegionalReplicaCount : 1
  TargetRegions[1]       :
    Name                 : East US 2
    RegionalReplicaCount : 2
  TargetRegions[2]       :
    Name                 : Central US
    RegionalReplicaCount : 1
  Source                 :
    ManagedImage         :
      Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/images/test1
  ReplicaCount           : 1
  ExcludeFromLatest      : False
  PublishedDate          : 11/14/2018 12:00:00 AM
  EndOfLifeDate          : 2/18/2025 12:07:00 PM
ProvisioningState        : Succeeded
StorageProfile           :
  OsDiskImage            :
    SizeInGB             : 127
    HostCaching          : ReadWrite
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/galleries/gallery1/images/image1/versions/1.1.0
Name                     : 1.1.0
Type                     : Microsoft.Compute/galleries/images/versions
Location                 : eastus2
Tags                     : {}
```

<span data-ttu-id="bc7da-113">"1" ile başlayan galeri görüntü sürümlerini edinin.</span><span class="sxs-lookup"><span data-stu-id="bc7da-113">Get the gallery image versions that starts with "1".</span></span>

### <span data-ttu-id="bc7da-114">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="bc7da-114">Example 3</span></span>
```powershell
PS C:\> Get-AzGalleryImageVersion -ResourceGroupName rg1 -GalleryName gallery1 -GalleryImageDefinitionName image1

ResourceGroupName        : rg1
PublishingProfile        :
  TargetRegions[0]       :
    Name                 : South Central US
    RegionalReplicaCount : 1
  TargetRegions[1]       :
    Name                 : East US 2
    RegionalReplicaCount : 2
  TargetRegions[2]       :
    Name                 : Central US
    RegionalReplicaCount : 1
  Source                 :
    ManagedImage         :
      Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/images/test1
  ReplicaCount           : 1
  ExcludeFromLatest      : False
  PublishedDate          : 11/14/2018 12:00:00 AM
  EndOfLifeDate          : 2/18/2025 12:07:00 PM
ProvisioningState        : Succeeded
StorageProfile           :
  OsDiskImage            :
    SizeInGB             : 127
    HostCaching          : ReadWrite
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/galleries/gallery1/images/image1/versions/1.0.0
Name                     : 1.0.0
Type                     : Microsoft.Compute/galleries/images/versions
Location                 : eastus2
Tags                     : {}

ResourceGroupName        : rg1
PublishingProfile        :
  TargetRegions[0]       :
    Name                 : South Central US
    RegionalReplicaCount : 1
  TargetRegions[1]       :
    Name                 : East US 2
    RegionalReplicaCount : 2
  TargetRegions[2]       :
    Name                 : Central US
    RegionalReplicaCount : 1
  Source                 :
    ManagedImage         :
      Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/images/test1
  ReplicaCount           : 1
  ExcludeFromLatest      : False
  PublishedDate          : 11/14/2018 12:00:00 AM
  EndOfLifeDate          : 2/18/2025 12:07:00 PM
ProvisioningState        : Succeeded
StorageProfile           :
  OsDiskImage            :
    SizeInGB             : 127
    HostCaching          : ReadWrite
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/galleries/gallery1/images/image1/versions/1.1.0
Name                     : 1.1.0
Type                     : Microsoft.Compute/galleries/images/versions
Location                 : eastus2
Tags                     : {}
```

<span data-ttu-id="bc7da-115">Tüm galeri görüntü sürümlerini edinin.</span><span class="sxs-lookup"><span data-stu-id="bc7da-115">Get all gallery image versions.</span></span>

## <span data-ttu-id="bc7da-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bc7da-116">PARAMETERS</span></span>

### <span data-ttu-id="bc7da-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc7da-117">-DefaultProfile</span></span>
<span data-ttu-id="bc7da-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bc7da-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc7da-119">-ExpandReplicationStatus</span><span class="sxs-lookup"><span data-stu-id="bc7da-119">-ExpandReplicationStatus</span></span>
<span data-ttu-id="bc7da-120">Çoğaltma durumunu göster.</span><span class="sxs-lookup"><span data-stu-id="bc7da-120">Show replication status.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc7da-121">-Gallerımagedefinitionname</span><span class="sxs-lookup"><span data-stu-id="bc7da-121">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="bc7da-122">Galeri resim tanımının adı.</span><span class="sxs-lookup"><span data-stu-id="bc7da-122">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc7da-123">-Gallertadı</span><span class="sxs-lookup"><span data-stu-id="bc7da-123">-GalleryName</span></span>
<span data-ttu-id="bc7da-124">Galeri adı.</span><span class="sxs-lookup"><span data-stu-id="bc7da-124">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc7da-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="bc7da-125">-Name</span></span>
<span data-ttu-id="bc7da-126">Galeri görüntüsü sürümünün adı.</span><span class="sxs-lookup"><span data-stu-id="bc7da-126">The name of the gallery image version.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryImageVersionName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="bc7da-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc7da-127">-ResourceGroupName</span></span>
<span data-ttu-id="bc7da-128">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="bc7da-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc7da-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="bc7da-129">-ResourceId</span></span>
<span data-ttu-id="bc7da-130">Galeri görüntüsü sürümü için kaynak KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="bc7da-130">The resource ID for the gallery image version</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc7da-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc7da-131">CommonParameters</span></span>
<span data-ttu-id="bc7da-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bc7da-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc7da-133">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="bc7da-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc7da-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bc7da-134">INPUTS</span></span>

### <span data-ttu-id="bc7da-135">System. String</span><span class="sxs-lookup"><span data-stu-id="bc7da-135">System.String</span></span>

### <span data-ttu-id="bc7da-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="bc7da-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="bc7da-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bc7da-137">OUTPUTS</span></span>

### <span data-ttu-id="bc7da-138">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psgallerımageversion</span><span class="sxs-lookup"><span data-stu-id="bc7da-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="bc7da-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bc7da-139">NOTES</span></span>

## <span data-ttu-id="bc7da-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bc7da-140">RELATED LINKS</span></span>
