---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDisk.md
ms.openlocfilehash: 3704dc536f727e530477965ef75710e50645c442
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752957"
---
# <span data-ttu-id="94cc4-101">Get-AzDisk</span><span class="sxs-lookup"><span data-stu-id="94cc4-101">Get-AzDisk</span></span>

## <span data-ttu-id="94cc4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94cc4-102">SYNOPSIS</span></span>
<span data-ttu-id="94cc4-103">Yönetilen diskin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="94cc4-103">Gets the properties of a Managed disk.</span></span>

## <span data-ttu-id="94cc4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="94cc4-104">SYNTAX</span></span>

```
Get-AzDisk [[-ResourceGroupName] <String>] [[-DiskName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="94cc4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="94cc4-105">DESCRIPTION</span></span>
<span data-ttu-id="94cc4-106">**Get-Azdısk** cmdlet 'ı, yönetilen bir diskin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="94cc4-106">The **Get-AzDisk** cmdlet gets the properties of a Managed disk.</span></span>

## <span data-ttu-id="94cc4-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="94cc4-107">EXAMPLES</span></span>

### <span data-ttu-id="94cc4-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="94cc4-108">Example 1</span></span>
```
PS C:\> Get-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'

ResourceGroupName  : ResourceGroup01
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.DiskSku
Zones              :
TimeCreated        : 6/29/2018 4:26:27 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
DiskIOPSReadWrite  : 500
DiskMBpsReadWrite  : 100
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compu
                     te/disks/Disk01
Name               : Disk01
Type               : Microsoft.Compute/disks
Location           : westus2
Tags               : {}
```

<span data-ttu-id="94cc4-109">Bu komut, ' ResourceGroup01 ' kaynak grubundaki ' Disk01 ' adındaki diskin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="94cc4-109">This command gets the properties of the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="94cc4-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="94cc4-110">Example 2</span></span>
```
PS C:\> Get-AzDisk -ResourceGroupName 'ResourceGroup01'

ResourceGroupName  : ResourceGroup01
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.DiskSku
Zones              :
TimeCreated        : 6/29/2018 4:26:27 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
DiskIOPSReadWrite  : 500
DiskMBpsReadWrite  : 100
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compu
                     te/disks/win1_OsDisk_1
Name               : win1_OsDisk_1
Type               : Microsoft.Compute/disks
Location           : westus2
Tags               : {}

ResourceGroupName  : ResourceGroup01
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.DiskSku
Zones              :
TimeCreated        : 6/29/2018 4:27:27 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
DiskIOPSReadWrite  : 500
DiskMBpsReadWrite  : 100
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compu
                     te/disks/win1_OsDisk_2
Name               : win1_OsDisk_2
Type               : Microsoft.Compute/disks
Location           : westus2
Tags               : {}
```

<span data-ttu-id="94cc4-111">Bu komut, ' ResourceGroup01 ' kaynak grubundaki tüm disklerin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="94cc4-111">This command gets the properties of all disks in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="94cc4-112">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="94cc4-112">Example 3</span></span>
```
PS C:\> Get-AzDisk

ResourceGroupName  : ResourceGroup01
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.DiskSku
Zones              :
TimeCreated        : 6/29/2018 4:26:27 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
DiskIOPSReadWrite  : 500
DiskMBpsReadWrite  : 100
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compu
                     te/disks/win1_OsDisk_1
Name               : win1_OsDisk_1
Type               : Microsoft.Compute/disks
Location           : westus2
Tags               : {}

ResourceGroupName  : ResourceGroup02
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.DiskSku
Zones              :
TimeCreated        : 6/29/2018 4:27:27 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
DiskIOPSReadWrite  : 500
DiskMBpsReadWrite  : 100
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup02/providers/Microsoft.Compu
                     te/disks/win1_OsDisk_2
Name               : win1_OsDisk_2
Type               : Microsoft.Compute/disks
Location           : westus2
Tags               : {}
```

<span data-ttu-id="94cc4-113">Bu komut, aboneliğin altındaki tüm disklerin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="94cc4-113">This command gets the properties of all disks under the subscription.</span></span>

### <span data-ttu-id="94cc4-114">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="94cc4-114">Example 4</span></span>
```
PS C:\> Get-AzDisk -Name win_OsDisk*

ResourceGroupName  : ResourceGroup01
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.DiskSku
Zones              :
TimeCreated        : 6/29/2018 4:26:27 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
DiskIOPSReadWrite  : 500
DiskMBpsReadWrite  : 100
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compu
                     te/disks/win1_OsDisk_1
Name               : win1_OsDisk_1
Type               : Microsoft.Compute/disks
Location           : westus2
Tags               : {}

ResourceGroupName  : ResourceGroup02
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.DiskSku
Zones              :
TimeCreated        : 6/29/2018 4:27:27 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
DiskIOPSReadWrite  : 500
DiskMBpsReadWrite  : 100
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup02/providers/Microsoft.Compu
                     te/disks/win1_OsDisk_2
Name               : win1_OsDisk_2
Type               : Microsoft.Compute/disks
Location           : westus2
Tags               : {}
```

<span data-ttu-id="94cc4-115">Bu komut, win1_OsDisk ile başlayan abonelik adının altındaki tüm disklerin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="94cc4-115">This command gets the properties of all disks under the subscription name starting with win1_OsDisk.</span></span>

## <span data-ttu-id="94cc4-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="94cc4-116">PARAMETERS</span></span>

### <span data-ttu-id="94cc4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94cc4-117">-DefaultProfile</span></span>
<span data-ttu-id="94cc4-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="94cc4-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94cc4-119">-DiskName</span><span class="sxs-lookup"><span data-stu-id="94cc4-119">-DiskName</span></span>
<span data-ttu-id="94cc4-120">Diskin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="94cc4-120">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="94cc4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94cc4-121">-ResourceGroupName</span></span>
<span data-ttu-id="94cc4-122">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="94cc4-122">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="94cc4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94cc4-123">CommonParameters</span></span>
<span data-ttu-id="94cc4-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="94cc4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94cc4-125">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="94cc4-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94cc4-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="94cc4-126">INPUTS</span></span>

### <span data-ttu-id="94cc4-127">System. String</span><span class="sxs-lookup"><span data-stu-id="94cc4-127">System.String</span></span>

## <span data-ttu-id="94cc4-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="94cc4-128">OUTPUTS</span></span>

### <span data-ttu-id="94cc4-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSDİsk</span><span class="sxs-lookup"><span data-stu-id="94cc4-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="94cc4-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="94cc4-130">NOTES</span></span>

## <span data-ttu-id="94cc4-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="94cc4-131">RELATED LINKS</span></span>
