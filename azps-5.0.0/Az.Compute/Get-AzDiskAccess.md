---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskAccess.md
ms.openlocfilehash: 69f83b7c98850ba74476e6d81803e748f48bea6a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323362"
---
# <span data-ttu-id="e8d6d-101">Get-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="e8d6d-101">Get-AzDiskAccess</span></span>

## <span data-ttu-id="e8d6d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8d6d-102">SYNOPSIS</span></span>
<span data-ttu-id="e8d6d-103">Disk erişimler 'in özelliklerini alır</span><span class="sxs-lookup"><span data-stu-id="e8d6d-103">Gets the properties of Disk Accesses</span></span>

## <span data-ttu-id="e8d6d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e8d6d-104">SYNTAX</span></span>

### <span data-ttu-id="e8d6d-105">DefaultParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e8d6d-105">DefaultParameterSet (Default)</span></span>
```
Get-AzDiskAccess [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e8d6d-106">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="e8d6d-106">ResourceIDParameterSet</span></span>
```
Get-AzDiskAccess [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8d6d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e8d6d-107">DESCRIPTION</span></span>
<span data-ttu-id="e8d6d-108">**Get-AzDiskAccess** cmdlet 'ı disk erişiminin özelliklerini alır</span><span class="sxs-lookup"><span data-stu-id="e8d6d-108">The **Get-AzDiskAccess** cmdlet gets the properties of Disk Accesses</span></span>

## <span data-ttu-id="e8d6d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e8d6d-109">EXAMPLES</span></span>

### <span data-ttu-id="e8d6d-110">Örnek 1: varsayılan parametre kümesini kullanma</span><span class="sxs-lookup"><span data-stu-id="e8d6d-110">Example 1: Using Default Parameter Set</span></span> 
```
PS C:\> Get-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -Name 'DiskAccess01'

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:02:50 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccess01
Name                       : DiskAccess01
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}
```

<span data-ttu-id="e8d6d-111">Bu komut, ' ResourceGroup01 ' kaynak grubundaki ' DiskAccess01 ' adındaki disk erişim kaynağının özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="e8d6d-111">This command gets the properties of a Disk Access resource named 'DiskAccess01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="e8d6d-112">Örnek 2: kaynak grubuna göre Get-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="e8d6d-112">Example 2: Get-AzDiskAccess by Resource Group</span></span>
```
PS C:\> Get-AzDiskAccess -ResourceGroupName 'ResourceGroup01'

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:02:50 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccess01
Name                       : DiskAccess01
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:05:19 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccess02
Name                       : DiskAccess02
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}
```

<span data-ttu-id="e8d6d-113">Bu komut, ' ResourceGroup01 ' kaynak grubundaki tüm disk erişimleri özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="e8d6d-113">This command gets the properties of all disk accesses in the resource group 'ResourceGroup01'.</span></span>


### <span data-ttu-id="e8d6d-114">Örnek 3: tüm disk erişimini alma</span><span class="sxs-lookup"><span data-stu-id="e8d6d-114">Example 3: Getting all Disk Access</span></span>
```
PS C:\> Get-AzDiskAccess

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:02:50 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccess01
Name                       : DiskAccess01
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:05:19 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup21/providers/Microsoft.Compute/diskAccesses/DiskAccess02
Name                       : DiskAccess02
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:05:19 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup08/providers/Microsoft.Compute/diskAccesses/DiskAccess03
Name                       : DiskAccess03
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}
```

<span data-ttu-id="e8d6d-115">Bu komut, aboneliğin altındaki tüm disk erişimleri özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="e8d6d-115">This command gets the properties of all disk accesses under the subscription.</span></span>

### <span data-ttu-id="e8d6d-116">Örnek 4: joker karakter kullanarak tüm disk erişimini alma</span><span class="sxs-lookup"><span data-stu-id="e8d6d-116">Example 4: Get all Disk Access using Wildcard Character</span></span>
```
PS C:\> Get-AzDiskAccess -Name DiskAccessMicrosoft*

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:02:50 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccessMicrosoftAzure
Name                       : DiskAccessMicrosoftAzure
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:05:19 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccessMicrosoftTeams
Name                       : DiskAccessMicrosoftTeams
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}
```

<span data-ttu-id="e8d6d-117">Bu komut, abonelik adı altındaki ' DiskAccessMicrosoft ' ile başlayan tüm disk erişimleri özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="e8d6d-117">This command gets the properties of all disk accesses under the subscription name starting with 'DiskAccessMicrosoft'.</span></span>

### <span data-ttu-id="e8d6d-118">Örnek 5: ResourceId kullanarak disk erişimi alma.</span><span class="sxs-lookup"><span data-stu-id="e8d6d-118">Example 5: Get Disk Access using ResourceId.</span></span>
```
PS C:\> Get-AzDiskAccess -ResourceId '/subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccess01'

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:02:50 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccess01
Name                       : DiskAccess01
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}
```

<span data-ttu-id="e8d6d-119">Bu komut, verilen RESOURCEID ile disk erişiminin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="e8d6d-119">This command gets the properties of a Disk Access with the given ResourceId.</span></span>


## <span data-ttu-id="e8d6d-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e8d6d-120">PARAMETERS</span></span>

### <span data-ttu-id="e8d6d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8d6d-121">-DefaultProfile</span></span>
<span data-ttu-id="e8d6d-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e8d6d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8d6d-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="e8d6d-123">-Name</span></span>
<span data-ttu-id="e8d6d-124">Disk erişiminin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e8d6d-124">Specifies the name of a disk access.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases: diskAccessName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="e8d6d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8d6d-125">-ResourceGroupName</span></span>
<span data-ttu-id="e8d6d-126">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e8d6d-126">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="e8d6d-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="e8d6d-127">-ResourceId</span></span>
<span data-ttu-id="e8d6d-128">Disk erişiminizin kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="e8d6d-128">Resource ID for your disk access.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIDParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8d6d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8d6d-129">CommonParameters</span></span>
<span data-ttu-id="e8d6d-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e8d6d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8d6d-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e8d6d-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8d6d-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e8d6d-132">INPUTS</span></span>

### <span data-ttu-id="e8d6d-133">System. String</span><span class="sxs-lookup"><span data-stu-id="e8d6d-133">System.String</span></span>

## <span data-ttu-id="e8d6d-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e8d6d-134">OUTPUTS</span></span>

### <span data-ttu-id="e8d6d-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSDısaccess</span><span class="sxs-lookup"><span data-stu-id="e8d6d-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span></span>

## <span data-ttu-id="e8d6d-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e8d6d-136">NOTES</span></span>

## <span data-ttu-id="e8d6d-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e8d6d-137">RELATED LINKS</span></span>
