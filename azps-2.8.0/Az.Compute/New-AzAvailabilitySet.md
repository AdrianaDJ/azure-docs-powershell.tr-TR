---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: BF6AA8D4-D624-4BE1-A393-1A43909450C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzAvailabilitySet.md
ms.openlocfilehash: 50aef7afbd90580bfbae34c9131353fcf29bf2f4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752870"
---
# <span data-ttu-id="e2272-101">New-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="e2272-101">New-AzAvailabilitySet</span></span>

## <span data-ttu-id="e2272-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2272-102">SYNOPSIS</span></span>
<span data-ttu-id="e2272-103">Azure kullanılabilirlik kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e2272-103">Creates an Azure availability set.</span></span>

## <span data-ttu-id="e2272-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e2272-104">SYNTAX</span></span>

```
New-AzAvailabilitySet [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-PlatformUpdateDomainCount] <Int32>] [[-PlatformFaultDomainCount] <Int32>] [[-Sku] <String>]
 [-ProximityPlacementGroupId <String>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e2272-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e2272-105">DESCRIPTION</span></span>
<span data-ttu-id="e2272-106">**New-AzAvailabilitySet** cmdlet 'ı bir Azure kullanılabilirlik kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e2272-106">The **New-AzAvailabilitySet** cmdlet creates an Azure availability set.</span></span>

## <span data-ttu-id="e2272-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e2272-107">EXAMPLES</span></span>

### <span data-ttu-id="e2272-108">Örnek 1: kullanılabilirlik kümesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="e2272-108">Example 1: Create an availability set</span></span>
```
PS C:\> New-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" -Location "West US"
```

<span data-ttu-id="e2272-109">Bu komut, ResourceGroup11 adlı kaynak grubunda AvailabilitySet03 adlı bir kullanılabilirlik kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e2272-109">This command creates an availability set named AvailabilitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="e2272-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e2272-110">PARAMETERS</span></span>

### <span data-ttu-id="e2272-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="e2272-111">-AsJob</span></span>
<span data-ttu-id="e2272-112">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="e2272-112">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2272-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2272-113">-DefaultProfile</span></span>
<span data-ttu-id="e2272-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e2272-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2272-115">-Konum</span><span class="sxs-lookup"><span data-stu-id="e2272-115">-Location</span></span>
<span data-ttu-id="e2272-116">Kullanılabilirlik kümesinin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="e2272-116">Specifies the location for the availability set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2272-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="e2272-117">-Name</span></span>
<span data-ttu-id="e2272-118">Kullanılabilirlik kümesi için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="e2272-118">Specifies a name for the availability set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2272-119">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="e2272-119">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="e2272-120">Platform hatası etki alanı sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e2272-120">Specifies the platform fault domain count.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2272-121">-PlatformUpdateDomainCount</span><span class="sxs-lookup"><span data-stu-id="e2272-121">-PlatformUpdateDomainCount</span></span>
<span data-ttu-id="e2272-122">Platform Güncelleştirmesi etki alanı sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e2272-122">Specifies the platform update domain count.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2272-123">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="e2272-123">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="e2272-124">ProximityPlacementGroup kimliği</span><span class="sxs-lookup"><span data-stu-id="e2272-124">The Id of ProximityPlacementGroup</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2272-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2272-125">-ResourceGroupName</span></span>
<span data-ttu-id="e2272-126">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e2272-126">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2272-127">-SKU</span><span class="sxs-lookup"><span data-stu-id="e2272-127">-Sku</span></span>
<span data-ttu-id="e2272-128">SKU 'nun adı.</span><span class="sxs-lookup"><span data-stu-id="e2272-128">The Name of Sku.</span></span>
<span data-ttu-id="e2272-129">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="e2272-129">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e2272-130">Hizalanmış: yönetilen diskler Için</span><span class="sxs-lookup"><span data-stu-id="e2272-130">Aligned: For managed disks</span></span>
- <span data-ttu-id="e2272-131">Klasik: yönetilmeyen diskler Için</span><span class="sxs-lookup"><span data-stu-id="e2272-131">Classic: For unmanaged disks</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2272-132">Etiketli</span><span class="sxs-lookup"><span data-stu-id="e2272-132">-Tag</span></span>
<span data-ttu-id="e2272-133">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="e2272-133">Key-value pairs in the form of a hash table.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2272-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2272-134">CommonParameters</span></span>
<span data-ttu-id="e2272-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e2272-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2272-136">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e2272-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2272-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e2272-137">INPUTS</span></span>

### <span data-ttu-id="e2272-138">System. String</span><span class="sxs-lookup"><span data-stu-id="e2272-138">System.String</span></span>

### <span data-ttu-id="e2272-139">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="e2272-139">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="e2272-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e2272-140">OUTPUTS</span></span>

### <span data-ttu-id="e2272-141">Microsoft. Azure. Commands. COMPUTE. modeller. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="e2272-141">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="e2272-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e2272-142">NOTES</span></span>

## <span data-ttu-id="e2272-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e2272-143">RELATED LINKS</span></span>

[<span data-ttu-id="e2272-144">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="e2272-144">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="e2272-145">Remove-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="e2272-145">Remove-AzAvailabilitySet</span></span>](./Remove-AzAvailabilitySet.md)

