---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: BF6AA8D4-D624-4BE1-A393-1A43909450C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzAvailabilitySet.md
ms.openlocfilehash: cd61e2119ea84ccfc5fb6a7f5fe597e80c9fd417
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276792"
---
# <span data-ttu-id="a4bbb-101">New-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="a4bbb-101">New-AzAvailabilitySet</span></span>

## <span data-ttu-id="a4bbb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4bbb-102">SYNOPSIS</span></span>
<span data-ttu-id="a4bbb-103">Azure kullanılabilirlik kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a4bbb-103">Creates an Azure availability set.</span></span>

## <span data-ttu-id="a4bbb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a4bbb-104">SYNTAX</span></span>

```
New-AzAvailabilitySet [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-PlatformUpdateDomainCount] <Int32>] [[-PlatformFaultDomainCount] <Int32>] [[-Sku] <String>]
 [-ProximityPlacementGroupId <String>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a4bbb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a4bbb-105">DESCRIPTION</span></span>
<span data-ttu-id="a4bbb-106">**New-AzAvailabilitySet** cmdlet 'ı bir Azure kullanılabilirlik kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a4bbb-106">The **New-AzAvailabilitySet** cmdlet creates an Azure availability set.</span></span>

## <span data-ttu-id="a4bbb-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a4bbb-107">EXAMPLES</span></span>

### <span data-ttu-id="a4bbb-108">Örnek 1: kullanılabilirlik kümesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="a4bbb-108">Example 1: Create an availability set</span></span>
```
PS C:\> New-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" -Location "West US"
```

<span data-ttu-id="a4bbb-109">Bu komut, ResourceGroup11 adlı kaynak grubunda AvailabilitySet03 adlı bir kullanılabilirlik kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a4bbb-109">This command creates an availability set named AvailabilitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="a4bbb-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a4bbb-110">PARAMETERS</span></span>

### <span data-ttu-id="a4bbb-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="a4bbb-111">-AsJob</span></span>
<span data-ttu-id="a4bbb-112">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="a4bbb-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="a4bbb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4bbb-113">-DefaultProfile</span></span>
<span data-ttu-id="a4bbb-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a4bbb-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4bbb-115">-Konum</span><span class="sxs-lookup"><span data-stu-id="a4bbb-115">-Location</span></span>
<span data-ttu-id="a4bbb-116">Kullanılabilirlik kümesinin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a4bbb-116">Specifies the location for the availability set.</span></span>

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

### <span data-ttu-id="a4bbb-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="a4bbb-117">-Name</span></span>
<span data-ttu-id="a4bbb-118">Kullanılabilirlik kümesi için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="a4bbb-118">Specifies a name for the availability set.</span></span>

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

### <span data-ttu-id="a4bbb-119">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="a4bbb-119">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="a4bbb-120">Platform hatası etki alanı sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a4bbb-120">Specifies the platform fault domain count.</span></span>

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

### <span data-ttu-id="a4bbb-121">-PlatformUpdateDomainCount</span><span class="sxs-lookup"><span data-stu-id="a4bbb-121">-PlatformUpdateDomainCount</span></span>
<span data-ttu-id="a4bbb-122">Platform Güncelleştirmesi etki alanı sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a4bbb-122">Specifies the platform update domain count.</span></span>

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

### <span data-ttu-id="a4bbb-123">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="a4bbb-123">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="a4bbb-124">Bu kullanılabilirlik kümesiyle kullanılacak yakınlık yerleşimi grubunun kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="a4bbb-124">The resource id of the Proximity Placement Group to use with this availability set.</span></span>

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

### <span data-ttu-id="a4bbb-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4bbb-125">-ResourceGroupName</span></span>
<span data-ttu-id="a4bbb-126">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a4bbb-126">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="a4bbb-127">-SKU</span><span class="sxs-lookup"><span data-stu-id="a4bbb-127">-Sku</span></span>
<span data-ttu-id="a4bbb-128">SKU 'nun adı.</span><span class="sxs-lookup"><span data-stu-id="a4bbb-128">The Name of Sku.</span></span>
<span data-ttu-id="a4bbb-129">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="a4bbb-129">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a4bbb-130">Hizalanmış: yönetilen diskler Için</span><span class="sxs-lookup"><span data-stu-id="a4bbb-130">Aligned: For managed disks</span></span>
- <span data-ttu-id="a4bbb-131">Klasik: yönetilmeyen diskler Için</span><span class="sxs-lookup"><span data-stu-id="a4bbb-131">Classic: For unmanaged disks</span></span>

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

### <span data-ttu-id="a4bbb-132">Etiketli</span><span class="sxs-lookup"><span data-stu-id="a4bbb-132">-Tag</span></span>
<span data-ttu-id="a4bbb-133">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="a4bbb-133">Key-value pairs in the form of a hash table.</span></span>

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

### <span data-ttu-id="a4bbb-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4bbb-134">CommonParameters</span></span>
<span data-ttu-id="a4bbb-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a4bbb-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4bbb-136">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a4bbb-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4bbb-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a4bbb-137">INPUTS</span></span>

### <span data-ttu-id="a4bbb-138">System. String</span><span class="sxs-lookup"><span data-stu-id="a4bbb-138">System.String</span></span>

### <span data-ttu-id="a4bbb-139">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="a4bbb-139">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="a4bbb-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a4bbb-140">OUTPUTS</span></span>

### <span data-ttu-id="a4bbb-141">Microsoft. Azure. Commands. COMPUTE. modeller. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="a4bbb-141">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="a4bbb-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a4bbb-142">NOTES</span></span>

## <span data-ttu-id="a4bbb-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a4bbb-143">RELATED LINKS</span></span>

[<span data-ttu-id="a4bbb-144">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="a4bbb-144">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="a4bbb-145">Remove-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="a4bbb-145">Remove-AzAvailabilitySet</span></span>](./Remove-AzAvailabilitySet.md)


