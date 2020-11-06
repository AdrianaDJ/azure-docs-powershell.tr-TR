---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: BF6AA8D4-D624-4BE1-A393-1A43909450C4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmAvailabilitySet.md
ms.openlocfilehash: b5e9828c0cf9f73f88a44b7a4471a22bbfbe49af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589876"
---
# <span data-ttu-id="26b26-101">New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="26b26-101">New-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="26b26-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26b26-102">SYNOPSIS</span></span>
<span data-ttu-id="26b26-103">Azure kullanılabilirlik kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="26b26-103">Creates an Azure availability set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26b26-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="26b26-104">SYNTAX</span></span>

```
New-AzureRmAvailabilitySet [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-PlatformUpdateDomainCount] <Int32>] [[-PlatformFaultDomainCount] <Int32>] [[-Sku] <String>] [-Managed]
 [<CommonParameters>]
```

## <span data-ttu-id="26b26-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="26b26-105">DESCRIPTION</span></span>
<span data-ttu-id="26b26-106">**Yeni-AzureRmAvailabilitySet** cmdlet 'ı bir Azure kullanılabilirlik kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="26b26-106">The **New-AzureRmAvailabilitySet** cmdlet creates an Azure availability set.</span></span>

## <span data-ttu-id="26b26-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="26b26-107">EXAMPLES</span></span>

### <span data-ttu-id="26b26-108">Örnek 1: kullanılabilirlik kümesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="26b26-108">Example 1: Create an availability set</span></span>
```
PS C:\> New-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" -Location "West US"
```

<span data-ttu-id="26b26-109">Bu komut, ResourceGroup11 adlı kaynak grubunda AvailablitySet03 adlı bir kullanılabilirlik kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="26b26-109">This command creates an availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="26b26-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="26b26-110">PARAMETERS</span></span>

### <span data-ttu-id="26b26-111">-Konum</span><span class="sxs-lookup"><span data-stu-id="26b26-111">-Location</span></span>
<span data-ttu-id="26b26-112">Kullanılabilirlik kümesinin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="26b26-112">Specifies the location for the availability set.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26b26-113">-Yönetilen</span><span class="sxs-lookup"><span data-stu-id="26b26-113">-Managed</span></span>
<span data-ttu-id="26b26-114">Yönetilen kullanılabilirlik kümesi</span><span class="sxs-lookup"><span data-stu-id="26b26-114">Managed Availability Set</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26b26-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="26b26-115">-Name</span></span>
<span data-ttu-id="26b26-116">Kullanılabilirlik kümesi için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="26b26-116">Specifies a name for the availability set.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26b26-117">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="26b26-117">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="26b26-118">Platform hatası etki alanı sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="26b26-118">Specifies the platform fault domain count.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26b26-119">-PlatformUpdateDomainCount</span><span class="sxs-lookup"><span data-stu-id="26b26-119">-PlatformUpdateDomainCount</span></span>
<span data-ttu-id="26b26-120">Platform Güncelleştirmesi etki alanı sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="26b26-120">Specifies the platform update domain count.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26b26-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26b26-121">-ResourceGroupName</span></span>
<span data-ttu-id="26b26-122">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="26b26-122">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26b26-123">-SKU</span><span class="sxs-lookup"><span data-stu-id="26b26-123">-Sku</span></span>
<span data-ttu-id="26b26-124">SKU 'nun adı</span><span class="sxs-lookup"><span data-stu-id="26b26-124">The Name of Sku</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26b26-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26b26-125">CommonParameters</span></span>
<span data-ttu-id="26b26-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="26b26-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26b26-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26b26-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26b26-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="26b26-128">INPUTS</span></span>

### <span data-ttu-id="26b26-129">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="26b26-129">None</span></span>
<span data-ttu-id="26b26-130">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="26b26-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="26b26-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="26b26-131">OUTPUTS</span></span>

## <span data-ttu-id="26b26-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="26b26-132">NOTES</span></span>

## <span data-ttu-id="26b26-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="26b26-133">RELATED LINKS</span></span>

[<span data-ttu-id="26b26-134">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="26b26-134">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="26b26-135">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="26b26-135">Remove-AzureRmAvailabilitySet</span></span>](./Remove-AzureRmAvailabilitySet.md)


