---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: BF6AA8D4-D624-4BE1-A393-1A43909450C4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmAvailabilitySet.md
ms.openlocfilehash: 5a1d583d9eee535f519b6748867b4026dcc45006
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764157"
---
# <span data-ttu-id="90bb6-101">New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="90bb6-101">New-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="90bb6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90bb6-102">SYNOPSIS</span></span>
<span data-ttu-id="90bb6-103">Azure kullanılabilirlik kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="90bb6-103">Creates an Azure availability set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90bb6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="90bb6-104">SYNTAX</span></span>

```
New-AzureRmAvailabilitySet [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-PlatformUpdateDomainCount] <Int32>] [[-PlatformFaultDomainCount] <Int32>] [[-Sku] <String>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90bb6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="90bb6-105">DESCRIPTION</span></span>
<span data-ttu-id="90bb6-106">**Yeni-AzureRmAvailabilitySet** cmdlet 'ı bir Azure kullanılabilirlik kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="90bb6-106">The **New-AzureRmAvailabilitySet** cmdlet creates an Azure availability set.</span></span>

## <span data-ttu-id="90bb6-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="90bb6-107">EXAMPLES</span></span>

### <span data-ttu-id="90bb6-108">Örnek 1: kullanılabilirlik kümesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="90bb6-108">Example 1: Create an availability set</span></span>
```
PS C:\> New-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" -Location "West US"
```

<span data-ttu-id="90bb6-109">Bu komut, ResourceGroup11 adlı kaynak grubunda AvailablitySet03 adlı bir kullanılabilirlik kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="90bb6-109">This command creates an availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="90bb6-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="90bb6-110">PARAMETERS</span></span>

### <span data-ttu-id="90bb6-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="90bb6-111">-AsJob</span></span>
<span data-ttu-id="90bb6-112">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="90bb6-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="90bb6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90bb6-113">-DefaultProfile</span></span>
<span data-ttu-id="90bb6-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="90bb6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90bb6-115">-Konum</span><span class="sxs-lookup"><span data-stu-id="90bb6-115">-Location</span></span>
<span data-ttu-id="90bb6-116">Kullanılabilirlik kümesinin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="90bb6-116">Specifies the location for the availability set.</span></span>

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

### <span data-ttu-id="90bb6-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="90bb6-117">-Name</span></span>
<span data-ttu-id="90bb6-118">Kullanılabilirlik kümesi için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="90bb6-118">Specifies a name for the availability set.</span></span>

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

### <span data-ttu-id="90bb6-119">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="90bb6-119">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="90bb6-120">Platform hatası etki alanı sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="90bb6-120">Specifies the platform fault domain count.</span></span>

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

### <span data-ttu-id="90bb6-121">-PlatformUpdateDomainCount</span><span class="sxs-lookup"><span data-stu-id="90bb6-121">-PlatformUpdateDomainCount</span></span>
<span data-ttu-id="90bb6-122">Platform Güncelleştirmesi etki alanı sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="90bb6-122">Specifies the platform update domain count.</span></span>

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

### <span data-ttu-id="90bb6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90bb6-123">-ResourceGroupName</span></span>
<span data-ttu-id="90bb6-124">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="90bb6-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="90bb6-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="90bb6-125">-Sku</span></span>
<span data-ttu-id="90bb6-126">SKU 'nun adı.</span><span class="sxs-lookup"><span data-stu-id="90bb6-126">The Name of Sku.</span></span>
<span data-ttu-id="90bb6-127">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="90bb6-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="90bb6-128">Hizalanmış: yönetilen diskler Için</span><span class="sxs-lookup"><span data-stu-id="90bb6-128">Aligned: For managed disks</span></span>
- <span data-ttu-id="90bb6-129">Klasik: yönetilmeyen diskler Için</span><span class="sxs-lookup"><span data-stu-id="90bb6-129">Classic: For unmanaged disks</span></span>

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

### <span data-ttu-id="90bb6-130">Etiketli</span><span class="sxs-lookup"><span data-stu-id="90bb6-130">-Tag</span></span>
<span data-ttu-id="90bb6-131">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="90bb6-131">Key-value pairs in the form of a hash table.</span></span>

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

### <span data-ttu-id="90bb6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90bb6-132">CommonParameters</span></span>
<span data-ttu-id="90bb6-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="90bb6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90bb6-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90bb6-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90bb6-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="90bb6-135">INPUTS</span></span>

### <span data-ttu-id="90bb6-136">System. String</span><span class="sxs-lookup"><span data-stu-id="90bb6-136">System.String</span></span>

### <span data-ttu-id="90bb6-137">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="90bb6-137">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="90bb6-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="90bb6-138">OUTPUTS</span></span>

### <span data-ttu-id="90bb6-139">Microsoft. Azure. Commands. COMPUTE. modeller. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="90bb6-139">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="90bb6-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="90bb6-140">NOTES</span></span>

## <span data-ttu-id="90bb6-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="90bb6-141">RELATED LINKS</span></span>

[<span data-ttu-id="90bb6-142">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="90bb6-142">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="90bb6-143">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="90bb6-143">Remove-AzureRmAvailabilitySet</span></span>](./Remove-AzureRmAvailabilitySet.md)


